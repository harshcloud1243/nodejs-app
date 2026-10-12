# Node.js Application Deployment 

## 1. Introduction

This project demonstrates the deployment of a Node.js application using Jenkins CI/CD, GitHub Webhook, and PM2.

The application is developed using Node.js and Express.js. The source code is stored in GitHub, and Jenkins is used to automate the deployment process. PM2 runs the Node.js application in the background.

### Technologies Used

* Node.js
* Express.js
* Git and GitHub
* Jenkins
* GitHub Webhook
* PM2
* Linux

## 2. Architectural Diagram

The project follows a CI/CD workflow in which GitHub stores the source code, a webhook triggers Jenkins, and PM2 manages the running Node.js application.

<img width="1672" height="941" alt="wide_flat_infographic_diagram_on_a_white_backgroun" src="https://github.com/user-attachments/assets/27eea5be-79b2-4373-a0ca-ed314927a1d5" />


### Architecture Workflow

1. Developer pushes code to GitHub.
2. GitHub Webhook triggers the Jenkins pipeline.
3. Jenkins checks out the source code and installs dependencies.
4. The application is deployed on a Linux server.
5. PM2 starts and manages the Node.js application in the background.
6. Users access the application through a web browser using port 3000.

Note: The exact automated steps depend on the configured Jenkins pipeline.

## 3. Output

The application displays the following message when the home route is accessed:

```text
Hiii from jenkins, added webhook, we are from 18 May Devops batch
```
<img width="1349" height="548" alt="Screenshot 2026-10-12 174239" src="https://github.com/user-attachments/assets/0f22948d-c7a6-4b6e-947c-707a58c09f9d" />


### Browser URL

```text
http://YOUR_PUBLIC_IP:3000/
```

Replace `YOUR_PUBLIC_IP` with the public IP address of your server.

The application must be running, and port 3000 must be allowed in the server's network security rules.

## 4. Input

The project uses the following files:

### app.js

This file contains the Node.js application code. It creates an Express server, defines the home route (`/`), and listens on port 3000.

### package.json

This file contains the project name, version, application entry point, start command, and Express.js dependency.

The configured start command is:

```bash
npm start
```

### Input Workflow

1. Developer writes or updates the application code.
2. The code is pushed to the GitHub repository.
3. Jenkins retrieves the code for the configured deployment process.

## 5. Background Process Using PM2

PM2 is a process manager used to run and manage Node.js applications in the background.

### Start the Application

```bash
sudo pm2 start app.js
```

### Check Application Status

```bash
sudo pm2 status
```

### View Application Logs

```bash
sudo pm2 logs
```

### Restart the Application

```bash
sudo pm2 restart app
```

### Stop the Application

```bash
sudo pm2 stop app
```

PM2 helps keep the application running in the background and provides process monitoring and restart capabilities.

## 6. Conclusion

This project demonstrates a basic Node.js application deployment workflow using GitHub, Jenkins, GitHub Webhook, and PM2.

It provides practical knowledge of source code management, CI/CD automation, Linux server deployment, and background process management using PM2.
