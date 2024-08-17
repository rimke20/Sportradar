# Postman Collection Setup and Test Execution Instructions

In this file instructions will be written on how to import and run Postman collections and environment files in Postman.

## Prerequisites

Before you start make sure that you have these:

- Postman account - you can register at https://www.postman.com/
- You can use Postman in your browser without downloading the desktop application. Go to https://www.postman.com/ and login with your account.
- Postman – Download and install the Postman desktop application. You can download the application from the url https://www.postman.com/.

## Step 1: Import Postman Collection

1. Open Postman.
2. Click on “Import” button at the top left corner on the Postman application.
3. Click "select files" button and locate the exported Postman collection JSON file.
4. Select the JSON File then click open button.
5. The collection should now be visible under Collections tabs on left sidebar.

## Step 2: Import Postman Environment

1. Repeat the steps mentioned in the first step
2. Click on “Import” button at the top left corner on the Postman application.
3. Click "select files" button and locate the exported Postman environment JSON file.
4. Select the JSON File then click open button.
5. The collection should now be visible under Environments tabs on left sidebar.

## Step 3: Selecting the Environment

1. In Postman, you will see a dropdown located in the top right corner of its window. When no environment is selected it will have the text - no environment.
2. Choose it by clicking on the dropdown to select the imported environment from the list below.

## Step 4: Run Tests in Postman

1. Go to the Collections tab on the left sidebar.
2. Click on the collection that you imported - three dots next to the name of the collection.
3. Click on the Run collection button, which opens the Collection Runner.
4. Make sure the correct environment file is selected.
5. Click Run to execute all the requests in the collection, along with the associated tests.

## Step 5: View Test Results

1. After the collection run is complete, the results will be displayed in the Collection Runner window.
2. You can view the status of each request and see whether the tests passed or failed.

## Test Explanation

In my assignment I have written my test cases in the test_scenarios.md file. In my Postman tests I have written expected error messages for the test flows that could not be tested properly due to the API restrictions.
I have mostly written functional tests and an example of performance testing in the Register test scenario.
I have also added the whole collection of the tests as a whole for easier execution of all the tests using the Postman CLI.

## Instructions for Postman CLI

1. Install Postman CLI for MAC:

- Open new terminal
- enter command: curl -o- "https://dl-cli.pstmn.io/install/osx_64.sh" | sh

2. Go to Postman on web or the application
3. Login with user
4. Find the collection you want to run
5. Click three dots next to the name of the collection
6. Click Run Collection
7. Under "Choose how to run your collection" select automate runs via CLI
8. For instructions how to download Postman CLI click the link under "Run on Postman CLI" - information for different OS.
9. Click on Add API key
10. Generate new or use existing API key for the user
11. Enter name for the API key
12. Click Insert Key
13. Copy command and run it in terminal
14. User will be logged in
15. Press enter again to execute test script
16. Check test results in terminal or go to url that is generated at the end of the script and open it in browser
