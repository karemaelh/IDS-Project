# Snort Configuration Notes

## Key Settings Changed in snort.conf

### HOME_NET
ipvar HOME_NET 192.168.56.0/24

Set to lab network range to tell Snort what to protect.

### RULE_PATH
var RULE_PATH /etc/snort/rules

Points Snort to the rules directory.

### Interface
Snort runs on: enp0s3

Command used:
sudo snort -A fast -q -c /etc/snort/snort.conf -i enp0s3

## Alert Log Location
/var/log/snort/alert

## Rules File Location
/etc/snort/rules/local.rules
