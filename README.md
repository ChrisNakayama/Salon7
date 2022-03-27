# HairSalon

#### By **Chris Nakayama**

#### Hair HairSalon is a basic website that allows a salon owner to make a list of their stylists which will include information about their clients. This information can be updated or deleted.

## Technologies Used

- C#
- ASP.Net Core
- ASP.NET MVC
- Entity Framework
- MySql Database

## Description

This application allows the user to enter stylist and client information. It also saves those entries in persistent database files.

Database Structure

![Database Structure Image](/HairSalon/wwwroot/images/DatabaseImage.jpg)

## Setup/Installation Requirements

- Download C# and .NET installed on your computer, you can get the Software Development Kit or SDK for Mac here: Dot.Net for Mac and for Windows here: Dot.Net for Windows. Follow the instructions detailed in both links above for set up.
- Install and download: MySql Community
- Install and download: MySql Workbench
- Follow the instruction here for configuring MySql:
- Open the terminal on your local machine and navigate to where you want to clone the project
- Run the following command: git clone https://github.com/ChrisNakayama/Salon7
- Follow these steps to import the table needed for the project:
- Determine if the MySql server is running locally by typing the following into the command line mysql -uroot -p[The password you set up]
- Open MySql Workbench. Once open select the Administration tab. Next select Data Import/Restore. This opens up the Data Import window with the Import from Disk tab open. Select the radio button for Import from Self-Contained File. Click the button with the three dots (if on windows) or two dots (if on mac) at the end of the path field. This will open a window to search for the sql dump file on your local disk. Navigate to the root directory of the cloned project and select brit_wallace.sql and click the open button. Next, press the New... button. This will open a window where you can choose the name of the imported schema. Choose a name appropriate to the project, e.g. Best Client and click Okay. We'll need this name later when setting up the project to work with this schema. If on a mac, click the Start Import button. If on a windows machine, switch to the Import Progress tab on the Data Import page. Click the Import button. Finally, re-click on the Schemas tab. Right-click in the Schemas window, and select Refresh All. The imported schema should now be listed.
  \*Navigate back to the HairSalon/ directory and create a file named: appsettings.json. In this file, add the fowling configuration to set up the project to work with the schema you imported:
  {
  "ConnectionStrings": {
  "DefaultConnection": "Server=localhost;Port=3306;database=[THE-NAME-YOU-CHOSE-WHEN-IMPORTING-THE-SCHEMA];uid=root;pwd=[YOUR-PASSWORD-HERE];"
  }
  }
- In the BestClient main directory run dotnet build on the command line.
- Run dotnet run on the command line to start the web server.

## Known Bugs

None

## Contact Me

Let me know if you run into any issues or have questions, ideas, or concerns:
cnakayam@gmail.com

## License

Copyright (c) March 2022 Chris Nakayama
