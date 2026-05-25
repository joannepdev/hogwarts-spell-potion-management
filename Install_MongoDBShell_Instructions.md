## MongoDB Shell Installation Instructions

This guide describes the process I followed to install MongoDB Shell on my laptop, following the default installation instructions for Windows.
It may be useful for anyone setting up MongoDB (and its utilities) locally for the first time.

## Steps

### 1. Download MongoDB Shell

Download MongoDB Community Shell from the official website.

https://www.mongodb.com/try/download/community

You will be redirected to the Community Server download page.

From there:
- on the left-hand panel, select "Tools"
- scroll down to the MongoDB Shell section

For Windows, it is recommended to download the `.zip` installer for the latest available version (ie. 2.8.3).

## 2. Extract the .zip file

Locate the downloaded `.zip` file (usually in Downloads folder).

Right-click on it and select `Extract All`. If using WinRAR (or related programs), select `Extract All` from the context menu.

Extract the file into a temporary folder (may be Downloads folder) or directly into the MongoDB installation directory.

## 3. Place MongoDB Shell files into the `bin` directory

After extracting the `.zip` file, navigate to the folder:

    mongosh-2.8.1-win32-x64

Inside the `bin` subdirectory, locate the required files.

Then:

- copy mongosh.exe
- copy mongosh_crypt_v1.dll

and paste them into the MongoDB Server bin directory. For example:

    C:\Program Files\MongoDB\Server\8.2\bin

The `mongosh-2.8.1-win32-x64` folder and its contents have been moved into the MongoDB `bin` directory
(as shown above).

## 4. (Optional, but recommended) Add MongoDB Shell to PATH

In order to be able to run MongoDB Shell from every location in the terminal, it is recommended to add the path of the MongoDB `bin` directory
to a Windows environment variable. (`PATH`)

To add MongoDB to the system PATH, you need to access the Environment Variables settings.

Then, you can run from any location:

    mongosh

**Note:** Make sure both MongoDB and the MongoDB Shell (mongosh) have been added to the system PATH.

## 5. Verify MongoDB Shell installation

Open a new PowerShell or Command Prompt window inside your terminal. Then run:

    mongosh

If successful, you should enter the MongoDB shell interface.