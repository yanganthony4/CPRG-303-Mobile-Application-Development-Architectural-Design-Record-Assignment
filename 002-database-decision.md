Database Storage 

Status: Accepted 

Context:  

The app is designed to allow users to track their spending. Since this data is sensitive and related to personal financial information, secure storage and access are crucial. to accommodate 
both local storage and cloud access the app will store data locally on the user's device while also synchronizing with a remote MySQL database. this dual-storage approach allows for offline access 
while enabling data continuity across devices when connected to the internet. 

Decision:  

The chosen database solution is a combination of local encrypted storage on the device and a remote MySQL database. Locally, data will be encrypted to protect user privacy even without an internet 
connection. When internet access is available, the app will synchronize with the MySQL database, providing users with access to their spending history across devices. Data transmission and  
storage will be protected with encryption, secure API endpoints, and user authentication protocols. 

Consequences: 

* Enhanced Security - Encrypting data locally and in the MySQL, database ensures that sensitive financial information is protected both in transit and at rest. 
  Secure API endpoints and user authentication add additional layers of protection, limiting access to authorized actions only. 

* Cross-Device Access - Storing Data in remote MySQL database allows users to view their appending history from 
  any device with an internet connection, making it easier to access and manage financial data on the go. 

* Reliability and Data Integrity - MySQL's reliability makes it a strong choice for handling user data with minimal risk of data loss 
  or corruption. This also aligns well with potential app expansions that may require robust data management. 

* Offline Accessibility - Local storage enables users to access their spending data without requiring an internet connection, improving the app's usability in areas with limited connectivity 

* Development Complexity - Using both local storage and a remote MySQL database adds complexity to the data management layer. 
  However, the benefits of secure cross-platform data accessibility justify this setup 

* Scalability for Future Expansions - As the app grows, MySQL's scalability and community support allow for the easy the easy addition 
  of new features, such as analytics and spending recommendations, supporting long-term flexibility and adaptability. 
