Jenkins 1st Project-(Freestyle project)

Prerequisites:
        -->Jenkins Server
        ---> Sonarqube server
        ---->Nexus Repository
        ---->Apache Tomcat server
        
 Before starting the project we need to have all the above four servers installed and configured
 * In Jenkins, go to new item-->Freestyle project
 * Under source code management,give your git hub URL where your code resides and also configure your github password in Jenkins
 * Then in the build select "Invoke top level Maven target"( Since we are going to build Java project)
 * And also select Maven version
 * Goals To build the app- Clean package
 * Goals to push the code to Sonarqube - sonar:sonar
 * To combine both it is- clean package sonar:sonar
 Now build the Code
  * Then need to transfer it to Sonarqube to check the code vulnerabilites and bugs
    (And for this we need to update the sonarqube URL and token in pom.xml)
  * Once the code passed the checks in Sonarqube, need to send the artifact file or binary file(war file) to Nexus repository.
     (And for this we need to update the nexus username and password in settings.xml in maven-/var/lib/jenkins/tools/hudson.tasks.Maven_MavenInstallation/maven3.8.6/conf/settings.xml)

  * Once it got updated then we can start the build and the artifacts will save under snapshot repository in Nexus
  *
  
 
 
