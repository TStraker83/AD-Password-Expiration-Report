# Automated-Daily-Expired-Password-Scraper
Using Powershell to configure an Active Directory Expiring Password Report

<h2>Step 1 — Create an Organizational Unit</h2>

On the Domain Controller PC

Go To: Active Directory Users and Computers (ADUC), create an Organizational Unit (OU) called “EMPLOYEES”

- Start → Windows Administrative Tools → Active Directory Users and Computers

Right Click Your Domain Name Example: strakerlab.com

- New → Organizational Unit → Name → EMPLOYEES

We currently have no employees in this folder, so we need to populate the EMPLOYEES folder!!


<i><h2>Step 2 — Install an Excel reader (<b>optional</b>)</h2>

If You do not have a program that can read/open Excel formatted documents:

Go to WPS.com to download a free office suite.</i> 


<h2>Step 3 — Populate EMPLOYEES Folder</h2>

Open Powershell ISE as an administrator

- In the taskbar input Powershell ISE

- Right click and select Run as Administrator

In Powershell ISE:

- File → New

- Input: Install-Module ImportExcel -Scope CurrentUser (to install the Excel PowerShell module)

Then:

- Run

Once that process is complete:

- Copy and paste this script into Powershell

- Run the script 

Go to:
ADUC and open the "EMPLOYEES" folder to verify it has been populated

<h2>Step 4 — Password Report File</h2>

This script has created a file in your C: drive that will give you a report of all the employees and if their password has expired.

- In the taskbar input File Explorer

Go to:

This PC → Windows C: → PasswordChangeReport

Your Excel program will open with the PasswordChangeReport list

