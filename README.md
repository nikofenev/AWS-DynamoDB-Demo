# AWS-DynamoDB-Demo

## Demo run AWS DynamoDB locally with Java.

#### Prerequisites:
1. AWS Account
2. DynamoDB [Download link](http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DynamoDBLocal.html)


===================================================================================



1. Create AWS Credentials (in order to use DynamoDB, aws credentials are required).
  - Log in to your aws account console.
  - In the search bar type IAM (Manage User Access and Encryption Keys)
  - Select "Users" from the left navigation tab.
  - If you don't have any users at the time select "Add User"
  - Type in username and check the "programatic access" checkbox and click Next.
  - Do not need to select group at this moment, click Create User.
  - When user is created you will have the option to Download .csv file. 
  - Save the file to your home directory (MacOS /Users/<YOUR_USERNAME>/credentials)

2. Configure AWS Credentials 
  - Open the "credentials" with text editor.
  - And format it to look like this: 
```
[default]
aws_access_key_id = <YOUR_ACCESS_KEY>
aws_secret_access_key = <YOUR_SECRET_ACCESS_KEY>
```



