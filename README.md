# FleetDM notes

An example of `apparmor` rules to let fleetdm (aka orbit) run with minimal permissions.

If you have `auditd` and `apparmor-notify` installed, you can have desktop notification by running
```
sudo aa-notify -p -f /var/log/audit/audit.log
```
