# Cybersecurity-Script

This script was created in 2019 for the annual AFA Cyberpatriot Competition. 

I wanted to automate a lot of the prerequisite setup required for Windows before each competition, so I wrote a short script in Batch and PowerShell that covers most of the areas that we are generally awarded points for, as well as general security requirements. Most of the security requirements are pulled from my own experience, as well as CIS benchmarks and DoD STIGs.

This project taught me how to write scripts using PowerShell and Batch, as well as how to implement security best practices for the Windows OS.

In the future, I hope to implement:
  - application-specific security settings, such as for internet browsers or Filezilla
  - firewall rules and port scanning
  - application updating
  - 

WARNING: Make sure you are in a VM before running these scripts, as they can cause irreversible changes to your system!


How to use:
  1. Download and unzip contents to desktop.
  2. Save the "MasterScript.txt" file as "MasterScript.bat".
  3. Save the "featureuninstaller.txt" file as "featureuninstaller.ps1".
  4. Run the "MasterScript.bat" file as an administrator.
  5. Check to make sure each change made by the script went through.

Features:

- General Security Policies
  - Resets Local Security to default in case of prior tampering.
  - Sets audit policy to log all possible actions.
  - Create GodMode folder to centralize administration.
  - Imports a preconfigured GPO object using the LGPO utility.

- User Account Information
  - Outputs data about user accounts to a text file.
  - Sets passwords for all users to Earth*123456.
  - Disables generic Guest and Administrator accounts.
  - Updates user checkbox information (password expiration, password requirements, etc.).
  - Sets password policies for all users on the machine.

- Firewall
  - Sets firewall to default in case of prior tampering.
  - Turns on firewall for all profiles.

- Windows Services and Features
  - Configures services for maximum security and reduced attack surface.
  - Removes unneeded Windows features.
  - Enables BitLocker.

