# Speedtest dashboard widget for pfSense
Tested on Community Version community Version 2.6.0 and Pfsense+ 23.01

# Install

## Remove and Old speedtest CLI's
```
# Example how to remove conflicting or old versions using pkg
# pkg info | grep -i speed
# pkg remove speedtest
# pkg remove pkg remove -y py38-speedtest-cli-2.1.3
```

## Install the Official [Speedtest.net CLI](https://www.speedtest.net/apps/cli)
```
pkg update && pkg install -g libidn2 ca_root_nss
```
```
bsdver=$(freebsd-version | cut -d. -f1); [ "$bsdver" -eq 12 -o "$bsdver" -eq 13 ] && echo "Installing for BSD $bsdver"; pkg add "https://install.speedtest.net/app/cli/ookla-speedtest-1.2.0-freebsd$bsdver-x86_64.pkg" || (echo "Installing for BSD $bsdver"; pkg add --force "https://install.speedtest.net/app/cli/ookla-speedtest-1.2.0-freebsd13-x86_64.pkg")
```

## Fetch the Widget File
```
fetch -q -o /usr/local/www/widgets/widgets/speedtest.widget.php https://raw.githubusercontent.com/HoleInTheSeat/pfsense-speedtest-widget/master/speedtest.widget.php
```

Install the widget on your dashboard.
