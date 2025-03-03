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

## Queries

Some examples of `osquery` queries. 

You need an admin access to FleetDM manager to run them.

```
SELECT * FROM usb_devices WHERE removable = 1;
SELECT * FROM processes;
SELECT * FROM file where path like "/etc/ssh/%";
SELECT * FROM process_open_files;
SELECT * FROM process_open_sockets;
SELECT * FROM mounts;
```

## Todo

### File Carving

Explore file carving : https://osquery.readthedocs.io/en/latest/deployment/file-carving/

An example of implementation here : https://zercurity.medium.com/file-retrieval-with-osquery-using-carves-on-zercurity-9b157f7c0801
