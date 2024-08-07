# Java JDK Installation Guide Using Chocolatey

This guide provides step-by-step instructions to install the latest Java JDK on a Windows system using the Chocolatey package manager.

## Step 1: Install Chocolatey
### Open Command Prompt as Administrator

- Press `Win + X` and select **Windows Terminal (Admin)** or **Command Prompt (Admin)**.

### Run the Installation Command

Copy and paste the following command into the Command Prompt, then press `Enter`:

```shell
@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"


Verify Chocolatey Installation
Run the following command to check if Chocolatey is installed successfully:

choco --version

You should see the version number of Chocolatey if it was installed correctly.

Step 2: Install Java JDK Using Chocolatey
Install the Latest Java JDK
In the Command Prompt, run the following command to install the latest version of OpenJDK:

choco install openjdk

This command will download and install the latest version of the OpenJDK.

Set the Environment Variables
Chocolatey should handle setting the JAVA_HOME and PATH variables automatically. However, if it doesn't, follow these steps to set them manually:

Open the Environment Variables Dialog:

Press Win + R, type sysdm.cpl, and press Enter to open the System Properties window.
Click on the Advanced tab, then click on Environment Variables.
Add JAVA_HOME Variable:

Under System variables, click New.
Set Variable name to JAVA_HOME.
Set Variable value to the path of your JDK installation, which by default should be under C:\Program Files\Eclipse Adoptium\jdk-<version>.
Edit the PATH Variable:

In the System variables section, find and select the Path variable, then click Edit.
Click New and add the path to the bin directory of your JDK installation: %JAVA_HOME%\bin.
Step 3: Verify Java Installation
Open a new Command Prompt and run:

java -version

You should see the version information for the newly installed Java JDK.
