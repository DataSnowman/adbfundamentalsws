# Azure Databricks Fundamentals Workshop (adbfundamentalsws)
Use this repo for the Azure Databricks Fundamentals Workshop

## Step 1 Login to Azure Lab Services 

Here you will to register, start, and login to your Windows 11 desktop that you will use during the workshop.

1. Click on this [Registration Link](https://labs.azure.com/register/nqmlohsoc) for Azure Lab Services 

Refer to the paper you get during the workshop for your userid and password.

you may be using a organization similar to this `@MngEnvMCAP004660.onmicrosoft.com`

Enter your userid and click Next

![labsingin](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/labsingin.png)

Enter your password and click Sign in

![password](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/password.png)

You may be prompted for multifactor auth.  Check with your instructor.

You should endup at a screen that looks like this.

![adbfundamentals](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/adbfundamentals.png)

Click on the stopped toggle on the VM to start your VM

![startingvm](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/startingvm.png)

Once it says that it is Running click on the icon that looks like a monitor

![runningvm](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/runningvm.png)

Keep the download

![keep](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/keep.png)

Open the RDP file and click Connect

![openrdp](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/openrdp.png)

Enter the password provided by your instructor and click OK

![vmok](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/vmok.png)

Click Yes

![yes](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/yes.png)

Your Windows desktop should look like this

![win11desktop](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/win11desktop.png)

Open up the Microsoft Edge browser on the desktop and open up this [GitHub Repo](https://github.com/DataSnowman/adbfundamentalsws) to follow the rest of the directions from that remote desktop

![gitrepo](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/gitrepo.png)

Click on this [link](https://adb-7605877979396497.17.azuredatabricks.net/) to access the Databricks environment for the workshop

When the sign in pops up click Sign in with Azure AD

![signinwithaad](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/signinwithaad.png)

You may be prompted for multifactor auth.  Check with your instructor.

Your Azure Databricks Screen will look like this

![adbscreen](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/adbscreen.png)

In like the new UI so you might want to click the Enable new UI toggle

We will review the items available on the left nav panel

![reviewleftnavitems](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/reviewleftnavitems.png)

For the workshop today we will focus on:

    - Workspace
    - Data
    - Compute
    - SQL Editor
    - SQL Warehouses

## Step 2 Data Engineering

During this section of the workshop we will focus on reviewing and looking at a couple of Databricks Notebooks and using them for Data Engineering

To start this please clone or download a zip of the GitHub Repo we are using in the workshop

![clone](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/clone.png)

Git is installed on the VM so you can open a command prompt and paste in the following:

```
https://github.com/DataSnowman/adbfundamentalsws.git

```

Go into your Workspace in Databricks and navigate to the three dots to the right of your username and select import

![import](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/import.png)

Click on browse and navigate to where you cloned or downloaded the zip of the repo and select the users.dbc file and click open

![usersdbc](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/usersdbc.png)

Click Import

![clickimport](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/clickimport.png)


