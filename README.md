# FleetDM notes

## Systemd

You can override `orbit` systemd unit with [orbit.service](orbit.service). 

It will limit allocated resources for `orbit`.

## App armor

[apparmor-config](apparmor-config) is an example of `apparmor` rules to let fleetdm (aka orbit) run with minimal permissions.

If you have `auditd` and `apparmor-notify` installed, you can have desktop notification by running
```
sudo aa-notify -p -f /var/log/audit/audit.log
```
