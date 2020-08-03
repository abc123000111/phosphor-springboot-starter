# phosphor-springboot
This is a pure springboot demo using Phosphor for dynamic taint analysis.  
  
IDE: IntelliJ IDEA  
  
Run/Debug Configurations:  
|- Main class: com.example.phosphorspringboot.PhosphorSpringbootApplication  
|- VM options: -Xbootclasspath/a:path_to_Phosphor-0.0.5-SNAPSHOT.jar -javaagent:path_to_Phosphor-0.0.5-SNAPSHOT.jar=cacheDir=path_to_temp  
|- Working directory: path_to_phosphor-springboot/src/main/java  
|- JRE: path_to_jre-inst  
  
An exception is reported during running:  
  
Exception in thread "main" java.lang.ClassFormatError: Duplicate method name&signature in class file org/springframework/util/ConcurrentReferenceHashMap$SoftEntryReference
	at java.lang.Throwable.fillInStackTrace$$PHOSPHORTAGGED(Throwable.java)
	at java.lang.Throwable.fillInStackTrace$$PHOSPHORTAGGED(Throwable.java:783)
	at java.lang.Throwable.<init>(Throwable.java:265)
	at java.lang.Error.<init>(Error.java:70)
	at java.lang.LinkageError.<init>(LinkageError.java:55)
	at java.lang.ClassFormatError.<init>(ClassFormatError.java:54)
	at java.lang.ClassFormatError.<init>(ClassFormatError.java)
	at java.lang.ClassLoader.defineClass1(Native Method)
	at java.lang.ClassLoader.defineClass1$$PHOSPHORTAGGED(ClassLoader.java)
	at java.lang.ClassLoader.defineClass$$PHOSPHORTAGGED(ClassLoader.java:763)
	at java.security.SecureClassLoader.defineClass$$PHOSPHORTAGGED(SecureClassLoader.java:142)
	at java.net.URLClassLoader.defineClass$$PHOSPHORTAGGED(URLClassLoader.java:467)
	at java.net.URLClassLoader.access$100$$PHOSPHORTAGGED(URLClassLoader.java:73)
	at java.net.URLClassLoader$1.run$$PHOSPHORTAGGED(URLClassLoader.java:368)
	at java.net.URLClassLoader$1.run(URLClassLoader.java:0)
	at java.net.URLClassLoader$1.run(URLClassLoader.java:362)
	at java.security.AccessController.doPrivileged(Native Method)
	at java.security.AccessController.doPrivileged$$PHOSPHORTAGGED(AccessController.java)
	at java.net.URLClassLoader.findClass$$PHOSPHORTAGGED(URLClassLoader.java:361)
	at java.lang.ClassLoader.loadClass$$PHOSPHORTAGGED(ClassLoader.java:424)
	at sun.misc.Launcher$AppClassLoader.loadClass$$PHOSPHORTAGGED(Launcher.java:335)
	at java.lang.ClassLoader.loadClass$$PHOSPHORTAGGED(ClassLoader.java:357)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:0)
	at org.springframework.util.ConcurrentReferenceHashMap$ReferenceManager.createReference$$PHOSPHORTAGGED(ConcurrentReferenceHashMap.java:1001)
	at org.springframework.util.ConcurrentReferenceHashMap$Segment.lambda$doTask$0$$PHOSPHORTAGGED(ConcurrentReferenceHashMap.java:533)
	at org.springframework.util.ConcurrentReferenceHashMap$1.execute$$PHOSPHORTAGGED(ConcurrentReferenceHashMap.java:294)
	at org.springframework.util.ConcurrentReferenceHashMap$Segment.doTask$$PHOSPHORTAGGED(ConcurrentReferenceHashMap.java:537)
	at org.springframework.util.ConcurrentReferenceHashMap.doTask$$PHOSPHORTAGGED(ConcurrentReferenceHashMap.java:419)
	at org.springframework.util.ConcurrentReferenceHashMap.put$$PHOSPHORTAGGED(ConcurrentReferenceHashMap.java:282)
	at org.springframework.util.ConcurrentReferenceHashMap.put$$PHOSPHORTAGGED(ConcurrentReferenceHashMap.java:271)
	at org.springframework.core.io.support.SpringFactoriesLoader.loadSpringFactories$$PHOSPHORTAGGED(SpringFactoriesLoader.java:147)
	at org.springframework.core.io.support.SpringFactoriesLoader.loadFactoryNames$$PHOSPHORTAGGED(SpringFactoriesLoader.java:122)
	at org.springframework.boot.SpringApplication.getSpringFactoriesInstances$$PHOSPHORTAGGED(SpringApplication.java:426)
	at org.springframework.boot.SpringApplication.getSpringFactoriesInstances$$PHOSPHORTAGGED(SpringApplication.java:420)
	at org.springframework.boot.SpringApplication.<init>(SpringApplication.java:272)
	at org.springframework.boot.SpringApplication.<init>(SpringApplication.java:253)
	at org.springframework.boot.SpringApplication.run$$PHOSPHORTAGGED(SpringApplication.java:1237)
	at org.springframework.boot.SpringApplication.run$$PHOSPHORTAGGED(SpringApplication.java:1226)
	at com.example.phosphorspringboot.PhosphorSpringbootApplication.main$$PHOSPHORTAGGED(PhosphorSpringbootApplication.java:14)
	at com.example.phosphorspringboot.PhosphorSpringbootApplication.main(PhosphorSpringbootApplication.java)
