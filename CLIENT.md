# Queen's One-To-One
The Queen's OTO application works offline to ensure that no student data is accessible outside of the user's local machine. Therefore, there are a few tools that must be initially set up to get the application started.

# Initial Setup
## 1. Install Docker Desktop
The only external tool that is required to run Queen's OTO is Docker. The Docker engine is used to start/stop, download updates, and monitor the application. Essentially, the Docker engine communicates with our online services to fetch application updates and builds new app versions right on the user's local machine.

Head to the [Docker installation page](https://docs.docker.com/engine/install/) where install instructions for MacOS and Windows are available. Simply click on `Docker Desktop for Mac` or `Docker Desktop for Windows`, depending on your operating system of choice.

Once downloaded, ensure the Docker Engine is running before trying checking out the next step (start the Docker Desktop application).

## 2. Download Queen's OTO Package
The OTO dev team has bundled a range of scripts that will facilitate the use and maintenance of the application. Here's a brief overview of the package:
- `compose.yaml` is the file that describes how the Docker engine should set up the application. It should not be modified manually.
-  `init.ps1/init.sh` are both initialization scripts. The `.ps1` extension is for Windows Powershell users and the `.sh` file will work on the MacOS terminal. Windows users only require the .ps1 scripts, and Mac users only require the .sh scripts. This is the case with all subsequent scripts that will be mentioned. EXE files are also provided for Windows users. To execute them, simply double-click. This initialization script only needs to be run after the first time the user downloads this package. It creates the necessary folders and files for the application to run.
- `start` scripts will start the application if it is not already running.
- `stop` scripts will attempt to stop the application.
- `update` scripts will attempt to pull the latest updates from the dev team's codebase and will clean up any old versions before attempting to start the application.

Download the appropriate bundle from this repository. 
*MacOS users should download the Unix package*

## 3. Run the Initialization Script
Once the package is downloaded, the user can run the initialization script. To do this in Windows, find the unzipped folder, and simply click the `init.exe` executable.
*On MacOS, open a terminal in the folder location, type `./init.sh`*

The user should see that some folders and files have been created.
If everything ran smoothly, the user can now run the update script (same process as above) to pull down the latest version of the OTO application and start it up. Follow the prompts on the terminal to test out the application.

# Subsequent Process
If this isn't the first time the user starts the application, simply double-click the `start.exe` script or the `update.exe` script if the user received a notification that an update was available through email. They should then be able to access the updated application on any browser @ http://localhost:3000, as usual.

***For any questions about the initial setup or subsequent process, contact Samuel Emard-Thibault @ sam5thibault@gmail.com, 343-576-8776.***
