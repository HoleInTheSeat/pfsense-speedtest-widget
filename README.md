# Speedtest dashboard widget for pfSense

# Install

## Remove and Old speedtest CLI's
```
# Example how to remove conflicting or old versions using pkg
# pkg remove speedtest
# pkg remove pkg remove -y py38-speedtest-cli-2.1.3
```

## Install the Official [Speedtest.net CLI](https://www.speedtest.net/apps/cli)
```
pkg update && pkg install -g libidn2 ca_root_nss
```
```
freebsd-version && bsdver=$(freebsd-version | cut -c1-2) && if [ "$bsdver" = "13" ]; then echo "Installing for BSD $bsdver"; pkg add "https://install.speedtest.net/app/cli/ookla-speedtest-1.2.0-freebsd13-x86_64.pkg"; fi && if [ "$bsdver" = "12" ]; then echo "Installing for BSD $bsdver"; pkg add "https://install.speedtest.net/app/cli/ookla-speedtest-1.2.0-freebsd12-x86_64.pkg"; fi 
```

## Fetch the Widget File
```
fetch -q -o /usr/local/www/widgets/widgets/speedtest.widget.php https://raw.githubusercontent.com/HoleInTheSeat/pfsense-speedtest-widget/master/speedtest.widget.php
```

Install the widget on your dashboard.
