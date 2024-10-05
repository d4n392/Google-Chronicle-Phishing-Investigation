# Investigating Phishing Email Using Google Chronicle

## Step 1: Launch Chronicle and Perform Domain Search
Begin by launching Google Chronicle. In the search bar, input the domain signin.office365x24.com and click Search. This query retrieves all events associated with the specified domain, indicating whether any employees have interacted with it. The search results confirm that the domain exists in the ingested data, and you can click on it to delve deeper into its details.

## Step 2: Analyze Domain Information
After clicking on the domain, you will access the domain view. Here, evaluate the VT CONTEXT section for VirusTotal information, the WHOIS data for ownership details, and the Prevalence graph to assess the domain's historical access patterns. Take note of any suspicious indicators, especially if the domain has been flagged by VirusTotal or exhibits low prevalence, which could indicate a greater risk. Additionally, review the Resolved IPs to gather insights about the IP addresses associated with the domain.

## Step 3: Investigate Associated Assets and Events
Click on the TIMELINE tab to examine the events related to the domain, expanding all entries to review detailed HTTP requests, including GET and POST requests. The ASSETS tab will display a list of devices that accessed the domain. Document the names and numbers of these assets in your incident handler's journal, particularly focusing on any POST requests to pages that may indicate a successful phishing attempt, such as a login page.

## Step 4: Examine the Resolved IP Address
Under the Resolved IPs section, click on the IP address 40.100.174.34. This step allows you to investigate whether any other domains are linked to this IP address, revealing potential reuse of infrastructure by attackers. Document any additional POST requests, affected assets, and related domains that could suggest further malicious activity.




![Screenshot 2024-09-07 141820](https://github.com/user-attachments/assets/c3530d5d-c221-4ca0-97ff-a91c2e66f917)

![Screenshot 2024-09-07 141858](https://github.com/user-attachments/assets/367fe13f-1ab4-49e3-b7b7-76f1f36243b6)

![Screenshot 2024-09-07 141905](https://github.com/user-attachments/assets/055e9a62-fc63-4bd9-ad72-f2375ef66ebd)

![Screenshot 2024-09-07 141918](https://github.com/user-attachments/assets/df92203f-276e-45ea-891c-42b740eacccc)

![Screenshot 2024-09-07 142025](https://github.com/user-attachments/assets/c3687c98-74a7-484d-8a61-c5b3926c0385)

![Screenshot 2024-09-07 142056](https://github.com/user-attachments/assets/3c9e7177-2b0e-4015-bfc9-da5f4b3d9aa2)

![Screenshot 2024-09-07 142240](https://github.com/user-attachments/assets/49fc7501-56d8-42d8-ae22-2ff048f99a51)

![Screenshot 2024-09-07 142417](https://github.com/user-attachments/assets/dda2d490-b98a-4d3f-9550-61d13c7d2f07)

![Screenshot 2024-09-07 142426](https://github.com/user-attachments/assets/9e32802a-07d8-4b4c-a271-fde2b16d7700)

![Screenshot 2024-09-07 142501](https://github.com/user-attachments/assets/f30dbf5b-a357-406d-a6e3-464fe348c3ea)

![Screenshot 2024-09-07 142539](https://github.com/user-attachments/assets/ce8daa2e-f138-4283-b77f-0a7709e3dd92)

![Screenshot 2024-09-07 142641](https://github.com/user-attachments/assets/9f5ebc5f-dd04-40b2-83e5-3ada77c6bb52)

![Screenshot 2024-09-07 143359](https://github.com/user-attachments/assets/34760f19-717b-4592-aeb8-e2426c7999bb)

![Screenshot 2024-09-07 143430](https://github.com/user-attachments/assets/9b10a57e-41c7-41bc-addb-4c79d58b0531)

![Screenshot 2024-09-07 143628](https://github.com/user-attachments/assets/7c4a16cc-f300-44a3-8c2c-0b02144a96f4)

![Screenshot 2024-09-07 143727](https://github.com/user-attachments/assets/3aa292f6-6eb7-4f75-8461-e71ad9a1db4b)

![Screenshot 2024-09-07 143848](https://github.com/user-attachments/assets/9c2dd2e7-c563-478a-8634-521e2abd2117)

![Screenshot 2024-09-07 143940](https://github.com/user-attachments/assets/77dd5bf6-ed64-4639-b374-70ff774dfcdd)

Conclusion
This lab reinforced the importance of thorough investigations in identifying and analyzing potential phishing threats. By utilizing Google Chronicle's powerful querying and data analysis capabilities, you successfully uncovered suspicious domain activity and associated risks. The insights gathered will be crucial for enhancing your organization's cybersecurity posture and ensuring a proactive approach to threat management.


