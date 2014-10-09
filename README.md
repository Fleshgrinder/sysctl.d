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

## License
> This is free and unencumbered software released into the public domain.
>
> For more information, please refer to <http://unlicense.org>
