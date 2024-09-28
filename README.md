<h1>Updating Files Using A Python Algorithm</h1>

<h2>Description</h2>
Access to restricted content is controlled with an allow list of IP addresses, "allow_list.txt" identifies these IP addresses. A separate remove list identifies IP addresses that should no longer have access to this content. I created an algorithm to automate updating the "allow_list.txt" file and remove these IP addresses that should no longer have access. 


<h2>Languages and Utilities Used</h2>

- <b>Python</b> 

<h2>Environments Used </h2>

- <b>Windows 10 Pro </b>

<h2>Lab walk-through:</h2>

<p align="center">
Opening "allow_list.txt": <br/>
<img src="https://i.imgur.com/J1z09It.png" height="80%" width="80%" alt="Opening "allow_list.txt""/>
<br />
<br />
Reading the File Contents:  <br/>
<img src="https://i.imgur.com/sGCbE8m.png" height="80%" width="80%" alt="Reading the File Contents"/>
<br />
<br />
Converting the String to a List: <br/>
<img src="https://i.imgur.com/Rc8e9d4.png" height="80%" width="80%" alt="Converting the String to a List"/>
<br />
<br />
Iterating Through the Remove List:  <br/>
<img src="https://i.imgur.com/UZ0zfLS.png" height="80%" width="80%" alt="Iterating Through the Remove List"/>
<br />
<br />
Removing the IP Addresses That Are on the Remove List:  <br/>
<img src="https://i.imgur.com/l1lyzUT.png" height="80%" width="80%" alt="Removing the IP Addresses That Are on the Remove List"/>
<br />
<br />
Updating the File with the Revised List of OP Addresses:  <br/>
<img src="https://i.imgur.com/SXcExjF.png" height="80%" width="80%" alt="Updating the File with the Revised List of OP Addresses"/>
<br />
<br />

I wanted to write the updated allow list as a string to the file "allow_list.txt". This way, the restricted content will no longer be accessible to any IP addresses that were removed from the allow list. To rewrite the file, I appended the ".write()" function to the file "object file" that I identified in the "with" statement. I passed in the ip_addresses variable as the argument to specify that the contents of the file specified in the with statement should be replaced with the data in this variable.
<br />
<h2>Summary</h2>
I created an algorithm that removes IP addresses identified in a "remove_list" variable from the "allow_list.txt" file of approved IP addresses. This algorithm involved opening the file, converting it to a string to be read, and then converting this string to a list stored in the variable ip_addresses. I then iterated through the IP addresses in remove_list. With each iteration, I evaluated if each element was part of the ip_addresses list. If it was, I applied the ".remove()" method to it to remove the element from ip_addresses. After this, I used the ".join()" method to convert the ip_addresses back into a string so that I could write over the contents of the "allow_list.txt" file with the revised list of IP addresses.

