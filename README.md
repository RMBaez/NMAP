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
The command needed to find the answer is given during the module explaination. The question is looking for any packet that has a size greater than 1024 bytes. The command will be, tcp.flags.syn == 1 and tcp.flags.ack == 0 and tcp.window_size > 1024. . The numbers to the right of Displayed is the answer: <br/>
<img width="1440" alt="Screenshot 2025-04-04 at 10 23 13 AM" src="https://github.com/user-attachments/assets/c081e3aa-b58a-4a90-ab7a-d8d4ede25e09" />




<br />
<br />
Answer is 1000: <br/>





<h2>Program walk-through</h2>

<b>Answer the question below <br/>
Which scan type is used to scan the TCP port 80?

<p align="center">
Since we want to know that we are looking at port 80 via TCP. Click on the mint green filter bar, and use the filter tcp.port == 80. Looking at the first 4 results we can see that they are all part of the same stream by the connecting bracket. So next we want to move down to the Info section, to figure out what type of scan this could be. Taking a look at the different flags that were used, we see SYN, SYN ACK, ACK, RST ACK. It looks like the process of a Three-way Handshake.: <br/>
<img width="1440" alt="Screenshot 2025-04-04 at 10 35 15 AM" src="https://github.com/user-attachments/assets/88a82ae6-6f08-4f6c-bc79-6c5d2bd95312" />





<br />
<br />
Answer is TCP Connect: <br/>




<h2>Program walk-through</h2>

<b>Answer the question below <br/>
>How many "UDP close port" messages are there?


<p align="center">
The command needed to find the answer is given during the module explaination. The filter is icmp.type == 3 and icmp.code == 3. The numbers to the right of Displayed, is the answer: <br/>
<img width="1440" alt="Screenshot 2025-04-04 at 10 55 20 AM" src="https://github.com/user-attachments/assets/3b407a04-e9cb-4e36-81d6-7d67f1d40dc0" />


<br />
<br />
Answer is 1083: <br/>






<h2>Program walk-through</h2>

<b>Answer the question below <br/>
Which UDP port in the 55-70 port range is open?

<p align="center">
The filter to be used is udp.port in {55..70}. As we can see from the search results, the first UDP attempts met a closed port. But upon the third try, an open port was found.: <br/>
<img width="1440" alt="Screenshot 2025-04-04 at 11 16 50 AM" src="https://github.com/user-attachments/assets/3b057665-c16b-4b45-aad4-79e4bc86fb30" />


<br />
<br />
Answer is 68: <br/>




