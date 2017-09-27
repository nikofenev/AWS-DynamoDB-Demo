# AWS-DynamoDB- Java-Demo

## AWS DynamoDB running locally with Java using IntelliJ and Maven.
The demo performs basic operations 
Creates table, populates table, query table and inserts new item in the table. For more information go to 
[AWS Getting Started with DynamoDB](https://aws.amazon.com/dynamodb/getting-started/)

#### Prerequisites:
1. AWS Account
2. DynamoDB [Download link](http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DynamoDBLocal.html)


===================================================================================



###### 1. Create AWS Credentials (in order to use DynamoDB, aws credentials are required).
  - Log in to your aws account console.
  - In the search bar type IAM (Manage User Access and Encryption Keys)
  - Select "Users" from the left navigation tab.
  - If you don't have any users at the time select "Add User"
  - Type in username and check the "programatic access" checkbox and click Next.
  - Do not need to select group at this moment, click Create User.
  - When user is created you will have the option to Download .csv file. 
  - Save the file to your home directory (MacOS /Users/<YOUR_USERNAME>/credentials)

######  2. Configure AWS Credentials 
  - Open the "credentials" with text editor.
  - And format it to look like this: 
```
[default]
aws_access_key_id = <YOUR_ACCESS_KEY>
aws_secret_access_key = <YOUR_SECRET_ACCESS_KEY>
```
  - save the file and make sure there is no extension (.txt or .csv etc)
  - open terminal and in your home directory type:
  ```
  $ mkdir .aws
  $ cat credentials > .aws/credentials
  ```
  
  - the lines above will create the credentials file in ".aws" directory.

######  3. Create new IntelliJ Project
  - in this demo I use org.apache.maven.archetype.webapp
  - Open your pom.xml file and add the following dependencies:
  ```
  <dependencyManagement>
    <dependencies>
      <dependency>
        <groupId>com.amazonaws</groupId>
        <artifactId>aws-java-sdk-bom</artifactId>
        <version>1.11.106</version>
        <type>pom</type>
        <scope>import</scope>
      </dependency>
    </dependencies>
  </dependencyManagement>
  ```
  
  AND
  
  ```
  <dependency>
     <groupId>com.amazonaws</groupId>
     <artifactId>aws-java-sdk-s3</artifactId>
   </dependency>
   <dependency>
     <groupId>com.amazonaws</groupId>
     <artifactId>aws-java-sdk-dynamodb</artifactId>
   </dependency>
   ```
######  4. Open terminal.
  - Navigate to your DynamoDB_local_latest directory (see Prerequisites).
  - Type in the following command: 
  ```
  $ java -Djava.library.path=./DynamoDBLocal_lib -jar DynamoDBLocal.jar
  ```
  - the line above will start DynamoDB and it should look like this:
  ```
  Initializing DynamoDB Local with the following configuration:
  Port:	8000
  InMemory:	false
  DbPath:	null
  SharedDb:	false
  shouldDelayTransientStatuses:	false
  CorsParams:	*
  |
  ```
  - Leave it open and go back to your intelliJ project

######  5. In your intelliJ project click on MavenProject Lifecycle package.
######  6. In your intelliJ project click on MavenProject Lifecycle install.



######  7. Download and run the class MoviesCreateTable class [link](src/main/java/edu/MoviesCreateTable.java)
  - This class will create the Movies Table.
  

###### 8. Download and the class MoviesLoadData class [link](src/main/java/edu/MoviesLoadData.java)
  - This class will populate the data with the moviesdata.json bellow
  - Download moviesdata.json file [link](src/main/resources/moviedata.json)


######  10. Download and run MoviesQuery class [link](src/main/java/edu/MoviesQuery.java)
  - This class will query the data
  
######  11. Download and run MoviesItemOps01 class [link](src/main/java/edu/MoviesItemOps01.java)
  - This class will add new item to the Movies table.
  
===========================================================================

All information and code is retrieved from Amazon Web Services
  
  
  


