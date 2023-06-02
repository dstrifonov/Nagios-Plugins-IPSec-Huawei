# Nagios-Plugins-IPSec-Huawei
Custom-made Nagios Plugin

This is Nagios plugin for checking state of IPSec tunnels on Huawei USG appliance.
It consists of two scripts:
  - The first script is executed bu crontab on every minute. It uses SSH to login with password to extract data from the appliance. Login with SSH key does not have access to IPSec related commends on the appliance.
  - The second script searches in extracted data for peer IP address and Ready flag (RD) and reports to Nagios.
