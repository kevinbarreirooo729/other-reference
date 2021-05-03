### Initiate a maven project.
* For Windows or Linux Terminal: 
  * mvn archetype:generate -DgroupId=com.themastersdev.httptest -DartifactId=HttpTestApp -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false
* Note -> -DartifactId defines the project's name; -DgroupId defines the package name; Check pom.xml within the project structure to edit project metadata;

### Run a maven project
* In the Windows Terminal run the following command in the maven project root folder:
  * mvnw spring-boot:run

## Important Notes
* When using Maven with a project that was initialized with Spring Initializr, make sure the version of Java that Maven is using matches the version of Java that was chosen in Spring Initialzr. To check the version of Java that Maven is using run the following command in the Windows Terminal:
  * mvn --version

   #### If the version of Java that Maven is using needs to be changed, then change the version of Java given to the JAVA_HOME environment variable. The Spring application should now run without problems. 
