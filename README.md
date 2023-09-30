# Network File Shares and Permissions
<p align="center">
<img src="https://i.imgur.com/JNflqQy.png"/>
</p>

<h1>Network File Shares and Permissions</h1>
In this tutorial, going off Active Directory Deployed in Azure [https://github.com/codymar7in/Active-Directory-Configuration-] we will create Network files and share permissions between them. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop Connection
- Active Directory Domain Services
- Server Manager
- Windows Administrative Tools
- Active Directory Users and Computers


<h2>Operating Systems Used </h2>

- Windows 10 (21H2)

<h2>High-Level Steps</h2>

- Log into Cilent-1 and DC-1 VM from [https://github.com/codymar7in/Active-Directory-Configuration-]
- Open DC-1 VM go to Windows Administrative Tools
- Load Active Directory Users and Computers
- Select a random user and log into with Remote Desktop Connection
- Go back to DC-1 VM open File Explorer got to Windows (C) and create the following files (read access, write access, no access, and accounting)
- Go into all the files propeties and allow certain permissions
- Go back to Cilent-1 VM and create a write file txt. file
- Go back to DC-1 VM and create a txt.file to read access for other users to see
- Create a new organzational unit called SECURITY GROUPS
- Create a new group in SECURITY GROUPS called ACCOUNTIANS
- Allow the accounting file to shar persmission with the ACCOUNTIANS
- Add the user in Cilent-1 to ACCOUNTIANS role
- Log into the user with ACCOUNTIANS role


<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/FOId7Va.png"/>
</p>
<p>
First we need to log back into Cilent-1 and DC-1 from [https://github.com/codymar7in/Active-Directory-Configuration-] using Remote Desktop Connection. Copy the Public IP and log into the VM indivudally.  
</p>
<br />

<p>
<img src="https://i.imgur.com/y0GpAJB.png"/>
</p>
<p>
Open DC-1 VM and click the window icon on the bottom left, then click Windows Administrative Tools
</p>
<br />

<p>
<img src="https://i.imgur.com/cme8s3r.png"/>
</p>
<p>
Next click Active Directory Users and Computers
</p>
<br />

<p>
<img src="https://i.imgur.com/anSP9Q6.png"/>
</p>
<p>
Now go to the Employees section and you will see all 2000 Employees created
</p>
<br />

<p>
<img src="https://i.imgur.com/7WFbxml.png"/>
</p>
<p>
Next click a random user and copy the display name on a notepad to not forget the name
</p>
<br />

<p>
<img src="https://i.imgur.com/yIwDoUV.png"/>
</p>
<p>
Now type File Explorer in the search bar and open the app
</p>
<br />

<p>
<img src="https://i.imgur.com/AiwPl0z.png"/>
</p>
<p>
Now click on Windows (C)
</p>
<br />

<p>
<img src="https://i.imgur.com/b7kcSLK.png"/>
</p>
<p>
From here create the following file read access, write access, no access, and accounting. To do this right click anywhere and click create new folder
</p>
<br />

<p>
<img src="https://i.imgur.com/zDCbB5z.png"/>
</p>
<p>
Next right click read access and go to properties
</p>
<br />

<p>
<img src="https://i.imgur.com/yewqg9O.png"/>
</p>
<p>
Go to the Sharing section and click share
</p>
<br />

<p>
<img src="https://i.imgur.com/JHwzRMD.png"/>
</p>
<p>
Next type domain users and click add
</p>
<br />


<p>
<img src="https://i.imgur.com/MUElRGj.png"/>
</p>
<p>
Now click the permissions level and click the read permission. Then click shar on the bottom right 
</p>
<br />

<p>
<img src="https://i.imgur.com/q2m0qkY.png"/>
</p>
<p>
To finish click Done 
</p>
<br />

<p>
<img src="https://i.imgur.com/5g0RC19.png"/>
</p>
<p>
Right click write access and go to the properties section 
</p>
<br />

<p>
<img src="https://i.imgur.com/TwTQEMx.png"/>
</p>
<p>
Next click the Sharing tab, and click share 
</p>
<br />

<p>
<img src="https://i.imgur.com/yUic7Lq.png"/>
</p>
<p>
Under permission level click read/write and then click share
</p>
<br />

<p>
<img src="https://i.imgur.com/VzpIjkS.png"/>
</p>
<p>
To finish click done 
</p>
<br />

<p>
<img src="https://i.imgur.com/OMRJFOw.png"/>
</p>
<p>
Then click close 
</p>
<br />

<p>
<img src="https://i.imgur.com/sm5FKNf.png"/>
</p>
<p>
Right click no access and click properties
</p>
<br />

<p>
<img src="https://i.imgur.com/TwbneX5.png"/>
</p>
<p>
Then click the sharing tab and then click share 
</p>
<br />

<p>
<img src="https://i.imgur.com/sLIeLWW.png"/>
</p>
<p>
Next in the permission level click read/write then click share 
</p>
<br />

<p>
<img src="https://i.imgur.com/wIt3c21.png"/>
</p>
<p>
To finish click Done 
</p>
<br />

<p>
<img src="https://i.imgur.com/w8LtGBE.png"/>
</p>
<p>
Then close the file 
</p>
<br />

<p>
<img src="https://i.imgur.com/wYluNlS.png"/>
</p>
<p>
Next go to Cilent-1 VM and go to Network > dc-1 in file explorer and click read access 
</p>
<br />

<p>
<img src="https://i.imgur.com/F9XhTBe.png"/>
</p>
<p>
Now right click go to new and click text document 
</p>
<br />

<p>
<img src="https://i.imgur.com/669GrN1.png"/>
</p>
<p>
Next you will see that we dont have permission to create the file 
</p>
<br />

<p>
<img src="https://i.imgur.com/EZ5HXsg.png"/>
</p>
<p>
Next go to the write access folder 
</p>
<br />

<p>
<img src="https://i.imgur.com/h1OCe3g.png"/>
</p>
<p>
Next right click and go to new. Then to text document 
</p>
<br />

<p>
<img src="https://i.imgur.com/SaA1fSh.png"/>
</p>
<p>
We can now click the file and call it hi admin. To show the admin 
</p>
<br />

<p>
<img src="https://i.imgur.com/MrRs8Z3.png"/>
</p>
<p>
Now go back to DC-1 VM and go to the read access folder 
</p>
<br />

<p>
<img src="https://i.imgur.com/O4KUuWx.png"/>
</p>
<p>
Now right click and go to new then to text document 
</p>
<br />

<p>
<img src="https://i.imgur.com/yX2Zl6U.png"/>
</p>
<p>
Next name the text file you can only read me 
</p>
<br />

<p>
<img src="https://i.imgur.com/uzjlj2m.png"/>
</p>
<p>
Next open the text file and type hello everyone 
</p>
<br />

<p>
<img src="https://i.imgur.com/aBZRtTc.png"/>
</p>
<p>
Next go back to Cilent 1 VM and you will see the text file in the read access folder
</p>
<br />

<p>
<img src="https://i.imgur.com/mF1KZc6.png"/>
</p>
<p>
Now go back to DC-1 VM and go to mydomain.com then right click. Go to new then to organizational unit 
</p>
<br />

<p>
<img src="https://i.imgur.com/Jj9FlS8.png"/>
</p>
<p>
Now for the name type _SECURITY_GROUPS then click ok 
</p>
<br />

<p>
<img src="https://i.imgur.com/Hc93FD7.png"/>
</p>
<p>
Next go in the _SECURITY_GROUPS and right click go to new then group
</p>
<br />

<p>
<img src="https://i.imgur.com/WzApx9P.png"/>
</p>
<p>
Now name the group ACCOUNTIANTS then click ok 
</p>
<br />

<p>
<img src="https://i.imgur.com/byzUzKY.png"/>
</p>
<p>
Next go to the accounting file and right click then go to the properties section 
</p>
<br />

<p>
<img src="https://i.imgur.com/XVwDap5.png"/>
</p>
<p>
Next go to the sharing tab then click share 
</p>
<br />

<p>
<img src="https://i.imgur.com/2W9VmrF.png"/>
</p>
<p>
Now type accountians then for permission click read/write once thats done click the share button 
</p>
<br />

<p>
<img src="https://i.imgur.com/XjFDVDe.png"/>
</p>
<p>
Now click done 
</p>
<br />

<p>
<img src="https://i.imgur.com/X6sGmFC.png"/>
</p>
<p>
Then to finsih it click close 
</p>
<br />

<p>
<img src="https://i.imgur.com/vm6xS9S.png"/>
</p>
<p>
Next go back to Cilent-1 VM and click the accounting folder and you can see we cant access it 
</p>
<br />

<p>
<img src="https://i.imgur.com/NnO4JlX.png"/>
</p>
<p>
Next go back to DC-1 VM then right click the accountiants name then go to the member tab 
</p>
<br />

<p>
<img src="https://i.imgur.com/Qwvg66s.png"/>
</p>
<p>
Next type the name of the user you are logged into then click ok  
</p>
<br />

<p>
<img src="https://i.imgur.com/ve3LJ8u.png"/>
</p>
<p>
To finish click ok 
</p>
<br />

<p>
<img src="https://i.imgur.com/VrT1UJ8.png"/>
</p>
<p>
Next go back to Cilent 1 VM and click the accounting folder and we can see you cant access it still 
</p>
<br />


<p>
<img src="https://i.imgur.com/cnvt3bg.png"/>
</p>
<p>
Next open up command prompt and type logoff
</p>
<br />

<p>
<img src="https://i.imgur.com/5En4NkI.png"/>
</p>
<p>
Next log back into Cilent 1 VM then click the Win key + R then type \\dc-1 then click ok 
</p>
<br />

<p>
<img src="https://i.imgur.com/pK88JQX.png"/>
</p>
<p>
Then go to the accounting folder and you can see you now have permission to access the folder 
</p>
<br />
