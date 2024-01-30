<h1>Splunk Authentication with LDAP</h1>


<h2>Description</h2>
Managing users and their access to logs ingested in splunk is a very important aspect of access control to avoid unauthorized access to sensitive data/logs. You can add users to splunk by using following three methods. Most commonly used approach is LDAP or commonly called AD authentication. As in any Enterprise,Active Directory is used for user management. We can use existing AD configuration to add and manage/update users in splunk. Below we will see step by step AD authentication configuration in splunk.Authentication methods supported by splunk include: Splunk built-in authentication,LDAP authentication (if enabled) and Scripted authentication (if enabled).
Splunk built-in authentication is the default.

<br />


<h2>Prerequisites for LDAP authentication</h2>

- <b> Active Directory domain is set up</b> 
- <b>Created records in DNS for ldap.forumsys.com</b>
- <b>All Domain Controllers have valid Certificates</b>



<h2>Project walk-through:</h2>



<br />
On the Search Head,click on setting and the authentication.Click the radio button to configure LDAP Authentication:  <br/>
<img src="https://user-images.githubusercontent.com/112047285/206101177-8b3088ed-1fe1-4a9c-850e-294d11e04747.png" height="80%" width="80%"/>
<br />
<br />
Configure a New LDAP Strategy: <br/>
<img src="https://user-images.githubusercontent.com/112047285/206101709-33cd1c38-57ad-4cdb-8c9e-93036d3bf3d4.png" height="80%" width="80%"/>
<br />
<br />
Verify LDAP Strategy details are successfully created and saved:  <br/>
<img src="https://user-images.githubusercontent.com/112047285/206102439-61e2e729-b743-4f2d-92ea-6a0f07ae2b4c.png" height="80%" width="80%"/>
<br />
<br />
Verify LDAP Groups :  <br/>
<img src="https://user-images.githubusercontent.com/112047285/206103812-e5b0c7b1-b8d0-48d6-9d41-9f50b9e5ac8d.png" height="80%" width="80%"/>
<br />
<br />
Map an LDAP Group to a Splunk role: <br/>
<img src="https://user-images.githubusercontent.com/112047285/206103194-e97cc915-da39-428c-8df0-31a44423e4ff.png" height="80%" width="80%"/>
                                                             
<br />
<br />
Verify the Group is mapped to the proper role and active: <br/>
<img src="https://user-images.githubusercontent.com/112047285/206104505-bf32b85b-c10e-4f67-b1cb-6e74cadaae8c.png" height="80%" width="80%"/>
<br />
<br />

Verify the configuration in the authentication.conf configuration file:  <br/>
<img src="https://user-images.githubusercontent.com/112047285/206105100-a9cb5440-4b20-4e66-b2d0-4034e83356e2.png" height="80%" width="80%"/>
<br />

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
