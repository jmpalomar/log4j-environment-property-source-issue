Steps to reproduce:

1. Build project `./gradlew build`
2. Run project `java -jar -jar build/libs/log4j-environment-property-source-issue-all.jar`
   As no configuration is provided no log message is printed to the console.
3. Run project `java -jar -jar build/libs/log4j-environment-property-source-issue-all.jar --spring.profiles.active=dev`
   As we provide a configuration log message is printed to the console.
4. Run project `LOG4J_CONFIGURATION_FILE=file:src/main/resources/log4j2.config java -jar build/libs/log4j-environment-property-source-issue-all.jar`
   When we provide configuration via environment variable log message is NOT printed to the console.
