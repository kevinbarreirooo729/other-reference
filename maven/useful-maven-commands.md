### Initiate a maven project.
* For Windows or Linux Terminal: 
  * mvn archetype:generate -DgroupId=com.themastersdev.httptest -DartifactId=HttpTestApp -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false
* Note -> -DartifactId defines the project's name; -DgroupId defines the package name; Check pom.xml within the project structure to edit project metadata;

### Run a maven project
* In the Windows Terminal run the following command in the maven project root folder:
  * ./mvnw spring-boot:run
