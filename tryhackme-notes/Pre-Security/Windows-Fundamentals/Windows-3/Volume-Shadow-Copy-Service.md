# Summary of Volume Shadow Copy Service (VSS) 

The Volume Shadow Copy Service (VSS) helps create consistent backups, called shadow copies or snapshots, of data. These shadow copies are stored in the System Volume Information folder on drives with system protection enabled. If VSS is active, users can create restore points, perform system restores, configure settings, and delete restore points. However, malware can target these shadow copies, making recovery difficult after a ransomware attack unless offline backups exist. For configuring Shadow Copies in a virtual machine, refer to the relevant instructions. Additionally, for hands-on interaction with VSS, consider exploring Day 23 of Advent of Cyber 2.

__QUESTION__: What is VSS?
__ANSWER__: Volume Shadow Copy Service