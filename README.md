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
    - Partner Connect

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

Open the users file and you should see these two notebooks

![notobooks](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/notobooks.png)

Open the first notebook LoadCMSFiles

![loadcmsfiles](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/loadcmsfiles.png)

In the first cell modify the uncomment (remove the #) last item so it is your username

user = "<yourusername>"

example would be usereighteen

![moduser](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/moduser.png)

`IMPORTANT` Let review what is going on in the notebook and please run one cell at a time

Before you run anything you need to attach the notebook to the cluster.  Find the WorkshopNIS cluster and click Attach

![attach](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/attach.png)

When you complete running the each cell there should be delta tables in the Data section of the Leftnav

![data](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/data.png)

Check your Storage accounts to find the input source data in Bronze

![bronze](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/bronze.png)

The output of the notebook will be in Silver

![silver](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/silver.png)

Open the second notebook LoadGoldSchema

![loadgoldschema](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/loadgoldschema.png)

As in the other notebook, in the first cell modify the uncomment (remove the #) last item so it is your username

user = "<yourusername>"

example would be usereighteen

`IMPORTANT` Let review what is going on in the notebook and please run one cell at a time

When you complete running the each cell there should be delta tables in the Data section of the Leftnav

![data](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/data.png)

Check your Storage accounts to find the input source data in Silver

![silver](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/silver.png)

The output of the notebook will be in gold folder in the Silver container

![gold](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/gold.png)

## Step 3 Data Analysis

Navigate to the SQL Editor in the Left Nav

![sqleditor](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/sqleditor.png)

Run some queries.  Here is a sample query

```
SELECT * FROM cms.datedimuserone1
```

Now lets try to access these delta tables in Power BI desktop

Navigate to Partner Connect in the Left Nav
and click on Setup Power BI Desktop

![partnerconnect](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/partnerconnect.png)

Click on Download connection file

![downloadconnectionfile](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/downloadconnectionfile.png)

Click on openfile

![openfile](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/openfile.png)

Click on Sign in and enter your username and password.  Then click Connect

![aadsignin](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/aadsignin.png)

Select your tables and click Load

![loadpbi](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/loadpbi.png)

Create the joins in your model

![joins](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/joins.png)

Start Building a Power BI Report

![pbireport](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/pbireport.png)

## Step 4 Introducing Microsoft Fabric

Now we are going to connect to the Delta tables we just created in the workshop by creating a Shortcut to the Delta files in Azure Data Lake Storage Gen2 using Microsoft Fabric.

Login to Microsoft Fabric in you browser on your lab services VM by opening another tab by clicking on the following link [Microsoft Fabric](https://fabric.microsoft.com/).  Here is the link if you need to cut and paste it into the browser

```
https://fabric.microsoft.com/
```

![fabrichome](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/fabrichome.png)

Click on Synapse Data Engineering

![synapsede](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/synapsede.png)

Create a workspace if one is not already created.  Click on Workspaces on the left nav.

![workspaces](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/workspaces.png)

Click on +New workspace which opens a dialog. 

![newws](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/newws.png)

I called mine workshop

![workspace](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/workspace.png)

Create a Lakehouse by clicking on +New and chosing Lakehouse. Lakehouse (Preview) while still in public preview

![lakehouse](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/lakehouse.png)

I called mine `medicare`.  Click Create

![medicare](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/medicare.png)

Click on New shortcut

![newsc](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/newsc.png)

Click on Azure Data Lake Storage Gen2

![adls](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/adls.png)

Now you need to create a connection string

![constring](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/constring.png)

Go back to Azure Storage Explorer and find your gold schema

![goldtables](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/goldtables.png)

Right click on a folder and scroll down to properties and select properties

![props](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/props.png)

Select the DFS URL

![dfs](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/dfs.png)

It should look something like this:

```
https://fabaccelerla3wfpqdmcv7c.dfs.core.windows.net/silver/cms/MedicareInpatientHospitalsByProviderAndService/userone1/gold/medicareinpatientfact
```
For the URL enter just the storage account

```
https://fabaccelerla3wfpqdmcv7c.dfs.core.windows.net
```
Then click Next

![url](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/url.png)

In the Shortcut setting enter the Shortcut name (the name of the folder which represents the delta table for example) and the Subpath.  Something like this:

```
/silver/cms/MedicareInpatientHospitalsByProviderAndService/userone1/gold/medicareinpatientfact
```
The path for your folder will vary

![scname](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/scname.png)

Click Create

Now create shortcuts for the data and drg tables using the same process.  The Storage URL will be the same as above and the Subpath will just need the last folder name changed.

You now should have the following 3 tables in your Lakehouse:

![goldschema](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/goldschema.png)

