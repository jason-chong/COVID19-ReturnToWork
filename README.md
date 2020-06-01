# COVID-19 Return To Work solution with Microsoft Healthcare Bot, Azure platform and Teams

***NOTE: Hi! This is my personal repository with contributions from Han Zhang & Greg Beaumont working on _*COVID-19 Back To Work Solution*_ at Microsoft. This is not production-grade code and has not been stress-tested. All instructions, code and templates are subject to review, modification and extensive testing from the individual user***

As countries worldwide seek to re-open their economies by relaxing “stay-at-home” orders, many employers are considering how to prepare their facilities and employees for the return to the physical workplace. To do this in a more safe manner, it is critical to monitor employees for common COVID-19 symptoms and provide a simple way for affected employees to physically return to the workplace once they are cleared to do so. Microsoft teams have developed a special solution template to enable employers worldwide to easily create deploy Microsoft technologies to scale and automate those critical steps for return to the workplace. We call it the “Back to Work” solution Accelerator Kit and below you will find detailed instructions on how to use this to empower a safer return to the workplace for your organization.

The COVID-19 Back to Work solution template is an ACCELERATOR KIT to help you quickly build and deploy a custom solution for your organization. Its highly customizable nature allows the solution to be deployed by organizations across all industries including healthcare workers, retail/manufacturing/frontline workers, students returning to campus, financial institutions. Microsoft’s platform provides the necessary capability by combining Healthcare Bot service with Azure platform as shown below:

![](https://github.com/nikitapitliya006/COVID19-ReturnToWork/blob/master/Screenshots/referenceArchitecture.png)

Choose a UI channel to run this solution. Two options available using this GitHub are - Web Chat and Microsoft Teams (Instructions for using MS Teams are being refined)

## Web Chat Channel 

1. [Configure Healthcare Bot](https://github.com/nikitapitliya006/ReturnToWork/blob/master/WebchatChannel/1-Configure-HealthcareBot.md) host using web chat channel 
2. [Create the backend Azure SQL Database](https://github.com/nikitapitliya006/COVID19-ReturnToWork/blob/master/WebchatChannel/2-Createbackend-AzureSQLDatabase.md)
3. [Configure Data Connection calls to Azure function](https://github.com/nikitapitliya006/COVID19-ReturnToWork/blob/master/WebchatChannel/3-DataConnection-AzureFunction.md) . This Azure function handles write to and read from backend database 
4. Configure Azure function to [Send automated notifications for taking assessment](https://github.com/nikitapitliya006/COVID19-ReturnToWork/blob/master/WebchatChannel/4-SendNotifications-AzureFunction.md) 
5. Create reports and dashboards with [Power BI for real-time visualization](https://github.com/nikitapitliya006/COVID19-ReturnToWork/blob/master/WebchatChannel/5-Visualize-PowerBI.md)

List of Microsoft services required:
* Healthcare Bot
* Azure App Service
* Azure SQL Database
* Azure function apps
* Power BI Pro or Premium


## Microsoft Teams Channel - This is a work in progress
For using Microsoft Teams as a channel, follow steps 1-3 from Web Chat channel config. Then follow these steps:
1. Integrate with [Microsoft Teams](https://github.com/nikitapitliya006/COVID19-ReturnToWork/blob/master/TeamsChannel-WorkInProgress/Integrate-MicrosoftTeams.md)
2. In the left pane of Healthcare bot admin portal, navigate to **Integration > Channels**. Click the activate toggle of the **Microsoft Teams** and Click **Save** to create the channel
3. Click on View and copy the Bot Id from Step 1 above. Search for this ID in your Teams client top Search bar and look for People tab to find a bot with configured bot name and type *_begin covid19_backToWork_sql_*
4. Register App and provide API permissions to allow Teams to interact with Health bot using [RegisterApp-APIpermissions](https://github.com/nikitapitliya006/COVID19-ReturnToWork/blob/master/TeamsChannel-WorkInProgress/RegisterApp-APIpermissions.md)
5. Create reports and dashboards with [Power BI for real-time visualization](https://github.com/nikitapitliya006/COVID19-ReturnToWork/blob/master/TeamsChannel-WorkInProgress/5-Visualize-PowerBI.md)

List of Microsoft services required:
* Healthcare Bot
* Microsoft Teams
* Azure SQL Database
* Azure function App
* Power BI Pro or Premium


## Additional Resources
* Step-by-step instructions on getting started are available [here](https://techcommunity.microsoft.com/t5/healthcare-and-life-sciences/updated-on-5-24-2020-quick-start-setting-up-your-covid-19/ba-p/1230537)
* Step-by-step instructions on using the Healthcare Bot template with Azure API for FHIR are available [here](https://techcommunity.microsoft.com/t5/healthcare-and-life-sciences/using-the-covid-19-back-to-work-template-in-microsoft-healthcare/ba-p/1425833)

More resources to be updated regularly. ARM templates to automate configuration are being worked on and will be available soon