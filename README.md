# Setting up .dev domains for local development on OSX.

This is needed if you want to use subdomains in your web app. Or if you're an anal retentive type.  

  
This is all from here > http://clintberry.com/2011/wildcard-sub-domains-on-osx-web-development-on-localhost/

1. `sudo -s`
2. `rndc-confgen > /etc/rndc.conf`  
3. `head -n5 /etc/rndc.conf |tail -n4 > /etc/rndc.key`
4. add this file > etc/named.conf
5. add this file > var/named/dev.zone
6. `launchctl load -w /System/Library/LaunchDaemons/org.isc.named.plist`
7. `named -g` then exit (ctrl + c)
8. `named`
9. add the file > etc/resolver/localhost.dev (name this as the url you want)
10. test by navigating to the URL
11. ???
12. profit