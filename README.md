# node-service

A systemd service file for node.js applications.

## Purpose

The goal is to have a node project be a proper system service, starting at
boot and restarting upon failure.

## Installation

```
git clone https://github.com/rwestlund/node-service
vim node-service/node.service
cp node-service/node.service /etc/systemd/system/
systemctl enable node
```

`NEW_USER` and `NEW_GROUP` may be used to drop node's root privileges after
binding to ports.

## Notes

If you do not use postgres, then remove the postgresql dependency from the
file.
