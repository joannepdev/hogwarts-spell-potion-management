# MongoDB Installation Instructions

This guide describes the process I followed to install MongoDB on my laptop, following the default installation instructions for Windows.
It may be useful for anyone setting up MongoDB locally for the first time.

## Steps

### 1. Download MongoDB

Download MongoDB Community Server from the official website.

https://www.mongodb.com/try/download/community

For Windows, it is recommended to download the `.msi` installer.

During the default setup, it is optional to install the following components on your machine:

- MongoDB Compass
- MongoDB as a Windows Service

### 2. Run the installer

After the installer has been downloaded, launch the `.msi` file and follow the setup wizard.

**IMPORTANT:** If your computer has more than one drives, it is recommended MongoDB is installed on the C:/ drive (if sufficient space)
to avoid potential configuration issues or troubleshooting.

### 3. Create a directory where MongoDB is going to store data

Open File Explorer and navigate to the drive where MongoDB is installed (for example, `C:/`).

Then, create a folder named `data`.

Inside it, create a subfolder named `db`.

The final path, should look like this:

    C:\data\db

### 4. Add MongoDB to Environment Variables

In order to be able to run MongoDB from every location in the terminal, it is recommended to add the path of the `bin` directory
to a Windows environment variable. (`PATH`)

To add MongoDB to the system PATH, you need to access the Environment Variables settings.

#### Access Environment Variables settings:

1. Press the Win + S keys and search for "Environment Variables"

2. Click on **Edit the system environment variables**

3. In the System Properties window, click **Environment Variables...**

4. Under User variables section on the Environment Variables window, find and select `Path`
    - then, click **Edit**

5. Click **New** and add the MongoDB bin directory path.
    - (e.g `C:\Program Files\MongoDB\Server\<version>\bin`)

6. Click OK to save all changes.

Note: For the changes to take effect, either restart your terminal or make sure it is not running.

### 5. Verify MongoDB installation

After adding the MongoDB bin directory to the PATH, open a new PowerShell or Command Prompt window inside your terminal.

In order to successfully start MongoDB, run inside your terminal the following command:

    mongod

If MongoDB is configured correctly, the server will start and display log messages.

**Note #1:** Make sure the `C:\data\db` directory exists before running the above command.

**Note #2:** If a command is not recognized in either PowerShell or Command Prompt, make sure the terminal has been restarted 
after updating the PATH environment variable.

**Note #3:** In some MongoDB versions, the MongoDB shell (mongosh) is not included by default and may need to be installed separately.