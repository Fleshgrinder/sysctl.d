# sysctl.d
My personal kernel system variables configuration for web servers.

> Files found under the `/etc/sysctl.d` directory that end with `.conf` are
> parsed within *sysctl(8)* at boot time.  If you want to set kernel variables
> you can either edit `/etc/sysctl.conf` or make a new file.
>
> The filename isn't important, but don't make it a package name as it may clash
> with something the package builder needs later. It must end with `.conf`
> though.
>
> My personal preference would be for local system settings to go into
> `/etc/sysctl.d/local.conf` but as long as you follow the rules for the names
> of the file, anything will work. See *sysctl.conf(8)* man page for details
> of the format.
>
> <footer>— <cite>`/etc/sysctl.d/README.sysctl`</cite></footer>

## Installation
```
sysctl -a > ~/sysctl_defaults.conf
git clone https://github.com/Fleshgrinder/sysctl.d.git
cp sysctl.d/sysctl.conf /etc/sysctl.conf
sysctl -p
```

## References
- Oskar Andreasson: “[Ipsysctl-tutorial](https://www.frozentux.net/documents/ipsysctl-tutorial/)”, 2002.
- ESnet: “[Linux Tuning](http://fasterdata.es.net/host-tuning/linux/)”, September 22th, 2014.
- nixCraft: “[Linux Tune Network Stack (Buffers Size) To Increase Networking Performance](http://www.cyberciti.biz/faq/linux-tcp-tuning/)”, May 20th, 2009.
- nixCraft: “[Linux Kernel /etc/sysctl.conf Security Hardening](http://www.cyberciti.biz/faq/linux-kernel-etcsysctl-conf-security-hardening/)”, October 27th, 2009.
- nixCraft: “[Top 20 Nginx WebServer Best Security Practices](http://www.cyberciti.biz/tips/linux-unix-bsd-nginx-webserver-security.html)”, March 6th, 2010.
- sergioxii: “[Nginx and PHP-FPM for heavy load wordpress web server with high traffic 2000+ concurrent connections](http://itresident.com/nginx/nginx-and-php-fpm-for-heavy-load-wordpress-web-server-with-high-traffic-2000-concurrent-connections/)”, February 26th, 2012.
- The PostgreSQL Global Development Group: “[Managing Kernel Resources](http://www.postgresql.org/docs/devel/static/kernel-resources.html)”, 2014.

## License
[![AGPL-3.0](https://upload.wikimedia.org/wikipedia/commons/thumb/0/06/AGPLv3_Logo.svg/128px-AGPLv3_Logo.svg.png)](https://www.gnu.org/licenses/agpl-3.0.html)
