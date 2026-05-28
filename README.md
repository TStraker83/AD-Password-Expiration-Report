Using Powershell to configure an Active Directory Expiring Password Report


<h2>Step 1 — Create an Organizational Unit</h2>

On the Domain Controller PC

Go To: Active Directory Users and Computers (ADUC), create an Organizational Unit (OU) called “EMPLOYEES”

- Start → Windows Administrative Tools → Active Directory Users and Computers

Right Click Your Domain Name Example: strakerlab.com

- New → Organizational Unit → Name: EMPLOYEES
<p><img width="700" height="450" alt="image" src="https://github.com/user-attachments/assets/fb3a8519-4e61-4ac0-ba51-e51e65607698" />
</p>

We currently have no employees in this folder, so we need to populate the EMPLOYEES folder!!
<p><img width="700" height="450" alt="image" src="https://github.com/user-attachments/assets/c3113de2-8470-42bb-9039-9930ea14a406" /></p>


<i><h2>Step 2 — Install an Excel reader (<b>optional</b>)</h2>

If You do not have a program that can read/open Excel formatted documents:

Go to WPS.com to download a free office suite.</i> 


<h2>Step 3 — Populate EMPLOYEES Folder</h2>

Open Powershell ISE as an administrator

- In the taskbar input Powershell ISE

- Right click and select Run as Administrator

In Powershell ISE:

- File → New

- Input: <b>Install-Module ImportExcel -Scope CurrentUser</b> (to install the Excel PowerShell module)

Then:

- Run
<p><img width="700" height="450" alt="image" src="https://github.com/user-attachments/assets/3c2d8d38-b324-4b2f-b67f-7b324b923715" />
</p>

Once that process is complete:

- Copy and paste this script into Powershell

- Run the script 

<p><img width="700" height="450" alt="image" src="https://github.com/user-attachments/assets/54daac52-c181-4bc0-b79f-dc8bde28e87a" />
</p>

Go to:
ADUC and open the "EMPLOYEES" folder to verify it has been populated

<p><img width="700" height="450" alt="image" src="https://github.com/user-attachments/assets/58efc023-a993-41c3-9f63-47a97cc587a9" />
</p>


<h2>Step 4 — Password Report File</h2>

This script has created a file in your C: drive that will give you a report of all the employees and if their password has expired.

- In the taskbar input File Explorer

<p><img width="700" height="450" alt="image" src="https://github.com/user-attachments/assets/ec21d127-9439-43fe-9a85-1c56e4a1e304" />
</p>
Go to:

This PC → Windows C: → PasswordChangeReport

Your Excel program will open with the PasswordChangeReport list
<p><img width="700" height="450" alt="image" src="https://github.com/user-attachments/assets/89f0586c-cafd-4576-9b21-f0fc5e5e591d" />
</p>
