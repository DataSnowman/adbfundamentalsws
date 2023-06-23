# Azure Databricks Fundamentals Workshop (adbfundamentalsws)
Use this repo for the Azure Databricks Fundamentals Workshop

Welcome to the workhop.  The purpose of the workshop is to bring you up to speed on some of the Data Engineering, Data Science, and Data Analysis capabilities of Azure Databricks.  You will be using resources in Azure for this workshop.  Each of you will recieve a userid and password to access the resources.  Please consult your instuctor if you have any questions or blockers.

The Workshop is broken into two parts:

    - Data Engineering and Data Science

    - Data Analysis

Prior to starting the hands-on activites you will need to complete Step 1.

During Step 1 you will log into a VM that is deployed on Azure Labservice.  This will ensure that everyone has the same capabilites by using a standard Window 11 VM that already has the software you need installed.

Sections:

[Step 1 Login to Azure Lab Services](https://github.com/DataSnowman/adbfundamentalsws/tree/main#step-1-login-to-azure-lab-services)

[Step 2 Data Engineering](https://github.com/DataSnowman/adbfundamentalsws/tree/main#step-2-data-engineering)

[Step 3 Data Science Simple Starter](https://github.com/DataSnowman/adbfundamentalsws/tree/main#step-3-data-science-simple-starter)

[Step 4 Data Analysis](https://github.com/DataSnowman/adbfundamentalsws/tree/main#step-4-data-analysis)

[Step 5 Introducing Microsoft Fabric](https://github.com/DataSnowman/adbfundamentalsws/tree/main#step-5-introducing-microsoft-fabric)

## Step 1 Login to Azure Lab Services 

Here you will to register, start, and login to your Windows 11 desktop that you will use during the workshop.

1. Click on this [Registration Link](https://labs.azure.com/register/nqmlohsoc) for Azure Lab Services 

Refer to the paper you get during the workshop for your userid and password.

you may be using a organization similar to this `@MngEnvMCAP004660.onmicrosoft.com`

Enter your userid and click Next

![labsignin](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/labsignin.png)

Enter your password and click Sign in

![password](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/password.png)

`Note: You may be prompted for multifactor auth.  Check with your instructor.`

You should endup at a screen that looks like this.

![adbfundamentals](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/adbfundamentals.png)

Click on the stopped toggle on the VM to start your VM

![startingvm](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/startingvm.png)

Once it says that it is Running click on the icon that looks like a monitor

![runningvm](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/runningvm.png)

Keep the download if you browser prompts you.

![keep](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/keep.png)

Open the RDP file and click Connect

![openrdp](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/openrdp.png)

Enter the password provided by your instructor and click OK

![vmok](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/vmok.png)

Click Yes

![yes](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/yes.png)

Your Windows desktop should look like this.  Notice the following applications that you will use during the workshop:

    - Power BI Desktop
    - Microsoft Azure Storage Explorer
    - Git (to clone this repository to your VM)

![win11desktop](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/win11desktop.png)

Open up the Microsoft Edge browser on the desktop and open up this [GitHub Repo](https://github.com/DataSnowman/adbfundamentalsws) to follow the rest of the directions from that remote desktop VM.  If you prefer to cut and paste it here is the link

```
https://github.com/DataSnowman/adbfundamentalsws
```

![gitrepo](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/gitrepo.png)


## Step 2 Data Engineering

During this section of the workshop we will focus on reviewing and looking at a couple of Databricks Notebooks and using them for Data Engineering activities.

Click on this [link](https://adb-7605877979396497.17.azuredatabricks.net/) to access the Databricks environment for the workshop

When the sign in pops up click Sign in with Azure AD

![signinwithaad](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/signinwithaad.png)

`Note: You may be prompted for multifactor auth.  Check with your instructor.`

Your Azure Databricks Screen will look like this

![adbscreen](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/adbscreen.png)

In like the new UI so you might want to click the `Enable new UI` toggle

We will review the items available on the left nav panel

![reviewleftnavitems](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/reviewleftnavitems.png)

For the workshop today we will focus on:

    - Workspace
    - Data
    - Compute
    - SQL Editor
    - SQL Warehouses
    - Partner Connect

To start this please clone or download a zip of the GitHub Repo we are using in the workshop

![clone](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/clone.png)

Git is installed on the VM so you can open a command prompt and paste in the following:

```
git clone https://github.com/DataSnowman/adbfundamentalsws.git

```

Go into your Workspace in Databricks and navigate to the three dots to the right of your username and select import

![import](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/import.png)

Click on browse and navigate to where you cloned or downloaded the zip of the repo and select the dataengineering.dbc file and click Open

![usersdbc](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/usersdbc.png)

Click Import

![clickimport](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/clickimport.png)

Open the dataengineering folder and you should see these two notebooks

![notobooks](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/notobooks.png)

Open the first notebook `LoadCMSFiles`

![loadcmsfiles](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/loadcmsfiles.png)

In the first cell modify the uncomment (remove the #) last item so it is your username

user = "<yourusername>"

example would be (besure to use your user so you don't colide with another user)

```
user = "usereighteen"
```

![moduser](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/moduser.png)

`IMPORTANT` Let review what is going on in the notebook and please run one cell at a time

Before you run anything you need to attach the notebook to the cluster.  Find the WorkshopNIS cluster and click Attach

![attach](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/attach.png)

When you complete running each cell there should be delta tables in the Data section of the Leftnav

![data](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/data.png)

Open up Microsoft Azure Storage Explorer to check your Storage accounts to find the input source data in Bronze

![bronze](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/bronze.png)

The output of the notebook will be in Silver

![silver](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/silver.png)

`Congrats: You just completed moving source csv files in the bronze container and wrote the data as Delta/Parquet output to the silver container.  You created a Delta table that references those files.` 

Now you are going to take that Delta/Parquet data created in the first notebook and create three Delta tables:

    - Datedim
    - DRGdim
    - MedicareInpatientFact

Open the second notebook `LoadGoldSchema`

![loadgoldschema](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/loadgoldschema.png)

As in the other notebook, in the first cell modify the uncomment (remove the #) last item so it is your username

user = "<yourusername>"

example would be (besure to use your user so you don't colide with another user)

```
user = "usereighteen"
```

`IMPORTANT` Let review what is going on in the notebook and please run one cell at a time

When you complete running the each cell there should be delta tables in the Data section of the Leftnav

![data](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/data.png)

Check your Storage accounts to find the input source data in Silver

![silver](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/silver.png)

The output of the notebook will be in gold folder in the Silver container

![gold](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/gold.png)

`Congrats: You just completed creating the Delta/Parquet output that we will use in the Data Analysis section later in the workshop.`  


Lets now look at the Data Science capabilities in Azure Databricks.


## Step 3 Data Science Simple Starter

Go into your Workspace in Databricks and navigate to the three dots to the right of your username and select import

![import](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/import.png)

Click on browse and navigate to where you cloned or downloaded the zip of the repo and select the `diabetesmlmodel.dbc` file and click Open

![diabetesdbc](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/diabetesdbc.png)

Click Import

![importdiabetes](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/importdiabetes.png)

Open the dataengineering folder and you should see these the new notebook.  You could of also created a new folder in you Databricks workspace call datascience and import the notebook into that folder.

![diabetesnotebook](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/diabetesnotebook.png)

Open the diabetesmlmodel notebook

![loaddiabetes](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/loaddiabetes.png)

In the first cell modify the uncomment (remove the #) last item so it is your username

user = "<yourusername>"

example would be (besure to use your user so you don't colide with another user)

```
user = "usereighteen"
```

![moduser18](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/moduser18.png)

`IMPORTANT` Let review what is going on in the notebook and please run one cell at a time

When you complete running the each cell there should be a delta table in the Data section of the Leftnav called `diabetesageadb<username>` (your username will be concatinated on the end of the table name so you can find your table amongst the other users tables)

`Let's stop hear and take a break before we resume.  The diabetes notebook demonstrated a bunch of ways of accessing the data and the creation of a machine learning model.  This is just a start put be aware that much of the Machine Learning and Deep Learning that creates AI Models like ChatGPT use Python.  You have just run three PySpark notebooks that emerse you in what Data Engineers and Data Scientists work with.` 


## Step 4 Data Analysis

`We are now going to leverage the Delta tables we created in the Data Engineering section.`

Navigate to the SQL Editor in the Left Nav

![sqleditor](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/sqleditor.png)

Run some queries.  Here is a sample query

```
SELECT * FROM cms.datedimuserone1
```

Note that you will need to put your username on the end of SELECT * FROM cms.datedim`<username>`

Try some adhoc queries of your own.  Here is another example to try:

```
select distinct DRG_Cd, DRG_Desc from cms.medicareinpatienthospitals order by DRG_Cd
```

### Access Databricks SQL Warehouse using Power BI

Now lets try to access these delta tables in Power BI desktop

Navigate to Partner Connect in the Left Nav and click on Setup Power BI Desktop

![partnerconnect](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/partnerconnect.png)

Click on Download connection file

![downloadconnectionfile](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/downloadconnectionfile.png)

Click on openfile

![openfile](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/openfile.png)

Make sure you select Azure Active Directory and then click on Sign in and enter your username and password.  Then click Connect

![aadsignin](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/aadsignin.png)

Select your tables and click Load

![loadpbi](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/loadpbi.png)

Create the joins in your model

![joins](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/joins.png)

Start Building a Power BI Report

![pbireport](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/pbireport.png)

`Please ask any questions you have about using Power BI.  Our focus today is Azure Databricks but many Data Analysts and Business users are comfortable using Power BI.  Power BI can access the Delta table you created in all the previous steps.


## Step 5 Introducing Microsoft Fabric

Now we are going to connect to the Delta tables we just created in the workshop by creating a Shortcut to the Delta files in Azure Data Lake Storage Gen2 using Microsoft Fabric.

Login to Microsoft Fabric in your browser on your lab services VM by opening another tab by clicking on the following link [Microsoft Fabric](https://fabric.microsoft.com/).  Here is the link if you need to cut and paste it into the browser

```
https://fabric.microsoft.com/
```

![fabrichome](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/fabrichome.png)

Click on Synapse Data Engineering

![synapsede](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/synapsede.png)

Find your workspace by clicking on Workspaces on the left nav.

![workspaces](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/workspaces.png)

Your workspace should look like this:

![yourws](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/yourws.png)

Your will either be in `NC Databricks Workshop 1-9`

![ncdw1-9](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/ncdw1-9.png)

Or `NC Databricks Workshop 10-18`

![ncdw10-18](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/ncdw10-18.png)

### Create a Lakehouse of your own

Create a Lakehouse by clicking on +New and chosing Lakehouse. Lakehouse (Preview) while still in public preview

![lakehouse](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/lakehouse.png)

As we have been doing all day please name it `user<number>`.  Click Create

An examlpe would be "userone", "Usertwo", etc

![useronelh](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/useronelh.png)

You should now have an empty Lakehouse that looks something like this: 

![yourlh](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/yourlh.png)

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
Shortcut Name: medicareinpatientfact 
URL: /silver/cms/MedicareInpatientHospitalsByProviderAndService/userone/gold/medicareinpatientfact
```
The path for your folder will vary

![scname](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/scname.png)

Click Create

Now create shortcuts for the data and drg tables using the same process.  The Storage URL will be the same as above and each Subpath will just need the last folder name changed.

You now should have the following 3 tables in your Lakehouse:

![goldschema](https://raw.githubusercontent.com/datasnowman/adbfundamentalsws/main/images/goldschema.png)

### Explore the Warehouse SQL Endpoint




