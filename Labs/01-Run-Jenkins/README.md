![](../../resources/logos.png)

----
# Jenkins Labs - Run Jenkins Server

[![Open in Cloud Shell](https://gstatic.com/cloudssh/images/open-btn.svg)](https://console.cloud.google.com/cloudshell/editor?cloudshell_git_repo=https://github.com/nirgeier/JenkinsLabs)

### **<kbd>CTRL</kbd> + click to open in new window**   

---

## 01. Run Jenkins Server
- For this demo we will use Jenkins with docker container. 
- Our image is build upon `jenkinsci/blueocean` and is pre-configured using `Jenkins Configuration as Code` [casc.yaml](./jenkins-casc-server/jenkins-casc.yaml) 
---
#### Start Jenkins
```sh
# Navigate to the custom image folder
cd ./Jenkins-casc-server

# Build and run the custom image
docker-compose up -d --build 
```

- Wait for the server to load and than open your browser at port 8888 (The port is defined inside the [.env](./Jenkins-casc-server/.env))
```sh
## .env
...
# Listen on the desired ports
# - Port 8888   exposes the web interface 
HOST_PORT_WEB=8888
```

---
:arrow_forward: [02-Download-Jenkins-CLI](../02-Download-Jenkins-CLI)