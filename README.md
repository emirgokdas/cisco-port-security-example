# Port Security Example

This repository provides example configurations for setting up Port Security on Cisco switches.

## What is Port Security?

Port Security is a feature that allows you to control access to an individual port on a switch. It helps in preventing unauthorized devices from connecting to the network. You can limit the number of MAC addresses on a port, specify which MAC addresses are allowed, and define actions to take when a violation occurs.

## Configurations

### 1. Basic Port Security

The basic configuration limits the port to one MAC address.

File: `configs/basic_port_security.txt`

```plaintext
interface FastEthernet0/1
 switchport mode access
 switchport port-security
 switchport port-security maximum 1
 switchport port-security violation restrict
 switchport port-security mac-address sticky
