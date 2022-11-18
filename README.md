# CMPG-323-Project
This is a CMPG 323 project I will be working on for this semester

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
        
  
   Screenshot of API MANAGEMENT:
   
   ![API_MANAGEMENT](https://user-images.githubusercontent.com/90704811/189646362-63a5ae28-a95a-432a-b784-cf10ab40ae72.png)
        
 ## Reference List
  https://www.flagship.io/git-branching-strategies/#:~:text=A%20branching%20strategy%2C%20therefore%2C%20is,interact%20with%20a%20shared%20codebase
