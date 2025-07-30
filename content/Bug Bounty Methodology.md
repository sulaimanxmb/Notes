While using caido if you get a GET or POST request try changing it to TRACE request (It sends your request back from server) to see if the request got modified are not
###  Reconnaissance :
#### Subdomain enumeration :
**Active Subdomain enumeration :** Interacting with target continuously, by brute forcing

There is a command with amass

**Passive Subdomain enumeration :** using public data (Better ngl)


`subfinder -d example.com -all -recursive -t 200 > subfinder.txt` 

`amass enum -d example.com -o amass.txt`

`assetfinder --subs-only example.com > assetfinder.txt`

combine all these to subdomains.txt

`cat subdomains.txt | sudo httpx -sc > alive_domains.txt`

#### Live & Resolving 
(have no idea what this does but check these subdomains)

`dnsx -l subdomains.txt -r resolvers.txt -o dnsx_resolved.txt`

Then Resolve to IP's :
`dnsx -l dnsx_resolved.txt -a -resp-only -o dnsx_resolved_ips.txt`

run nmap for those IP's
`nmap -iL dnsx_resolved_ips.txt -sV -oN nmap_dnsx.txt`

#### Probing :
use this:
`httpx -l subdomains.txt -title -sc -location -p 80,443,8000,8080,8443 -td -cl 
`-probe -o probe_httpx.txt`

**Note : The failed ones which appear are mostly 404 forbidden pages**

`cat httpx.txt | grep -v "FAILED" | awk '{print $1}' | tee probed_only_domains.txt`
This gives only domain names

#### Content Discovery :

`cat probed_domains.txt | feroxbuster --stdin -s 200 --no-recursion -k 
`--random-agent --no-state -r -W 0 -w feroxbuster.txt`  

or do manually

#### Archived URL's (wayback machine) :

`katana -passive -pss waybackarchive,commoncrawl,alienvault -f qurl -u target.com | anew katana_urls.txt`

#### ASN :

`amass intel -asn <ASN_Number> -o asn_targets.txt`

Use censys and shodan here

#### Finding files :

`katana -list probed_domains.txt -jc | grep "\.js"`

