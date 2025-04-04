<h1>Wireshark- NMAP</h1>


<h2>Description</h2>
Nmap is an industry-standard tool for mapping networks, identifying live hosts and discovering the services. 

<h2>Questions</h2>

- <b>What is the total number of the "TCP Connect" scans?</b>
- <b>Which scan type is used to scan the TCP port 80?</b>
- <b>How many "UDP close port" messages are there?</b>
- <b>Which UDP port in the 55-70 port range is open?</b>


<h2>Languages and Utilities Used</h2>

- <b>Wireshark</b> 


<h2>Environments Used </h2>

- <b>TryHackMe VM</b> 

<h2>Program walk-through</h2>

<b>Answer the question below <br/>

What is the total number of the "TCP Connect" scans?

<p align="center">
At the top of the Wireshark window, click on Statistics from the menu bar. In the drop-down, click on Resolved Addresses.: <br/>
<img width="1440" alt="Screenshot 2025-03-31 at 1 59 05 PM" src="https://github.com/user-attachments/assets/a80aef1c-2a04-4410-a472-6703ce2a9226" />


<br />
<br />
Resolved Addresses window will pop-up. At the top of this window is a search field labeled Search for entry. Type bbc into this search field.:  <br/>
<img width="1440" alt="Screenshot 2025-03-31 at 2 03 38 PM" src="https://github.com/user-attachments/assets/64c65c1a-ed79-44e1-b640-921ff43b0102" />


<br />
<br />
Answer is 199.232.24.81: <br/>





<h2>Program walk-through</h2>

<b>Answer the question below <br/>
Which scan type is used to scan the TCP port 80?

<p align="center">
Go to the Menu bar and click Statistics. Click on the Conversations option from the drop-down menu: <br/>
<img width="1440" alt="Screenshot 2025-03-31 at 2 13 54 PM" src="https://github.com/user-attachments/assets/400d3db0-5bf5-47e8-a5ac-2f65929ad900" />



<br />
<br />
The Conversations window will pop-up. You can see the different tabs at the top of this window. The tab that pertains to this question is the IPv4 tab. Look at the number on this tab, this is the answer to this question:  <br/>
<img width="1440" alt="Screenshot 2025-03-31 at 2 16 01 PM" src="https://github.com/user-attachments/assets/3c4be1d0-663f-4d14-8779-cf4834af5f10" />



<br />
<br />
Answer is 435: <br/>




<h2>Program walk-through</h2>

<b>Answer the question below <br/>
>How many "UDP close port" messages are there?


<p align="center">
Go to the menu bar and click Statistics. On the drop-down menu click Endpoints: <br/>
<img width="1440" alt="Screenshot 2025-03-31 at 2 20 20 PM" src="https://github.com/user-attachments/assets/521ffbf1-7848-4c1d-a521-da1d84327198" />




<br />
<br />
The Endpoints window will pop-up. Look at the bottom left of the window. Click the checkbox next to Name Resolution:  <br/>
<img width="1440" alt="Screenshot 2025-03-31 at 2 22 04 PM" src="https://github.com/user-attachments/assets/5710b409-c70d-433f-b3c9-169f7c361d2d" />




<br />
<br />
After checking the Name Resolution checkbox, the MAC address will now display the resolved Name. Looking down through the list, you need to find the name Micro-St. Once you find it look across the row till you get to the Bytes column, displaying the amount of Bytes that were transferred from that Name/MAC Address: <br/>
<img width="1440" alt="Screenshot 2025-03-31 at 2 23 22 PM" src="https://github.com/user-attachments/assets/0219dbc9-9043-476d-a6a0-ecdd1bf7da3d" />

<br />
<br />
Answer is 7474: <br/>






<h2>Program walk-through</h2>

<b>Answer the question below <br/>
Which UDP port in the 55-70 port range is open?

<p align="center">
Go to the Endpoints window. Click on the labeled IPv4: <br/>
<img width="1440" alt="Screenshot 2025-03-31 at 2 29 51 PM" src="https://github.com/user-attachments/assets/1da54492-f57a-49e5-8ca4-9fd69e9242b2" />



<br />
<br />
You will now be presented with the IPv4 Endpoints from the pcapng file in the table format. Look for the column labeled City, and click on it to alphabitize them:  <br/>
<img width="1440" alt="Screenshot 2025-03-31 at 2 31 23 PM" src="https://github.com/user-attachments/assets/c1ecf09e-7b05-4aa0-be64-c5e3a6095f82" />


<br />
<br />
Scroll down till you find Kansas City. Once you have found it, count the number of times it appears and you will have your answer.
<img width="1440" alt="Screenshot 2025-03-31 at 2 33 33 PM" src="https://github.com/user-attachments/assets/aab49713-897a-402f-b344-ab17b81982e3" />


<br />
<br />
Answer is 4: <br/>




