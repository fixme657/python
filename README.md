Explanation:

Import the nmap library: This line imports the necessary library for performing Nmap scans.
Define the nmap_scan_to_html function:
Takes the target to scan and the outfile name as arguments.
Creates an nmap.PortScanner() object.
Performs the Nmap scan using scanner.scan(hosts=target, arguments='-sC -sV'):
-sC: Enables script scanning to gather more information about the target.
-sV: Enables service and version detection.
Opens the output HTML file in write mode ('w').
Writes the HTML header, title, and a heading for the scan results.
Writes the scan results in CSV format using scanner.csv().
Writes the closing HTML tags.
Prints a success message.
Includes a try-except block to handle potential errors during the scan.
Call the function:
Sets the target_ip variable to the IP address or network you want to scan.
Calls the nmap_scan_to_html function with the target_ip.
To use this script:

Install the nmap library:
Bash
pip install python-nmap
חשוב להשתמש בקוד בזהירות.

Replace target_ip with the actual IP address or network you want to scan.
Run the script:
Bash
python your_script_name.py
חשוב להשתמש בקוד בזהירות.

This will perform the Nmap scan and save the results in an HTML file named nmap_scan.html (or the name you specified in the outfile argument). You can then open this file in any web browser to view the scan results.

Note:

This script provides a basic example. You can customize it further by:
Adding more Nmap scan options using the arguments parameter.
Modifying the HTML output to include more details or a different layout.
Implementing error handling and logging for better monitoring.
Ensure you have the necessary permissions to perform network scans on your system.
Use this script responsibly and ethically, respecting the privacy and security of others.
