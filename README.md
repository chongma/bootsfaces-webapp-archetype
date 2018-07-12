# bootsfaces-webapp-archetype
Webapp archetype for BootsFaces

This archetype should be available at Maven central at  
`<groupId>net.bootsfaces</groupId>`  
`<artifactId>bootsfaces-webapp-archetype</artifactId>`  
`<version>1.2.0</version>`  

If you cannot get it at Maven you can clone this project and install it into your local Maven catalog (.m2)  
`git clone https://github.com/chongma/bootsfaces-webapp-archetype.git`  
`cd bootsfaces-webapp-archetype`  
`mvn install archetype:update-local-catalog`  

## Command line usage

To create a runnable BootsFaces project using this archetype install maven and then run the following from the command line  
`mvn archetype:generate -DarchetypeGroupId=net.bootsfaces -DarchetypeArtifactId=bootsfaces-webapp-archetype -DarchetypeVersion=1.2.0`

Maven will prompt you for a groupId, artifactId, version and package, e.g.  
`Define value for property 'groupId': test`  
`Define value for property 'artifactId': test`  
`Define value for property 'version' 1.0-SNAPSHOT: :`  
`Define value for property 'package' test: :  ` 

## Starting the server

Change directory to the new project, e.g.  
`cd test`

To package the project and start the TomEE instance (make sure there are no other Application servers running on 8080)  
`mvn package tomee:start`

The test application can now be viewed at e.g.  
[http://localhost:8080/](http://localhost:8080/)

To stop the TomEE instance  
`mvn tomee:stop`

## Editing the files

If you are using the archetype to create a reproducer for the BootsFaces team the files you might need to edit are  
`src/main/java/beans/BookBean.java`  
`src/main/webapp/index.xhtml`  
`src/main/webapp/book.xhtml`  
`src/main/webapp/result.xhtml`  