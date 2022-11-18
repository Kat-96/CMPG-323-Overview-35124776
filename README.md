# CMPG-323-Project
This is a CMPG 323 project I will be working on for this semester and I will be keeping record/overview of every project in this readme file to ensure easy navigation to the repositories I will be working in as well as provide a clear overview of how the whole project will look like.

## Repositories for each project 

## Project-1

In this project, [CMPG-323-Overview---35124776](https://github.com/Kat-96/CMPG-323-Overview---35124776) repo was created. It will serve as an overview for all the projects that I will be creating in the near future, and will help in keeping '@Kat-96 CMPG323 35124776 Kanban PROJECT' project up to date

## Project-2

In this project I will create a repo called [CMPG-323-Project2-35124776](https://github.com/Kat-96/CMPG-323-Project2-35124776), which will basically be used to keep the activities of project 2

## Project-3

For this project I will be creating a repo called [CMPG-323-Project3-35124776](https://github.com/Kat-96/CMPG-323-Project3-35124776), it will store the activities of project 3

## Project-4

[CMPG-323-Project4-35124776](https://github.com/Kat-96/CMPG-323-Project4-35124776) repo will be created, it will store the activities of project 4

## Project-5

[CMPG-323-Project5-35124776](https://github.com/Kat-96/CMPG-323-Project5-35124776) repo will be created, it will store the activities of project 5

## Diagram explaining project and repository context and how they are integrated
  ![PROJ_DIAGRAM](https://user-images.githubusercontent.com/90704811/185258451-8a78f6f5-faba-469d-b534-e618be914134.png)

## Branching Stratergies to be used
 I will make use of a Branching Stratergy known as GitHub Flow.
 I will create the main branch and then proceed to creating new branches that I will be working in such as feature branches that stem directly from the master, and then merged back into main.
 
  ![Branching_Stratergy_OR](https://user-images.githubusercontent.com/90704811/185413904-5fae41e3-b19c-463e-9590-4078b8187b22.png)
    
 ## The use of a .gitignore file within each project
   For projects 2,3,4, and 5, I will create a .gitignore file which will store all the files I do not want appearing in my git repository

 ## Storage of Credentials and Sensitive Information
  The storage of credentials and sensitive info will be done on Azure
  
  
## Overview for Projects: 
## Project 1
  Number of Items By label
  ![Number of Items by Label](https://user-images.githubusercontent.com/90704811/202712319-92101276-640e-46f6-832b-93d8d362a370.png)
  
  Number of Items By Sprint
  ![Number of Items by Sprint](https://user-images.githubusercontent.com/90704811/202713219-29d72763-9dcb-4e3b-945a-3ebb5b331295.png)

## Project 2
In this project I will be creating a CRUD RESTful API that will connect to a database storing IoT device data. The API will contain at least one get, post, patch and delete method per resource.

## List of all endpoints: 

### Register to get User autherization
#### Request Body
    curl -X 'POST' \
      'https://cmpg323appservice.azurewebsites.net/api/Authenticate/register' \
      -H 'accept: */*' \
      -H 'Content-Type: application/json' \
      -d '{
      "username": "12345678",
      "email": "Kat@gmail.com",
      "password": "Kat@123"
    }'

     
## User Login 
#### Request
      curl -X 'POST' \
      'https://cmpg323appservice.azurewebsites.net/api/Authenticate/login' \
      -H 'accept: */*' \
      -H 'Content-Type: application/json' \
      -d '{
      "username": "12345678",
      "password": "Kat@123"
      }'
        
//COPY TOKEN 

## Authorize
#### Response
  ![Authorization_Response](https://user-images.githubusercontent.com/90704811/189106951-42e3a336-f70e-454b-981f-cecfc9e4c770.png)
 
//Now the user has been authorized

## GET all Device entries
#### Request Body
        curl -X 'POST' \
      'https://cmpg323appservice.azurewebsites.net/api/Devices' \
      -H 'accept: text/plain' \
      -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJodHRwOi8vc2NoZW1hcy54bWxzb2FwLm9yZy93cy8yMDA1LzA1L2lkZW50aXR5L2NsYWltcy9uYW1lIjoiMTIzNDU2NzgiLCJqdGkiOiJlYWM0YWZhNS05MzQ2LTQ5ZTctODA0MC1kZjVlOTYxNmIyOGEiLCJleHAiOjE2NjI2NDUwODAsImlzcyI6Imh0dHA6Ly9sb2NhbGhvc3Q6NjE5NTUiLCJhdWQiOiJodHRwOi8vbG9jYWxob3N0OjQyMDAifQ.NYABV1eF-hKCI2759VTD4kUpQdYf81m4arfCaD__k9U' \
      -H 'Content-Type: application/json' \
      -d '{
      "deviceId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
      "deviceName": "Laptop",
      "categoryId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
      "zoneId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
      "status": "string",
      "isActvie": true,
      "dateCreated": "2022-09-08T11:08:40.758Z"
    }'
   
## Retrieve one Device from the database based on the ID parsed through
#### Request       
       curl -X 'GET' \
      'https://cmpg323appservice.azurewebsites.net/api/Devices/3fa85f64-5717-4562-b3fc-2c963f66afa6' \
      -H 'accept: text/plain' \
      -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJodHRwOi8vc2NoZW1hcy54bWxzb2FwLm9yZy93cy8yMDA1LzA1L2lkZW50aXR5L2NsYWltcy9uYW1lIjoiMTIzNDU2NzgiLCJqdGkiOiJlYWM0YWZhNS05MzQ2LTQ5ZTctODA0MC1kZjVlOTYxNmIyOGEiLCJleHAiOjE2NjI2NDUwODAsImlzcyI6Imh0dHA6Ly9sb2NhbGhvc3Q6NjE5NTUiLCJhdWQiOiJodHRwOi8vbG9jYWxob3N0OjQyMDAifQ.NYABV1eF-hKCI2759VTD4kUpQdYf81m4arfCaD__k9U'

## Create a new Device entry
#### Request
        curl -X 'POST' \
          'https://cmpg323appservice.azurewebsites.net/api/Devices' \
          -H 'accept: text/plain' \
          -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJodHRwOi8vc2NoZW1hcy54bWxzb2FwLm9yZy93cy8yMDA1LzA1L2lkZW50aXR5L2NsYWltcy9uYW1lIjoiMTIzNTY3ODkiLCJqdGkiOiI3NTA1NzI1OC0wZjg2LTQwNjAtYmUwMi03ZjgxMGY0NGY0ZDYiLCJleHAiOjE2NjI2NTQwOTcsImlzcyI6Imh0dHA6Ly9sb2NhbGhvc3Q6NjE5NTUiLCJhdWQiOiJodHRwOi8vbG9jYWxob3N0OjQyMDAifQ.2hQApxBBAa1JcK35FVHTtNuiH_WADFlDgqwatG_ltEw' \
          -H 'Content-Type: application/json' \
          -d '{
          "deviceId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
          "deviceName": "Phone",
          "categoryId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
          "zoneId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
          "status": "string",
          "isActvie": true,
          "dateCreated": "2022-09-08T13:48:08.054Z"
        }'
        
## update an existing Device entry
#### Request 
    curl -X 'PUT' \
      'https://cmpg323appservice.azurewebsites.net/api/Devices/3fa85f64-5717-4562-b3fc-2c963f66afa6' \
      -H 'accept: */*' \
      -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJodHRwOi8vc2NoZW1hcy54bWxzb2FwLm9yZy93cy8yMDA1LzA1L2lkZW50aXR5L2NsYWltcy9uYW1lIjoiMTIzNDU2NzgiLCJqdGkiOiJlYWM0YWZhNS05MzQ2LTQ5ZTctODA0MC1kZjVlOTYxNmIyOGEiLCJleHAiOjE2NjI2NDUwODAsImlzcyI6Imh0dHA6Ly9sb2NhbGhvc3Q6NjE5NTUiLCJhdWQiOiJodHRwOi8vbG9jYWxob3N0OjQyMDAifQ.NYABV1eF-hKCI2759VTD4kUpQdYf81m4arfCaD__k9U' \
      -H 'Content-Type: application/json' \
      -d '{
      "deviceId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
      "deviceName": "string",
      "categoryId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
      "zoneId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
      "status": "string",
      "isActvie": true,
      "dateCreated": "2022-09-08T11:49:28.223Z"
    }'
     
## Delete an existing Device entry

#### Request
        curl -X 'DELETE' \
          'https://cmpg323appservice.azurewebsites.net/api/Devices/3fa85f64-5717-4562-b3fc-2c963f66afa6' \
          -H 'accept: text/plain' \
          -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJodHRwOi8vc2NoZW1hcy54bWxzb2FwLm9yZy93cy8yMDA1LzA1L2lkZW50aXR5L2NsYWltcy9uYW1lIjoiMTIzNDU2NzgiLCJqdGkiOiJlYWM0YWZhNS05MzQ2LTQ5ZTctODA0MC1kZjVlOTYxNmIyOGEiLCJleHAiOjE2NjI2NDUwODAsImlzcyI6Imh0dHA6Ly9sb2NhbGhvc3Q6NjE5NTUiLCJhdWQiOiJodHRwOi8vbG9jYWxob3N0OjQyMDAifQ.NYABV1eF-hKCI2759VTD4kUpQdYf81m4arfCaD__k9U'
                
 ## Create a new Zone entry
 #### Request
         curl -X 'POST' \
          'https://cmpg323appservice.azurewebsites.net/api/Zones' \
          -H 'accept: text/plain' \
          -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJodHRwOi8vc2NoZW1hcy54bWxzb2FwLm9yZy93cy8yMDA1LzA1L2lkZW50aXR5L2NsYWltcy9uYW1lIjoiMTIzNTY3ODkiLCJqdGkiOiI3NTA1NzI1OC0wZjg2LTQwNjAtYmUwMi03ZjgxMGY0NGY0ZDYiLCJleHAiOjE2NjI2NTQwOTcsImlzcyI6Imh0dHA6Ly9sb2NhbGhvc3Q6NjE5NTUiLCJhdWQiOiJodHRwOi8vbG9jYWxob3N0OjQyMDAifQ.2hQApxBBAa1JcK35FVHTtNuiH_WADFlDgqwatG_ltEw' \
          -H 'Content-Type: application/json' \
          -d '{
          "zoneId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
          "zoneName": "first floor",
          "zoneDescription": "Room",
          "dateCreated": "2022-09-08T13:49:58.924Z"
        }'
 
#### Request
        curl -X 'POST' \
          'https://cmpg323appservice.azurewebsites.net/api/Zones' \
          -H 'accept: text/plain' \
          -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJodHRwOi8vc2NoZW1hcy54bWxzb2FwLm9yZy93cy8yMDA1LzA1L2lkZW50aXR5L2NsYWltcy9uYW1lIjoiMTIzNDU2NzgiLCJqdGkiOiJlYWM0YWZhNS05MzQ2LTQ5ZTctODA0MC1kZjVlOTYxNmIyOGEiLCJleHAiOjE2NjI2NDUwODAsImlzcyI6Imh0dHA6Ly9sb2NhbGhvc3Q6NjE5NTUiLCJhdWQiOiJodHRwOi8vbG9jYWxob3N0OjQyMDAifQ.NYABV1eF-hKCI2759VTD4kUpQdYf81m4arfCaD__k9U' \
          -H 'Content-Type: application/json' \
          -d '{
          "zoneId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
          "zoneName": "Zone",
          "zoneDescription": "string",
          "dateCreated": "2022-09-08T12:19:52.935Z"
        }
 
## Retrieve all Zone entries 
#### Request
        curl -X 'GET' \
          'https://cmpg323appservice.azurewebsites.net/api/Zones' \
          -H 'accept: text/plain' \
          -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJodHRwOi8vc2NoZW1hcy54bWxzb2FwLm9yZy93cy8yMDA1LzA1L2lkZW50aXR5L2NsYWltcy9uYW1lIjoiMTIzNDU2NzgiLCJqdGkiOiJlYWM0YWZhNS05MzQ2LTQ5ZTctODA0MC1kZjVlOTYxNmIyOGEiLCJleHAiOjE2NjI2NDUwODAsImlzcyI6Imh0dHA6Ly9sb2NhbGhvc3Q6NjE5NTUiLCJhdWQiOiJodHRwOi8vbG9jYWxob3N0OjQyMDAifQ.NYABV1eF-hKCI2759VTD4kUpQdYf81m4arfCaD__k9U'

## Retrieve one Zone from the database based on the ID parsed through
#### Request 
        curl -X 'GET' \
          'https://cmpg323appservice.azurewebsites.net/api/Zones/3fa85f64-5717-4562-b3fc-2c963f66afa6' \
          -H 'accept: text/plain' \
          -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJodHRwOi8vc2NoZW1hcy54bWxzb2FwLm9yZy93cy8yMDA1LzA1L2lkZW50aXR5L2NsYWltcy9uYW1lIjoiMTIzNDU2NzgiLCJqdGkiOiJlYWM0YWZhNS05MzQ2LTQ5ZTctODA0MC1kZjVlOTYxNmIyOGEiLCJleHAiOjE2NjI2NDUwODAsImlzcyI6Imh0dHA6Ly9sb2NhbGhvc3Q6NjE5NTUiLCJhdWQiOiJodHRwOi8vbG9jYWxob3N0OjQyMDAifQ.NYABV1eF-hKCI2759VTD4kUpQdYf81m4arfCaD__k9U'
          
## Delete an existing Zone entry on the database
#### Request
        curl -X 'DELETE' \
          'https://cmpg323appservice.azurewebsites.net/api/Zones/3fa85f64-5717-4562-b3fc-2c963f66afa6' \
          -H 'accept: text/plain' \
          -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJodHRwOi8vc2NoZW1hcy54bWxzb2FwLm9yZy93cy8yMDA1LzA1L2lkZW50aXR5L2NsYWltcy9uYW1lIjoiMTIzNDU2NzgiLCJqdGkiOiJlYWM0YWZhNS05MzQ2LTQ5ZTctODA0MC1kZjVlOTYxNmIyOGEiLCJleHAiOjE2NjI2NDUwODAsImlzcyI6Imh0dHA6Ly9sb2NhbGhvc3Q6NjE5NTUiLCJhdWQiOiJodHRwOi8vbG9jYWxob3N0OjQyMDAifQ.NYABV1eF-hKCI2759VTD4kUpQdYf81m4arfCaD__k9U'
           
## Update an existing Zone entry

#### Request
        curl -X 'PUT' \
          'https://cmpg323appservice.azurewebsites.net/api/Zones/3fa85f64-5717-4562-b3fc-2c963f66afa6' \
          -H 'accept: */*' \
          -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJodHRwOi8vc2NoZW1hcy54bWxzb2FwLm9yZy93cy8yMDA1LzA1L2lkZW50aXR5L2NsYWltcy9uYW1lIjoiMTIzNDU2NzgiLCJqdGkiOiJlYWM0YWZhNS05MzQ2LTQ5ZTctODA0MC1kZjVlOTYxNmIyOGEiLCJleHAiOjE2NjI2NDUwODAsImlzcyI6Imh0dHA6Ly9sb2NhbGhvc3Q6NjE5NTUiLCJhdWQiOiJodHRwOi8vbG9jYWxob3N0OjQyMDAifQ.NYABV1eF-hKCI2759VTD4kUpQdYf81m4arfCaD__k9U' \
          -H 'Content-Type: application/json' \
          -d '{
          "zoneId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
          "zoneName": "Zone1",
          "zoneDescription": "string",
          "dateCreated": "2022-09-08T12:47:56.270Z"
        }'
        
## Create a new Category entry
#### Request
        curl -X 'POST' \
          'https://cmpg323appservice.azurewebsites.net/api/Categories' \
          -H 'accept: text/plain' \
          -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJodHRwOi8vc2NoZW1hcy54bWxzb2FwLm9yZy93cy8yMDA1LzA1L2lkZW50aXR5L2NsYWltcy9uYW1lIjoiMTIzNTY3ODkiLCJqdGkiOiI3NTA1NzI1OC0wZjg2LTQwNjAtYmUwMi03ZjgxMGY0NGY0ZDYiLCJleHAiOjE2NjI2NTQwOTcsImlzcyI6Imh0dHA6Ly9sb2NhbGhvc3Q6NjE5NTUiLCJhdWQiOiJodHRwOi8vbG9jYWxob3N0OjQyMDAifQ.2hQApxBBAa1JcK35FVHTtNuiH_WADFlDgqwatG_ltEw' \
          -H 'Content-Type: application/json' \
          -d '{
          "categoryId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
          "categoryName": "Tv",
          "categoryDescription": "string",
          "dateCreated": "2022-09-08T13:24:25.756Z"
        }'
 
## Retrieves all Category entries
#### Request
        curl -X 'GET' \
          'https://cmpg323appservice.azurewebsites.net/api/Categories' \
          -H 'accept: text/plain' \
          -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJodHRwOi8vc2NoZW1hcy54bWxzb2FwLm9yZy93cy8yMDA1LzA1L2lkZW50aXR5L2NsYWltcy9uYW1lIjoiMTIzNTY3ODkiLCJqdGkiOiI3NTA1NzI1OC0wZjg2LTQwNjAtYmUwMi03ZjgxMGY0NGY0ZDYiLCJleHAiOjE2NjI2NTQwOTcsImlzcyI6Imh0dHA6Ly9sb2NhbGhvc3Q6NjE5NTUiLCJhdWQiOiJodHRwOi8vbG9jYWxob3N0OjQyMDAifQ.2hQApxBBAa1JcK35FVHTtNuiH_WADFlDgqwatG_ltEw'

## Retrieve one Category from the database based on the ID parsed through
#### Request
        curl -X 'GET' \
          'https://cmpg323appservice.azurewebsites.net/api/Categories/3fa85f64-5717-4562-b3fc-2c963f66afa6' \
          -H 'accept: text/plain' \
          -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJodHRwOi8vc2NoZW1hcy54bWxzb2FwLm9yZy93cy8yMDA1LzA1L2lkZW50aXR5L2NsYWltcy9uYW1lIjoiMTIzNTY3ODkiLCJqdGkiOiI3NTA1NzI1OC0wZjg2LTQwNjAtYmUwMi03ZjgxMGY0NGY0ZDYiLCJleHAiOjE2NjI2NTQwOTcsImlzcyI6Imh0dHA6Ly9sb2NhbGhvc3Q6NjE5NTUiLCJhdWQiOiJodHRwOi8vbG9jYWxob3N0OjQyMDAifQ.2hQApxBBAa1JcK35FVHTtNuiH_WADFlDgqwatG_ltEw'
               
## Update an existing Category
#### Request
        curl -X 'PUT' \
          'https://cmpg323appservice.azurewebsites.net/api/Categories/3fa85f64-5717-4562-b3fc-2c963f66afa6' \
          -H 'accept: */*' \
          -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJodHRwOi8vc2NoZW1hcy54bWxzb2FwLm9yZy93cy8yMDA1LzA1L2lkZW50aXR5L2NsYWltcy9uYW1lIjoiMTIzNTY3ODkiLCJqdGkiOiI3NTA1NzI1OC0wZjg2LTQwNjAtYmUwMi03ZjgxMGY0NGY0ZDYiLCJleHAiOjE2NjI2NTQwOTcsImlzcyI6Imh0dHA6Ly9sb2NhbGhvc3Q6NjE5NTUiLCJhdWQiOiJodHRwOi8vbG9jYWxob3N0OjQyMDAifQ.2hQApxBBAa1JcK35FVHTtNuiH_WADFlDgqwatG_ltEw' \
          -H 'Content-Type: application/json' \
          -d '{
          "categoryId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
          "categoryName": "Tv",
          "categoryDescription": "telecommunication medium for transmitting moving images and sound",
          "dateCreated": "2022-09-08T13:31:33.384Z"
        }'
        
  
 ## Screenshot of API MANAGEMENT:
   
   ![API_MANAGEMENT](https://user-images.githubusercontent.com/90704811/189646362-63a5ae28-a95a-432a-b784-cf10ab40ae72.png)
 
 ## Project 3
 In this project, I was given an existing ASP.NET Core MVC Web Application that needed 
to be enhanced and improved. Therefore, I: 
  * used .NET CORE MVC Application 
  * Applied Design Pattern
  * Published the App to the service hosted on Azure and ensured that the App is secure and accessible

# This is how the user would use the App
  * The user would use this url => https://cmpg323webapplication1.azurewebsites.net to navigate to the hosted web application.
  * The user can Register their own account and login with their provided credentials.
  
   ![Register](https://user-images.githubusercontent.com/90704811/193010714-6128c60d-14f4-41c0-ba7b-a74a6a25c455.png)

    
  * Or the user can use the provided Login credentials.
  
   ![LOGIN](https://user-images.githubusercontent.com/90704811/193010423-e25acfd3-bb0f-4490-8bd9-c0b6fe423776.png)

   
  * Once logged in, the Zones, Categories and Devices tabs will be available to the user. 
  
   ![HomeTab](https://user-images.githubusercontent.com/90704811/193009300-48689f72-f610-49e3-b643-920963aa7b27.png)
   
  * The user will use the "+" icon to Add Zones, Categories and Devices.
  
   ![Add](https://user-images.githubusercontent.com/90704811/193009869-3d283f9f-135b-4e9e-8e5d-0dad5d3db501.png) 
   
  * The user will use the pencil icon to Edit the existing Zones, Categories and Devices.
  * The user will use the eye icon to View existing Zones, Categories and Devices on the Web App.
  * The user will use the bin icon to Delete existing Zones, Categories and Devices on the web app from the database.
  
   ![Icons](https://user-images.githubusercontent.com/90704811/193010600-46d3a83b-0e32-4787-9b05-e0644fb3bc57.png)
   
  * All the entries will be saved and stored in the database database. 
  * The user can logout, using "logout button" on the menu tab, once they have added, edited or deleted all the Zones, Categories and Devices.

# Security
  To ensure that no credentials are stored on GitHub, I used the gitignore file to store any sensitive information
  
## Project 4
I will be making some Testing in this project, and I will be using Robotic Process Automation

--Robotic Process Automation (RPA) refers to the use of technology to mimic human tasks in the same way that a person would execute a process.

The project will be opened using UIPATH, where the automation will be implemented.

Actions to be performed:
1. Login 
2. Category
    * Creat Category
    * Delete Categories
    * Read Category
    * update Category
   
3. Device
    * Create Device
    * Delete Device
    * Read Device
    * Update Device
   
4. Zones
     * Delete Zones
     * Create Zones 
     * Read Zones
     * Update Zones

All the tests for the above can be found in their respective folders.

Orchestrator
![orchestrator screenshot](https://user-images.githubusercontent.com/90704811/198321653-b7ab4a55-794a-4ac7-9b0b-e69b47dda4b4.png)

## Project 5
# POWER BI

   Reporting project, The report will be built in Power BI.

   For this project I will be using PowerBI to help share data that the devices gather overtime through visualisations built into a report or dashboard.

   The usage of the IoT devices, as well as their statuses can be managed through the following reports:

    * High-Level Metrics
    * Device Monitoring 
    * Device Registration

# High-Level Metrics

    This is a report that shows how counts of data points based on information could impact decision making and it looks like this:
    
![High-Level-Metrics](https://user-images.githubusercontent.com/90704811/200970637-8fc8e80c-3a36-458a-99a3-6cbfc654e07d.png)

# Device Monitoring
In this page(report), the user can:

      * monitor devices per category
      * monitor devices per zone
      * monitor online versus offline devices (status should depict whether a device is online or offline)

![Device-Monitoring](https://user-images.githubusercontent.com/90704811/200970890-9a5d100e-c7ff-4c63-8d39-6dbd7cf9ac81.png)

# Device Registration
In this page(report), the user can use the visuals to view: 
      
      * how many devices have been registered over a timespan
      * how many categories of devices have been created
      * how many zones contain registered devices on a timeline


![Device Registration](https://user-images.githubusercontent.com/90704811/200971159-01352232-cf17-48c7-883d-02743bf1c1bb.png)

# Filtering

I also made use of filters that can be applied across pages and visuals
The filtering can be used to:

      * filter the report based on device category
      * filter the report based on device platform
      * filter the report based on device zone
      * filter the report based on device registration date

![Filter](https://user-images.githubusercontent.com/90704811/200971867-ef2f3178-b713-42e2-815e-f89302b0440b.png)
