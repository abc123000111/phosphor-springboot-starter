# phosphor-springboot
This is a pure springboot demo using Phosphor for dynamic taint analysis.  
  
IDE: IntelliJ IDEA  
  
Run/Debug Configurations:  
|- Main class: com.example.phosphorspringboot.PhosphorSpringbootApplication  
|- VM options: -Xbootclasspath/a:path_to_Phosphor-0.0.5-SNAPSHOT.jar -javaagent:path_to_Phosphor-0.0.5-SNAPSHOT.jar=cacheDir=path_to_temp  
|- Working directory: path_to_phosphor-springboot/src/main/java  
|- JRE: path_to_jre-inst  
