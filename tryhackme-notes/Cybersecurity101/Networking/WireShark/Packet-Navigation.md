# Packet Numbers in Wireshark 

## Introduction 
Wireshark uses unique packet numbers to help analyze and navigate through packet captures. This feature enhances the ability to investigate specific events, making it a valuable tool for network analysis. 

## Key Points 

1. Packet Numbering 

• Each packet analyzed in Wireshark is assigned a unique number. 

• This numbering aids in counting packets and locating specific ones more efficiently. 

2. Navigating Packets 

• Users can navigate through packets using the "Go" menu and toolbar. 

• This feature allows tracking within packet frames and finding the next relevant packet in a conversation. 

3. Finding Packets 

• Users can search for packets based on their content via the "Edit -&gt; Find Packet" menu. 

• The search function accepts four inputs: Display filter, Hex, String, and Regex. Common searches involve String and Regex.

• Searches are case insensitive, but users can adjust case sensitivity if needed. 

• Analysts must know which search field to use among the packet list, packet details, and packet bytes to get accurate results. 

4. Marking Packets 

• Users can mark packets for further investigation using the "Edit" or right-click menu options. 

• Marked packets appear in black to distinguish them from others. 

• Note that marked packets are reset after closing the capture file. 

5. Packet Comments 

• Comments can be added to packets for reminders and insights in future investigations. 

• Unlike marked packets, comments remain in the capture file until manually removed. 

6. Exporting Packets 

• To focus on specific packets, analysts can export selected packets using the "File" menu, streamlining the analysis by reducing unnecessary data. 

7. Exporting Objects (Files) 

• Wireshark can extract and save transferred files from the captured data for further analysis. 

• Exporting objects is available only for specific protocol streams like DICOM, HTTP, IMF, SMB, and TFTP. 

8. Time Display Format 

• By default, Wireshark shows packet times as "Seconds Since Beginning of Capture. " 

• Users can switch to a more common UTC Time Display Format via the "View -&gt; Time 
Display Format" menu. 

9. Expert Info 

• Wireshark identifies protocol states to help spot unusual behavior, offering insights categorized by severity: 

• __Chat (Blue)__: Normal workflow information. 

• __Note (Cyan)__: Events like application errors. 

• __Warn (Yellow)__: Warnings about unusual errors. 

• __Error (Red)__: Issues such as malformed packets. 

• Users can access this expert information via the status bar or "Analyze -&gt; Expert Information" menu. 

## Conclusion 
Wireshark provides powerful features for packet analysis, including numbering, searching, marking, commenting, exporting, and extracting data. Understanding these functionalities allows analysts to conduct thorough investigations and efficiently manage large capture files.

# Try HAck Me Answers

- Q:Search the "r4w" string in packet details. What is the name of artist 1?
- A:r4w8173

- Q:Go to packet 12 and read the comments. What is the answer?
- A:911cd574a42865a956ccde2d04495ebf

- Q:There is a ".txt" file inside the capture file. Find the file and read it; what is the alien's name?
- A:PACKETMASTER

- Q: Look at the expert info section. What is the number of warnings?
- A: 1636