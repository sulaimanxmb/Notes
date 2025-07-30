
after getting all SUB-DOMAINS try for a subdomain takeover using Automated tools like :
1. Subzy       :     `sudo subzy run -targets (domains file)`
2. Nuclei


Use burp suite host or IP range in sitemap by a regix like `.*\.test\.com$

### Technologies :
***Censys*** does good job tracking technologies go [here](https://search.censys.io) 
check shodan too


# Testing :

### Login Bypasses :
for logging in some developers set a **Default OTP** which can be used to bypass otp
So create a new account using email and then use common code like 11111,00000,123456

Put dstny.com to censys and started testing on the first IP came

used : `gobuster dir -u http://185.39.124.194 -w /path/to/wordlist.txt -s "200,301,403" --status-codes-blacklist ""`
Better use feroxbuster ngl

If you see FTP port open then use `lftp ftp://IP` and try running ls orsmtg for connection

when a port is filtered that mostly means protected by firewall

If you get 404 page with IP restriction use `curl -H 'X-FORWARDED-FOR: 127.0.0.1:5000/secret'`