**Dev Containers tutorial**

This guide will show you how to use Visual Studio Code (VS Code) inside a special kind of computer environment called a Docker container. You don't need to know much about Docker for this. 

Running VS Code in a Docker container is helpful because it lets you create a clean and isolated workspace for your coding projects, which is separate from your regular computer setup.


Before you begin, make sure you have Visual Studio Code installed on your computer.

# Install Docker
    Docker Desktop
      You can download and install Docker Desktop, which is one option for using Docker. Alternatively, you can choose an          alternative like running Docker on a remote server or using a Docker-compatible command-line interface (CLI).

# Start Docker
  Open the Docker Desktop application to launch Docker. You'll see it's running when you spot the Docker whale icon in         your activity tray.
  Docker may take a little time to fully start. If the whale icon is moving, it's likely still in the startup phase. You can   click on the icon to check its status.
![docker-status](https://github.com/HIMANSHIMANGLA/Python/assets/95236452/a5c74cb1-127a-4d36-b429-638a1f1cc224)

# Check Docker
  Once Docker is running, you can confirm that everything is working by opening a new terminal window and typing the command:
```
docker --version
# Docker version 18.09.2, build 6247962
```
# Install the extension
  With the Dev Containers extension, you can use Visual Studio Code within a Docker container.
  ![dev-containers-extension](https://github.com/HIMANSHIMANGLA/Python/assets/95236452/d6fd87f1-1618-4ccd-b505-bd6ca51bb628)
<img width="606" alt="dev-containers-commands-simple" src="https://github.com/HIMANSHIMANGLA/Python/assets/95236452/861cf9ee-7fec-48b3-8a02-cc3ce5fbc3fd">

# Check installation
  Once you've installed the Dev Containers extension, you'll notice a new item in the status bar on the far left side of       Visual Studio Code.
![remote-status-bar](https://github.com/HIMANSHIMANGLA/Python/assets/95236452/c416fc66-7cbd-42bd-88b9-02e04760c5db)
  The Remote Status bar item can easily indicate whether Visual Studio Code is running in a local or remote context. By        clicking on this item, you can access the Dev Containers commands.
  <img width="606" alt="dev-containers-commands-simple" src="https://github.com/HIMANSHIMANGLA/Python/assets/95236452/b99cec42-eedd-4d8c-815a-aad16caad4e3">

# Get the sample
    To create a Docker container, follow these steps:
      1. Open a GitHub repository with a Node.js project.
      2. Use the Command Palette by pressing F1.
      3. Run the command "Dev Containers: Try a Dev Container Sample..."
      4. From the list that appears, select the Node.js sample.
![select-a-sample](https://github.com/HIMANSHIMANGLA/Python/assets/95236452/3a372cf7-8c26-4059-8639-496e365aa5cb)
      5. Wait for the container to build.

Once the container is built, Visual Studio Code will automatically establish a connection to it. It will also map the project folder from your local computer into the container, making your project accessible and editable within the containerized environment.
![dev-container-progress](https://github.com/HIMANSHIMANGLA/Python/assets/95236452/037ea97a-efd5-4124-b1f7-a50d5163d5b9)

# Check the container
  Once the container is up and running, and you're connected to it, you'll notice a change in your remote context in the       bottom left corner of the Status bar.
![connected](https://github.com/HIMANSHIMANGLA/Python/assets/95236452/6776f301-da9e-47cc-97d7-aa38c2325c46)

# Check your environment
Working in a container has a benefit - you can use precise versions of dependencies required by your application without affecting your local development setup.
Here, the container is equipped with Node.js version 18. You can verify this by opening a new terminal using Terminal > New Terminal (Ctrl+Shift+`) and running the following command:
```
node --version; npm --version
```
This should show the following versions:
![version-check-updated](https://github.com/HIMANSHIMANGLA/Python/assets/95236452/cf4c86ac-a06a-46c0-8a6a-9547213d8533)

# Run the application
  Now, you can press F5, which will run the application within the container. When the process begins, go to     http://localhost:3000 in your web browser, and you should see the basic Node.js server up and running!
  ![hello-remote-world](https://github.com/HIMANSHIMANGLA/Python/assets/95236452/8c07e339-1999-479d-b72a-006944e8b272)

# Ending your container connection
  To conclude your session within the container and return to using VS Code locally, you can simply go to "File" > "Close   Remote Connection."
