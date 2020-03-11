# CVE-2020-0796
NSE script to potentially detect vulnerable CVE-2020-0796 issue, with Microsoft SMBv3 Compression (aka coronablue)

The script is a modified version of smb-protocols.nse script with a modified output data for v3.11 detection. 
Note: This script just safe checks for SMBv3.11 version and doesn't attempt anything beyond that. The script doesn't currently check for Compression to confirm the vulnerability. 

Copy the .nse file to nmap/scripts/ folder and run update

``cp cve-2020-0796.nse /usr/share/nmap/scripts/``
``nmap --script-updatedb``

Run as 

``nmap -p445 --script cve-2020-0796 <<target>>``
