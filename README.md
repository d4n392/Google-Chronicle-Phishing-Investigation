# Investigating Phishing Email Using Google Chronicle

In this Google Chronicle lab, I embarked on a critical investigation into a _phishing_ email alert that raised concerns about a suspicious domain, _signin.office365x24.com_. By leveraging Chronicle’s robust search capabilities, I started with a direct query to uncover any potential interactions employees may have had with this domain. My exploration revealed not only the existence of the domain within the ingested data but also essential insights into its risk profile through detailed analysis of _VirusTotal_ data, _WHOIS_ information, and historical access patterns. The investigation took a pivotal turn as I discovered a _malicious IP address, 40.100.174.34_ associated with the domain. Highlighting the importance of proactive _threat hunting_ in identifying potential vulnerabilities within the organization. 

This lab enhanced my technical skills in using Chronicle, in addition it underscored the critical role that thorough investigations play in protecting against _phishing_ threats and strengthening overall cybersecurity defenses.

## Step 1: Launch Chronicle and Perform Domain Search
I launched Google Chronicle. In the search bar, input the domain signin.office365x24.com and clicked Search. This query retrieves all events associated with the specified domain, indicating whether any employees have interacted with it. The search results confirmed that the domain exists in the ingested data. I clicked on it to delve deeper into its details.

![Screenshot 2024-09-07 141820](https://github.com/user-attachments/assets/c3530d5d-c221-4ca0-97ff-a91c2e66f917)



## Step 2: Analyze Domain Information
After clicking on the domain, I accessed the domain view. Here, I evaluated the VT CONTEXT section for _VirusTotal_ information, the _WHOIS_ data for ownership details, and the Prevalence graph to assess the domain's historical access patterns. I find that 10 security vendors flagged the domain _signin.office365x24.com_ as malicious, and 2 security vendors flagged _login.office365x24.com_ as malicious, both domains having the _phishing_ classification. _Let's dig deeper._

![Screenshot 2024-09-07 141858](https://github.com/user-attachments/assets/367fe13f-1ab4-49e3-b7b7-76f1f36243b6)

![Screenshot 2024-09-07 142539](https://github.com/user-attachments/assets/ce8daa2e-f138-4283-b77f-0a7709e3dd92)

![Screenshot 2024-09-07 142641](https://github.com/user-attachments/assets/9f5ebc5f-dd04-40b2-83e5-3ada77c6bb52)

## Step 3: Investigate Associated Assets and Events
I clicked on the TIMELINE tab to examine the events related to the domain, expanding all entries to review detailed HTTP requests, including GET and POST requests. I then clicked the ASSETS tab to display a list of devices that accessed the domain. 

![Screenshot 2024-09-07 142417](https://github.com/user-attachments/assets/dda2d490-b98a-4d3f-9550-61d13c7d2f07)

![Screenshot 2024-09-07 141918](https://github.com/user-attachments/assets/df92203f-276e-45ea-891c-42b740eacccc)
_My findings show 24 events where this domain was accessed and 6 distinct assets that were affected_

## Step 4: Examine the Resolved IP Address
Under the Resolved IPs section, I clicked on the IP address _40.100.174.34_. This opened an investigation to whether any other domains were linked to this IP address.

![Screenshot 2024-09-07 142025](https://github.com/user-attachments/assets/c3687c98-74a7-484d-8a61-c5b3926c0385)

![Screenshot 2024-09-07 142056](https://github.com/user-attachments/assets/3c9e7177-2b0e-4015-bfc9-da5f4b3d9aa2)

![Screenshot 2024-09-07 142240](https://github.com/user-attachments/assets/49fc7501-56d8-42d8-ae22-2ff048f99a51)

![Screenshot 2024-09-07 143430](https://github.com/user-attachments/assets/9b10a57e-41c7-41bc-addb-4c79d58b0531)

![Screenshot 2024-09-07 143848](https://github.com/user-attachments/assets/9c2dd2e7-c563-478a-8634-521e2abd2117)

![Screenshot 2024-09-07 143940](https://github.com/user-attachments/assets/77dd5bf6-ed64-4639-b374-70ff774dfcdd)

There were two Indicator's of Compromise with a High Priority Intelligence Requirement, one of which was a brute force script ran from opening the link on the phishing email, using _POST /login.php_ HTTP requests. The two distinct domains associated with the IP _40.100.174.34_
are _signin.accounts-gooqle.com_ and _signin.office365x24.com_. ESET Threat Intelligence suggested blocking this IP with _High_ confidence and _High_ severity. 

## Conclusion
This Google Chronicle lab provided valuable insights into the investigation of _phishing_ emails, emphasizing the importance of proactive _threat hunting_. I learned how to effectively utilize Chronicle’s search capabilities to track down a suspicious domain, analyze its risk profile through _VirusTotal_ and _WHOIS_ data, and assess its prevalence in the system. The discovery of a malicious IP address linked to the _phishing_ attempt underscored the critical nature of thorough investigations in identifying potential _vulnerabilities_. Overall, this exercise enhanced my technical skills in cybersecurity while reinforcing the need for vigilance and comprehensive analysis in protecting organizational assets from _phishing_ threats.

