# Getting Started
You are in the right place if your looking to configure *syslog-ng* for remote collection.

## Pre-requisites
* **root** or **sudo** access to instance
* syslog-ng version 3.0 or higher
* `/etc/syslog-ng/syslog-ng.conf` file containing following line `@include "/etc/syslog-ng/conf.d/*.conf"`

## Enabling remote syslog collection
1. Ensure pre-requisites are met
2. Place included `appserver/config/splunk.syslog-ng.conf` in `/etc/syslog-ng/conf.d/`, modifying as needed
3. Restart syslog daemon, follow *Applying changes* section for how-to
4. Test to ensure data is being

## Applying changes
To apply configuration changes, the syslog daemon needs to be restarted by running `service syslog-ng restart`

# Troubleshooting
See README.md

### Checking version
```
root@x /e/syslog-ng# which syslog-ng
/usr/sbin/syslog-ng
root@x /e/syslog-ng#
root@x /e/syslog-ng# syslog-ng --version
syslog-ng 3.5.6
Installer-Version: 3.5.6
Revision:
Compile-Date: Aug 13 2014 13:54:36
Available-Modules: affile,afprog,afsocket-notls,afsocket-tls,afsocket,afstomp,afuser,basicfuncs,confgen,cryptofuncs,csvparser,dbparser,linux-kmsg-format,syslogformat,system-source
Enable-Debug: off
Enable-GProf: off
Enable-Memtrace: off
Enable-IPv6: on
Enable-Spoof-Source: on
Enable-TCP-Wrapper: on
Enable-Linux-Caps: on
Enable-Pcre: on
root@x /e/syslog-ng#
```

# Additional reference
Following documentation are great reference material:
* Admin guide - https://www.balabit.com/sites/default/files/documents/syslog-ng-ose-latest-guides/en/syslog-ng-ose-guide-admin/html/syslog-ng.conf.5.html
