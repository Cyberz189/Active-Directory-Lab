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


Begin by accessing Active Directory and navigating to the Sales organizational unit (OU). Then, utilize delegate control to set specific permissions, dictating which features can be controlled within that OU. Finally, verify and confirm the user who is to be granted these permissions.

![IMG_8632](https://github.com/Cyberz189/Active-Directory-Lab/assets/163569052/1be5d255-23f6-483e-8792-ef761be3d1c9)
![IMG_8636](https://github.com/Cyberz189/Active-Directory-Lab/assets/163569052/2fb8f6fe-3e4f-487f-9b10-c7338058defd)

By using RDP to remotely log into User Phillip who was granted permissions over the Sales Ou, and then opening powershell to begin the process of changing a another users password. The targeted user whos getting their password reset is "sophie" 



Every screenshot should have some text explaining what the screenshot is about.

Example below.

*Ref 1: Network Diagram*
