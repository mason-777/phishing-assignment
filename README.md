# phishing-assignment
Using a real life example email i recieved a few days back which has phishing characteristics.
Recieved a mail from Barnhill Contracting Company <career@barnhillscontracting.com> Using Zoho Mail offering me a job in the US.
Findings- 
1.The email address i recieved the mail from does not match the original domain of the site .i.e. (barnhillbuilt.com)
2.Checked the email header using an online tool mxtoolbox where the result points that the sender of the email is using zoho mail which is blacklisted and the ip address is 136.143.171.50
3.No SPF or DMARC Records found.
4.Company offering a dream salary of around 11000$ without any interview.
5.The mail consists of a pdf attachment( possible payload).
6.Used kali linux to scan for sub domains(barnhillscontracting.com) using amass
7.Ran a command amass enum -d barnhillbuilt.com, did not find any subdomain by the name barnhillscontracting.com
8.Used the nslookup command( nslookup barnhillscontracting.com), no such domain exists.
SUMMARY-A phishing email posing as a job offer from Barnhill Contracting Company was received from a fake address using the non-existent domain barnhillscontracting.com. Analysis showed the email was sent via a blacklisted Zoho Mail server with no SPF or DMARC records. The offer promised an unusually high salary without an interview and included a suspicious PDF attachment. DNS checks and subdomain scans confirmed the domain is not linked to the legitimate company, exposing it as a clear phishing attempt.
