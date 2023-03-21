# Speedtest dashboard widget for pfSense

## Install

To use this widget you will need to install the speedtest package

```
pkg update && pkg install -g libidn2 ca_root_nss
# Example how to remove conflicting or old versions using pkg
# pkg remove speedtest
# pkg remove pkg remove -y py38-speedtest-cli-2.1.3
# freeBSD 12 install
sudo pkg add "https://install.speedtest.net/app/cli/ookla-speedtest-1.2.0-freebsd12-x86_64.pkg"
# freeBSD 13 install
sudo pkg add "https://install.speedtest.net/app/cli/ookla-speedtest-1.2.0-freebsd13-x86_64.pkg"
fetch -q -o /usr/local/www/widgets/widgets/speedtest.widget.php https://raw.githubusercontent.com/HoleInTheSeat/pfsense-speedtest-widget/master/speedtest.widget.php
```

Install the widget on your dashboard.

