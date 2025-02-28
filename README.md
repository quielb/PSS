# SafeSearch for Pi-hole
![Pi-hole Logo](https://i0.wp.com/pi-hole.net/wp-content/uploads/2017/06/Vortex-r.png?resize=100%2C100&ssl=1)

# Supported Search Engines
<img src="https://www.festisite.com/static/partylogo/img/logos/google.png" alt="Google Logo" width="225" height="86">
<img src="https://dwglogo.com/wp-content/uploads/2016/01/DuckDuckGo_logo_004.svg" alt="DuckDuckGo Logo" width="275" height="154.75">
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e9/Bing_logo.svg/2000px-Bing_logo.svg.png" alt="Bing Logo" width="200" height="89.2">

# Installation
To install Pi-hole SafeSearch (PSS), simply run the following command in your terminal below. It will set up and install everything for you. 
```
curl -sSL https://raw......
```

# Uninstallation
If you wish to not enforce SafeSearch on your network anymore, please follow the steps below to completely uninstall PSS
1. `pss --disable`
2. PSS creates the following files:
  - `/var/log/pss.log`
  - `/etc/pss.ack`
  - `/tmp/safesearch.txt`
  - `/etc/dnsmasq.d/05-restrict.conf` (Version < 2.0)
  - `/etc/dnsmasq.d/SafeSearch.conf`
3. Version 2.1 will have the --uninstall option
  - User has to type y/n to confirm
  - All files will be deleted, including the script
  
# API Draft
- GET 
  - /ssStatus.php/?/getStatus
  - /ssStatus.php/?/getStatus/{provider}
  - /ssStatus.php/?/getStatistics
  - /ssStatus.php/?/getStatistics/{provider}
- POST
  - /ssStatus.php/?/enable/{provider}&auth={KEY}
  - /ssStatus.php/?/disable/{provider}&auth={KEY}
