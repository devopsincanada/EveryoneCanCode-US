# Setup Local Development Environment on Windows OS

⏲️ _Est. time to complete: 45 min._ ⏲️

## Here is what you will learn 🎯

You wil learn the following:

- Installing Git
- Installing Python
- Installing Python Libraries
- Setting up Python Virtual Environment
- Installing Visual Studio Code

## Table Of Contents

1. [Install Git](#install-git)
2. [Install Visual Studio Code](#install-visual-studio-code)
3. [Install Python](#install-python)
4. [Clone To-Do Application Repository](#clone-to-do-application-repo)
5. [Setup Python Virtual Environment](#setup-python-virtual-environment)

Depending on the operating system you are using, chose appropriate installation method below. For more details on Git and various installation refer to [Install Git on GitHub](https://github.com/git-guides/install-git)

### Install Git

Following the instruction below to install Git on Windows operating system. For detailed inf

- Verify if you already have the Git installed on your computer by checking below
  - On your computer from the the Widows task bar, search for command-line tool using "cmd", and open the command-line tool.
  ![Open Windows command-line window](../content-images/Sprint%2000/local/open-command-line-window.png)

  - Run command _git -v_ and verify output.
    If the Git not installed you will see error below.
    ![Output for Git not installed](../content-images/Sprint%2000/local/git-not-installed.png)

    If Git is installed you will see output below with Git version.
    ![Output for Git previously installed](../content-images/Sprint%2000/local/git-previously-installed.png)

- If Git is previously not installed, [click here to download](https://github.com/git-for-windows/git/releases/download/v2.44.0.windows.1/Git-2.44.0-64-bit.exe) Git installer for Windows.
- By default download file is located in the Download folder on your computer. If download location is changed, navigate to that location to install Git.
  ![Git installer location in download folder](../content-images/Sprint%2000/local/git-downloaded-installer.png)

- Double click on the Git installer file highlighted above to begin installation. You will Git setup menu as shown below, and click _Next_.
![Git installer setup menu](../content-images/Sprint%2000/local/git-installer-setup.png)

- Follow onscreen instructions and accept defaults folder to install Git, then click Nex to continue and accept all defaults until you reach Install option as shown below and click _Install_.

- Once the installation complete, uncheck _View release notes_ in the last screen and click _Finish_.


## Install Visual Studio Code

Follow the instructions below install VS Code on your computer. Visit [Visual Studio Code download page](https://code.visualstudio.com/download) to download latest version of installation package for your computer operating system.

- Download VS Code installer for Windows [by clicking here](https://code.visualstudio.com/sha/download?build=stable&os=win32-x64-user). This is a user installer to install for current user. Download [system installer](https://code.visualstudio.com/sha/download?build=stable&os=win32-x64) to install for all users using the computer. This will require elevation permissions to install for everyone.
- Go to _Downloads_ folder and double click VS Code installer to start installing
  ![VS Code installer in downloads folder](../content-images/Sprint%2000/local/vscode-installer-download.png)

- Accept license agreement and click _Next_ to continue installing VS Code.
  ![VS Code installer accept license](../content-images/Sprint%2000/local/vscode-installer-accept-license.png)

- Follow onscreen instructions and accept all default options and continue to the _Ready to Install_ option. Click _Install_ to finish installing VS Code and wait for the installation to complete.
  ![VS Code complete installation](../content-images/Sprint%2000/local/vscode-finish-installation.png)

- Uncheck _Launch Visual Studio Code_ and click _Finish_ to close the installer.

## Install Python

If you haven't already installed Python locally on your computer, follow instructions below to install Python.

- Open a terminal/console window.  You can use the command prompt or powershell (i.e., "cmd.exe").  
- Once inside the terminal, type `python`. 
- This should bring up a window from the Microsoft Store that allows you to install Python:
</br>
  ![Windows Store Python](./images/WindowsStore.png)
- Click the `Get` button and wait for it to finish downloading

If that didn't install Python or bring up the Microsoft Store's Python page, you can also just open the Microsoft Store and search for `Python`. Pick the 3.12 version in the list that shows up.

## Clone To-Do Application Repo
We now need to create a local copy of the To-Do Application repository that we created in an earlier step.

1. From the To-Do Application repository on GitHub, click on the "Code" button and copy the link to the repository
   ![Clone Repo](./images/visual-studio-code-clone-repo-01.png)

2. Open a terminal/console window.  For windows users you can use the command prompt or powershell (i.e., "cmd.exe").  For Mac and Linux users you can use the terminal application.

3. Navigate to the directory where you want to store the project

4. Run the following command to clone the repository:

    ```bash
    git clone <link_to_this_repo>
    ```

5. Navigate to the project directory:

    ```bash
    cd <project directory>
    ```

## Setup Python Virtual Environment

1. From the terminal window, navigate to the project directory

    ```bash
    cd <project directory>
    ```

    > [!TIP]
    > The repository for this training has a directory named `myApplication` that you can use as your default working directory while building the application or feel free to choose any directory where you would like to put this application.

2. Copy the following `requirements.txt` file from [Sprint 0](/Track_1_ToDo_App/Sprint-00%20-%20Environment%20Setup/src/requirements.txt) into your project directory.

3. Open up Visual Studio Code in the project directory by executing the following command.

    ```cmd
    code . 
    ```

4. From Visual Studio Code, either select "View/Command Palette" or press `Ctrl+Shift+P` to open the command palette.
![Command Palette](/Track_1_ToDo_App/Sprint-00%20-%20Environment%20Setup/images/SetupVirtualEnvrionment-01.png)

5. In the search box, type `Python` and then select the option `Python: Create Environement...` from the list of options.
![Create Environment](/Track_1_ToDo_App/Sprint-00%20-%20Environment%20Setup/images/SetupVirtualEnvrionment-02.png)

6. An environment type selection box will appear. Select `Venv Create a '.venv' environment in the current workspace` from the list of options.
![Select Environment Type](/Track_1_ToDo_App/Sprint-00%20-%20Environment%20Setup/images/SetupVirtualEnvrionment-03.png)

7. Select the Python interpreter version to use for the virtual environment.  If you have multiple versions of Python installed, you should select the version that you installed in the previous step.
![Select Python Interpreter](/Track_1_ToDo_App/Sprint-00%20-%20Environment%20Setup/images/SetupVirtualEnvrionment-04.png)

8. Check the box next to the `requirements.txt` file to install the required packages in the virtual environment and hit ok.
![Install Required Packages](/Track_1_ToDo_App/Sprint-00%20-%20Environment%20Setup/images/SetupVirtualEnvrionment-05.png)

9. You will see a notification in the bottom right corner of the screen indicating that the virutal environment is being created.  This can take a few minutes to complete.
![Virtual Environment Creation](/Track_1_ToDo_App/Sprint-00%20-%20Environment%20Setup/images/SetupVirtualEnvrionment-06.png)

10. Once the virtual environment is created, you should see a notification in the bottom right corner of the screen indicating that the virtual environment has been created. 
    This will create a new directory called `.venv` in the project directory that will contain the virtual environment.  All python packages installed in this environment will be isolated from the global python environment.

11. Open up a terminal window in Visual Studio Code and activate the virtual environment by running the following command.

    ```cmd
    .venv\Scripts\Activate
    ```

    You should see the name of the virtual environment in the terminal prompt to indicate that the virtual environment is active.


  
[🔼 Sprint 0 - Home](readme.md) [◀ Previous setup step](01%20-%20Setup%20GitHub%20Account.md) | [Next Sprint ▶](/Track_1_ToDo_App/Sprint-01%20-%20Basic%20Application/README.md)
