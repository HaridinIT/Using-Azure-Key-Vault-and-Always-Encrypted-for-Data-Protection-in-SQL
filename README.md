
<h1>Using Azure Key Vault and Always Encrypted for Data Protection in SQL</h1>

<h2>Description</h2>
In this project, Azure Key Vault was integrated with an Azure SQL Database to implement Always Encrypted. This involved creating a Key Vault, managing encryption keys, and securing sensitive data at rest and in transit. The project demonstrated methods to enhance data confidentiality and meet compliance standards using Azure's advanced encryption features.
<br />
<p align="center">
<img src="https://imgur.com/mGu7sIE.png" height="85%" width="85%" alt="Securing Azure SQL Database using always encrypted and Azure Key Vault"/>
</p

<h2>Languages and Environments Used (PaaS Components) </h2>


- <b>Azure</b>
- <b>PowerShell</b>
- <b>Azure KeyVault</b>
- <b>JSON</b>
- <b>Azure VM</b>
- <b>Azure SQL Database</b>
- <b>SQL Server</b>
- <b>Azure Defender for SQL</b> 
- <b>Visual Studio 2019</b>
- <b>SQL Server Management Studio<b>

<h2>Project walk-through:</h2>

<p align="center">
Deploy Azure SQL Database and Virtual Machine: <br/>
<img src="https://imgur.com/4IGTrgn.png" height="80%" width="80%" alt="Deploy SQL Database and Virtual Machine"/>

 <p align="center"> 
.json file was downloaded and loaded from \Allfiles\Labs\10\az-500-10_azuredeploy.json

<br />
<br />
Create Key Vault using PowerShell: <br/>
<img src="https://imgur.com/8uldW1P.png" height="80%" width="80%" alt="Created Key Vault using PowerShell"/>
<img src="https://imgur.com/RgLj6dG.png" height="80%" width="80%" alt="Resource Groups"/>
 <img src="https://imgur.com/A5vUVmh.png" height="80%" width="80%" alt="Key Vault"/>
<br />
<br />
Create Access Policy for Key Vault: <br/>
<img src="https://imgur.com/PlWZxn9.png" height="80%" width="80%" alt="Created Access Policy for Key Vault"/>
<br />
<br />
Add Key and Secret to Key Vault using PowerShell: <br/>
<img src="https://imgur.com/2wsvHWG.png" height="80%" width="80%" alt="Adding Keys to Key Vault"/>
<img src="https://imgur.com/pv6BJ4X.png" height="80%" width="80%" alt="Adding Secrets to Key Vault"/>
<br />
<br />

<p align="center">
Enable Application access to Azure SQL Database Service: <br/>
- <b>Create an application and copy its application id</b>
- <b>Add a secret expiring in 12 months in the Add a client secret pane</b>


<br />
<br />
Create a policy granting application access to Key Vault: <br/>
<img src="https://imgur.com/e03WKRc.png" height="80%" width="80%" alt="A policy granting client application access to Key Vault"/>
<br />
<br />
Configure SQL Server Firewall: <br/>
<img src="https://imgur.com/neGrVL8.png" height="80%" width="80%" alt="Configuring SQL server firewall"/>
<img src="https://imgur.com/nS21mYu.png" height="80%" width="80%" alt="Configuring SQL server firewall"/>

<p align="center">
Install and Configure SQL Server Management Studio on Azure VM: <br/>
- <b>Within SQL Server Management Studio, right click the medical database and click New Query</b>

<img src="https://imgur.com/WphGIMq.png" height="80%" width="80%" alt="Creates a table"/>
<br />
<br />
- <b>After the table is created successfully, in the Object Explorer pane, expand the medical database node, th etables node, right click the dbo.Patients node, and click Encrypt Columns. Click Next till Column Selection Page</b>
<br />
<br />
<img src="https://imgur.com/Ujdph7f.png" height="80%" width="80%" alt="Column selection page"/>
<img src="https://imgur.com/EkDiDbY.png" height="80%" width="80%" alt="Master Key Configuration"/>
<br />
<br />
<p align="center">
<img src="https://imgur.com/bJUt0gV.png" height="80%" width="80%" alt="Summary"/>


<p align="center">
Encryption Complete: <br/>

<p align="center">  
<img src="https://imgur.com/g9dqiLi.png" height="80%" width="80%" alt="Encryption Complete"/>

<p align="center">
Run data-driven application to illustrate the integration of Azure Key Vault for encrypting Azure SQL databases. <br/>
<img src="https://imgur.com/Xv1oJIH.png" height="80%" width="80%" alt="New Project"/>
<br />
<br />
Install the first NuGet package <br/>
<img src="https://imgur.com/Pp8V6rx.png" height="80%" width="80%" alt="Installing first NuGet Package"/>
<br />
<br />
Install the second NuGet package <br/>
<img src="https://imgur.com/4HmQ66E.png" height="80%" width="80%" alt="Installing second NuGet Package"/>
<br />
<br />
<img src="https://imgur.com/W7sIgjW.png" height="80%" width="80%" alt="Complete"/>
<br />
<br />

<h2>Verification:</h2>
<p align="center">
Run New Query in SQL Management Console, right click the medical database: <br/>
<img src="https://imgur.com/fjmz3er.png" height="80%" width="80%" alt="Execute New Query"/>
<img src="https://imgur.com/cHl14yZ.png" height="80%" width="80%" alt="Execute New Query"/>


<h2>Conclusion:</h2>
The project showcased the effective integration of Azure Key Vault with Always Encrypted to secure sensitive data in Azure SQL Database. By implementing key management and encryption practices, the project emphasized the importance of safeguarding critical information, ensuring confidentiality, and meeting compliance requirements in cloud-based environments.
