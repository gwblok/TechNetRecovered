#SCCM-Export TS to Excel
[Wayback Machine Link](http://web.archive.org/web/20200318074701/https://gallery.technet.microsoft.com/SCCM-Export-TS-vers-Excel-69b65e4c)

Author: [Gregory_B](https://techcommunity.microsoft.com/t5/user/viewprofilepage/user-id/11967) [Twitter](https://twitter.com/gbouchu)

Both PowerShell scripts in the archive allow you to export your SCCM task squence to Excel. The first one is run through the command line (CMTSExportToExcel -Siteserver "YOURSITESERVER" -Sitecode "YOURSITECODE" -TSName "TASKSEQUENCENAME

Both PowerShell scripts in the archive allow you to export your SCCM task squence to Excel.

The first one is run through the command line (CMTSExportToExcel -Siteserver "YOURSITESERVER" -Sitecode "YOURSITECODE" -TSName "TASKSEQUENCENAME")

The second one is launching a GUI where you can retrieve all your TS before exporting.

The export creates the following columns:

- ID

- Name

- Type (Group or Step, Groups are in bold)

- Description

- Condition (Yes / No, Yes is yellow)

- Continue on error (Yes / No, Yes is yellow)

- Enabled (Yes / No, No is yellow)

- Variables

 

- Variables



 

<#  .SYNOPSIS

      Document the selected SCCM task sequence in Excel

  .DESCRIPTION

      Collections created:

        The Excel sheet will give you seven columns:

        - Id of the task

        - Name of the task

        - Type of the task (Step or group). The name and type are bold if group

        - The description

       - If there is condition on the task (Yes or No)

        - If Continue on error is checked (Yes or No)

        - The variables assigned to the step (For now issue with the formatting of the variables)

     .PARAMETER

SiteServer   Your site server name. Mandatory

SiteCode    Your site code. Mandatory
TSName    The name of the TS you want to export. Mandatory

 .NOTES

      Author : Gregory Bouchu

     Website: http://microsoft-desktop.com/

     Twitter: @gbouchu


 .VERSION

    1.0: Public


 .EXAMPLE

      CMTSExportToExcel -Siteserver SCCM01 -Sitecode LAB -TSName Deployment_windows10
  #>
