# CVE-2020-0796
NSE script to detect vulnerable CVE-2020-0796 issue, with Microsoft SMBv3 Compression (aka coronablue, SMBGhost)

The script is a modified version of smb-protocols.nse script with a modified output data for v3.11 detection and validating CVE-2020-0796. 

Note: This script just safe checks for CVE-2020-0796 vulnerability on SMBv3 and doesn't attempt anything beyond that.
Checks for compression based on https://github.com/ollypwn/SMBGhost/
Copy the .nse file to nmap/scripts/ folder and run update

``cp cve-2020-0796.nse /usr/share/nmap/scripts/``
``nmap --script-updatedb``

Run as 

``nmap -p445 --script cve-2020-0796 <<target>>``
