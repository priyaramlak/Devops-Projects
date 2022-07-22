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
 
 
