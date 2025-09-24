# Trello API Test Collection

This Postman collection provides automated tests for Trello, including happy path and negative scenarios. It covers creating boards, lists, cards, inviting/removing members, and cleanup operations.  

Official Trello API documentation:  
🔗 https://developer.atlassian.com/cloud/trello/rest/  
You can explore the full API test collection here:  
🔗 [View API Testing Documentation](https://documenter.getpostman.com/view/30403835/2sB3QCRt4B)

### 🌐  Public Postman Collection

Click the button below to **fork and import the collection and environment** directly into Postman:  

[<img src="https://run.pstmn.io/button.svg" alt="Run In Postman" style="width: 128px; height: 32px;">](https://app.getpostman.com/run-collection/30403835-d6b6cae0-4413-45d9-a05b-2ae09425ff64?action=collection%2Ffork&source=rip_markdown&collection-url=entityId%3D30403835-d6b6cae0-4413-45d9-a05b-2ae09425ff64%26entityType%3Dcollection%26workspaceId%3D020287ed-6d31-4e92-8db7-3a22c44625da#?env%5BTrelloAPI-Test%5D=W3sia2V5IjoiYmFzZVVybCIsInZhbHVlIjoiaHR0cHM6Ly9hcGkudHJlbGxvLmNvbS8xIiwiZW5hYmxlZCI6dHJ1ZSwidHlwZSI6ImRlZmF1bHQiLCJzZXNzaW9uVmFsdWUiOiJodHRwczovL2FwaS50cmVsbG8uY29tLzEiLCJjb21wbGV0ZVNlc3Npb25WYWx1ZSI6Imh0dHBzOi8vYXBpLnRyZWxsby5jb20vMSIsInNlc3Npb25JbmRleCI6MH0seyJrZXkiOiJhcGlLZXkiLCJ2YWx1ZSI6IiIsImVuYWJsZWQiOnRydWUsInR5cGUiOiJkZWZhdWx0Iiwic2Vzc2lvblZhbHVlIjoiWU9VUl9BUElfS0VZIiwiY29tcGxldGVTZXNzaW9uVmFsdWUiOiJZT1VSX0FQSV9LRVkiLCJzZXNzaW9uSW5kZXgiOjF9LHsia2V5IjoidG9rZW4iLCJ2YWx1ZSI6IiIsImVuYWJsZWQiOnRydWUsInR5cGUiOiJkZWZhdWx0Iiwic2Vzc2lvblZhbHVlIjoiWU9VUl9UT0tFTiIsImNvbXBsZXRlU2Vzc2lvblZhbHVlIjoiWU9VUl9UT0tFTiIsInNlc3Npb25JbmRleCI6Mn1d)

After importing the collection and environment:

- The environment includes **placeholders** for `key` and `token` for security.
- For convenience, you can use the following **sample credentials** provided for this project (no personal data exposed):
  
   ```text
  key – d04f397d49182c8fc52f47e5c1591bd7
  token – ATTA074af120572f128adee6bd1d80a11a995e0f1be831be4bf739eae24bddf1c2b1C5FE8330
These are provided so you can run the tests immediately without creating a Trello account.
Using your own Trello account is also possible — simply replace the placeholders with your credentials.

### 📂 Files in This Repository

- **TrelloCollection.json** – Postman collection with requests and pre-request/test scripts 
- **TrelloEnv.json** – Environment file with variables (baseUrl, key, token) – key and token are empty for security, but sample is provided in this readme file  
- **package.json** – Optional NPM script to run the collection via Newman with HTML report generation  
- **README.md** – Project documentation

### ⚙️ Running Tests Locally
*Using Postman*  
1. Import TrelloCollection.json and TrelloEnv.json.
2. Fill in key and token in the environment.
3. Run the collection using Postman Runner.

*Using Newman* 
1. Install Newman globally (if not already): npm install  
   `-g newman newman-reporter-htmlextra`
2. Run the collection with the environment:  
   `newman run TrelloCollection.json -e TrelloEnv.json -r htmlextra`
3. Run script is defined in package.json to simplify running tests:  
   `newman run TrelloCollection.json -e TrelloEnv.json -r htmlextra --reporter-htmlextra-export ./newman/trello-report.html`  
    Then run: `npm run test:trello`

### 🧪 Folder & Request Descriptions

- Happy Path – Tests status codes, performance, headers, and performs cleanup of variables
- Negative Tests – Covers missing/invalid API key/token, invalid inputs, and nonexistent resources
- Requests include pre-request scripts, tests, and collection variables for dynamic execution


