# What is Integrity? 

Integrity refers to the ability to ensure that data remains unchanged. It is crucial in cybersecurity because we want to keep important data safe from unwanted changes. For example, when you download an application, you need to know that it has not been altered during the download process. 

To verify this, a hash is often provided with the file. A hash is a number generated using an algorithm applied to the data, which helps confirm that the file is intact. Common hashing algorithms include MD5, SHA1, and SHA256. 

For instance, when downloading WinSCP, you can find the hashes published alongside the files on their Sourceforge repository. After downloading the WinSCP-5. 21. 5-Setup. exe file, you can check its integrity by recalculating the hashes using specific commands, such as `md5sum`, `sha1sum`, and `sha256sum`. If the recalculated hashes match those published online, you can confirm that the file is unchanged. 

## Software and Data Integrity Failures 

This vulnerability happens when software or data is used without integrity checks, allowing an attacker to modify them, which can lead to unexpected issues. There are two main types of vulnerabilities here: 

• Software Integrity Failures 

• Data Integrity Failures