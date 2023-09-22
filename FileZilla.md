# Vulnerability Report

## Product Name: FileZilla Client

## Researcher: Abdullah Khawaja

## Vendor Homepage: https://filezilla-project.org/

## Software Download Link: FileZilla Client 3.65.0 for Windows (64-bit) https://download.filezilla-project.org/client/FileZilla_3.65.0_win64_sponsored2-setup.exe 

## Affected Version: 3.65.0

## Vulnerability Type: DLL Hijacking

## Description:

### Vulnerability Details:
A DLL hijacking vulnerability has been identified in FileZilla Client version 3.65.0. Specifically, the file "CLDAPI.dll" is missing from the application's installation directory, which could be exploited by an attacker.

### Exploitation:
An attacker with local access to the victim's system can take advantage of this vulnerability by placing a malicious DLL file with the same name, "CLDAPI.dll," in the "C:\Program Files\FileZilla FTP Client\" directory. When the vulnerable application is launched, it will unknowingly load the malicious DLL instead of the legitimate one.

### Impact:
The successful exploitation of this vulnerability can have severe consequences:

1. **Arbitrary Code Execution:** The attacker can execute arbitrary code on the targeted system with SYSTEM PRIVILEGES. This could lead to the compromise of sensitive data and complete control over the victim's machine.

2. **Persistence:** By replacing the legitimate DLL with a malicious one, the attacker can maintain persistence on the target system, ensuring that their code continues to execute every time the application runs.

## Recommendation:

To mitigate this vulnerability, we recommend the following actions:

1. **Update FileZilla Client:** Users should update their FileZilla Client software to the latest version available, which may include a fix for this vulnerability.

2. **Verify DLL Integrity:** System administrators and users should regularly verify the integrity of DLL files within the application's installation directory to ensure they have not been tampered with.

3. **Restrict File Permissions:** Limit access to the application's installation directory to authorized users only, and apply appropriate file permissions to prevent unauthorized modifications to DLL files.

4. **Monitor for Suspicious Activity:** Implement monitoring and logging solutions to detect any suspicious activity related to DLL loading and execution.

By following these recommendations, users can enhance the security of their systems and protect against potential exploitation of this vulnerability.
