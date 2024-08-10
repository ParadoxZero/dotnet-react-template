# Dotnet + React Template

Get started with your dotnet and react project using this template.

## How to use?

### Via Github
1. Navigate to https://github.com/ParadoxZero/dotnet-react-template.
2. Click on use this template

### Commandline
You can clone the repo and push it to your repo by editing the remote of the clone.
```
git clone https://github.com/ParadoxZero/dotnet-react-template
git remote set-url origin <your-repo>
git push -u origin main
```

### Editing the name
Since this is a pregenerated template. You will need to edit the name yourself. Effort has been made to keep this at minimum.
Edit the following - 

`package.json`
```
{
  "name": "dotnet-react-template",
.....
```

### Adding APIs
Follow your typical dotne workflow. You can create your controllers and services in the `api/` directory.

# Development
Use the steps below in your development work flow. Depending on whether you are working on client (UI) or
the server (API)

### Client/ WebUI
Client can be independently developed by standard vite - react dev flow - 
To start the client dev server just do - 
```bash
npm run dev 
```

If it's the first time. Make sure to run - 
```
npm install
```

### API server

If you want to test out E2E App. Build client before the server. Otherwise you can skip this. 
```
npm run build
```
This will populate the `wwwroot` folder with the client.
Then use the following command to run the dev server - 
```
dotnet run
```

You will need to confiure the dev envirement by creating a `appsettings.Development.json` based on the `appsettings.json` file.
Populate the connection string to be able to test out the server.

Example settings - 
```
  "CosmosDb": {
    "ConnectionString": "",
    "Database": "",
    "Container": ""
  },
  "EnableSwagger": false
```

If enabled, swagger will be available at `http://<origin>/swagger` URL. You can use the Swagger UI to test out APIs to ensure 
your changes work as expected.

Everything available in `appsettings.json` can be overriden by creating envirement variables witht the same name or 
with `CosmosDb:ConnectionString` like pattern for nested keys.
