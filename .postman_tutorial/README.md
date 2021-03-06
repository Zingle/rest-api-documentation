# Zingle API Postman Tutorial

[Postman](https://www.getpostman.com/) is a tool for exploring and testing APIs. Zingle has provided a Postman Collection, which is a group of API requests, to help introduce people to the Zingle API.  

To get started, click the button below, or you may import the collection and environment folders in this folder.

**Note** you will have to import the [environment file](https://raw.githubusercontent.com/Zingle/rest-api/master/.postman_tutorial/zingle_tutorial.postman_environment) after importing the collection.

[![Run in Postman](https://run.pstmn.io/button.svg)](https://www.getpostman.com/run-collection/01e478f68c71196fc86c#?env%5BZingle%20API%20Tutorial%5D=W3sia2V5IjoidXNlcm5hbWUiLCJ2YWx1ZSI6IllPVVJfWklOR0xFX1VTRVJOQU1FIiwidHlwZSI6InRleHQiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6InBhc3N3b3JkIiwidmFsdWUiOiJZT1VSX1pJTkdMRV9QQVNTV09SRCIsInR5cGUiOiJ0ZXh0IiwiZW5hYmxlZCI6dHJ1ZX0seyJrZXkiOiJ0ZXN0X3Bob25lX251bWJlciIsInZhbHVlIjoiWU9VUl9NT0JJTEVfUEhPTkVfTlVNQkVSIiwidHlwZSI6InRleHQiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6InNlcnZpY2VfaWQiLCJ2YWx1ZSI6IllPVVJfWklOR0xFX1NFUlZJQ0VfSUQiLCJ0eXBlIjoidGV4dCIsImVuYWJsZWQiOnRydWV9LHsia2V5Ijoic2VydmljZV9waG9uZV9udW1iZXIiLCJ2YWx1ZSI6IllPVVJfWklOR0xFX1NFUlZJQ0VfUEhPTkVfTlVNQkVSIiwidHlwZSI6InRleHQiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6InRlc3RfY29udGFjdF9pZCIsInZhbHVlIjoiWU9VUl9URVNUX0NPTlRBQ1RfSUQiLCJ0eXBlIjoidGV4dCIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoidGVzdF9sYWJlbF9pZCIsInZhbHVlIjoiWU9VUl9URVNUX0xBQkVMX0lEIiwidHlwZSI6InRleHQiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6InRlc3Rfd29ya2Zsb3dfaWQiLCJ2YWx1ZSI6IllPVVJfVEVTVF9XT1JLRkxPV19JRCIsInR5cGUiOiJ0ZXh0IiwiZW5hYmxlZCI6dHJ1ZX0seyJrZXkiOiJwaG9uZV9udW1iZXJfY2hhbm5lbF90eXBlX2lkIiwidmFsdWUiOiIwYTI5M2VhMy00NzIxLTQzM2UtYTAzMS02MTBlYmNmNDMyNTUiLCJ0eXBlIjoidGV4dCIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoiY29udGFjdF9jdXN0b21fZmllbGRfaWRfZmlyc3RfbmFtZSIsInZhbHVlIjoiZTAxYTM4NTYtODliMS00ZGI0LWJmNTYtMzhkNzk0NTRjOTIxIiwidHlwZSI6InRleHQiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6ImNvbnRhY3RfY3VzdG9tX2ZpZWxkX2lkX2xhc3RfbmFtZSIsInZhbHVlIjoiMGRmODA1MjQtM2IyNy00ZmIwLThlZWItYzgxYmQ0NDhkMjk0IiwidHlwZSI6InRleHQiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6ImNvbnRhY3RfY3VzdG9tX2ZpZWxkX2lkX3RpdGxlIiwidmFsdWUiOiI4NGQ2YTAzYS1hMDkzLTQ5NTEtYmQxMi02NTUxNTk3YmJiZjQiLCJ0eXBlIjoidGV4dCIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoiY29udGFjdF90aXRsZV9pZF9kciIsInZhbHVlIjoiYzU4NDNhNDQtNTZmZS00NWI5LWI5ZGUtZGVkMjdmNGEzNGMwIiwidHlwZSI6InRleHQiLCJlbmFibGVkIjp0cnVlfV0=)

## Setup

Once you've imported the collection and environment, you will need to input your Zingle username and password into the environment before you can run any of the requests in the collection.  In postman, click the Environments dropdown in the top-right corner and choose Manage Environments:

![Postman Environments Dropdown](https://github.com/Zingle/rest-api/blob/master/.postman_tutorial/images/postman_environments_dropdown.png "Postman Environments Dropdown")

In the Environments list, click on the Zingle API Tutorial Environment:

![Postman Environments List](https://github.com/Zingle/rest-api/blob/master/.postman_tutorial/images/postman_environments_list.png "Postman Environments List")

In the Manage Environments dialog, replace YOUR_ZINGLE_USERNAME and YOUR_ZINGLE_PASSWORD with the username and password you are using to access the API. You should also enter your own mobile phone number as the test_phone_number:

![Postman Manage Environment Dialog](https://github.com/Zingle/rest-api/blob/master/.postman_tutorial/images/postman_manage_environment.png "Postman Manage Environment Dialog")

## Tutorial Structure

The Postman collection is broken into four subfolders. They are organized in a way that introduces the simplest and most common API concepts first and gets more complex from there.  We recommend going through them in order.

### Populating Environment as you work through the tutorial

Each folder and request in the collection has a description. Some of these descriptions contain important information, such as prerequisites for running the request or environment variables that should be replaced with data returned by the request.  After selecting the request in Postman, click the arrow next to the collection name above the collection details to make sure the request description is visible:

![Postman Request Description](https://github.com/Zingle/rest-api/blob/master/.postman_tutorial/images/postman_request_description.png "Postman Request Description")

# Help
To report an issue with the API, please [Create a GitHub Issue](https://github.com/Zingle/rest-api/issues/new).








