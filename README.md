# Active-Directory-Lab


## Objective
Utilize Active Directory and PowerShell to remotely change a user's password, streamlining administrative tasks and ensuring efficient management of user accounts across distributed networks. This objective aims to enhance security and user access control by enabling administrators to execute password changes seamlessly, reducing the need for manual intervention and minimizing potential disruptions to user productivity.


The Detection Lab project aimed to establish a controlled environment for simulating and detecting cyber attacks. The primary focus was to ingest and analyze logs within a Security Information and Event Management (SIEM) system, generating test telemetry to mimic real-world attack scenarios. This hands-on experience was designed to deepen understanding of network security, attack patterns, and defensive strategies.

### Skills Learned

- Implement PowerShell scripts to remotely connect to Active Directory domains and execute password change commands.
- Utilize PowerShell cmdlets such as Set-ADAccountPassword to change user passwords securely and efficiently.
- Ensure proper authentication and authorization mechanisms are in place to authenticate administrators and restrict unauthorized access to password modification capabilities.


### Tools Used

- Active Directory
- RDP
- Powershell
- Linux and Windows



## Steps
![IMG_8628](https://github.com/Cyberz189/Active-Directory-Lab/assets/163569052/19f275eb-d456-4438-a234-dd7dabb07780)
![IMG_8629](https://github.com/Cyberz189/Active-Directory-Lab/assets/163569052/8bd81db9-2a15-407f-8694-a19f97113bc2)
![IMG_8630](https://github.com/Cyberz189/Active-Directory-Lab/assets/163569052/77a8517e-4017-4f68-bb29-7913555ea446)
![IMG_8631](https://github.com/Cyberz189/Active-Directory-Lab/assets/163569052/a48efdb9-8d1b-4102-b347-f04d3318b6fb)


Commence by accessing Active Directory and navigating to the Sales organizational unit (OU). Utilize delegate control to define precise permissions, specifying which features can be managed within that OU. Confirm the user, Phillip, who is to be granted these permissions. In this case, Phillip was granted the ability to reset user passwords and enforce password changes at the next logon.

![IMG_8632](https://github.com/Cyberz189/Active-Directory-Lab/assets/163569052/1be5d255-23f6-483e-8792-ef761be3d1c9)
![IMG_8636](https://github.com/Cyberz189/Active-Directory-Lab/assets/163569052/2fb8f6fe-3e4f-487f-9b10-c7338058defd)


Using RDP, remotely log into User Phillip, who has been granted permissions over the Sales OU. Once logged in, open PowerShell to initiate the process of resetting another user's password. In this case, the targeted user for the password reset is "Sophie." Utilize the following command: Set-ADAccountPassword sophie -Reset -NewPassword (Read-Host -AsSecureString -Prompt 'New Password') -Verbose

This command forces a password reset, allowing "Phillip," who controls password reset permissions on the Sales OU, to set a new password for Sophie. Subsequently, execute the command: Set-ADUser -ChangePasswordAtLogon $true -Identity sophie -Verbose

This command enables user "Sophie" to change her password to her preference during her next logon.

![IMG_8637](https://github.com/Cyberz189/Active-Directory-Lab/assets/163569052/9ec3e744-6eef-4cd2-84e3-e10890eb6eec)

![IMG_8638](https://github.com/Cyberz189/Active-Directory-Lab/assets/163569052/f0c762ca-4853-4975-8f26-10dea599653d)

![IMG_8639](https://github.com/Cyberz189/Active-Directory-Lab/assets/163569052/0cb6410a-eefe-497e-acf5-130dcbf709b9)

Here we can observe the commands working successfully, prompting "Sophie" to change her password immediately upon logging on.


![IMG_8640](https://github.com/Cyberz189/Active-Directory-Lab/assets/163569052/953f4218-a566-407b-896f-32108040b231)

Additionally, we can confirm that logging into "Sophie's" account proceeded smoothly with no issues on either end.

