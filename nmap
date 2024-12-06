import nmap

def nmap_scan_to_html(target, outfile="nmap_scan.html"):
  """
  Performs an Nmap scan and outputs the results in an HTML file.

  Args:
    target: The target to scan (e.g., '192.168.1.1', '192.168.1.0/24').
    outfile: The name of the output HTML file.

  Returns:
    None
  """

  try:
    scanner = nmap.PortScanner()
    scanner.scan(hosts=target, arguments='-sC -sV')  # Scan for services and versions

    with open(outfile, 'w') as f:
      f.write("<html>\n")
      f.write("<head>\n")
      f.write("<title>Nmap Scan Results</title>\n")
      f.write("</head>\n")
      f.write("<body>\n")
      f.write("<h1>Nmap Scan Results for " + target + "</h1>\n")
      f.write("<pre>\n")
      f.write(scanner.csv())  # Output scan results in CSV format
      f.write("</pre>\n")
      f.write("</body>\n")
      f.write("</html>\n")

    print(f"Nmap scan results saved to {outfile}")

  except Exception as e:
    print(f"An error occurred during the scan: {e}")

if __name__ == "__main__":
  target_ip = "192.168.1.1"  # Replace with your target IP address or network
  nmap_scan_to_html(target_ip)
