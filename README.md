# Cisco-Static-IP-LAN-Project
Static IPv4 LAN network simulation using Cisco Packet Tracer 9.0.0, Cisco 2911 router, 2960 switch, 2 PCs, and 2 laptops.
This project demonstrates the design and configuration of a **Static IP-based Local Area Network (LAN)** using **Cisco Packet Tracer version 9.0.0**.

The network is designed to provide communication between multiple end devices through a Cisco switch and router. Each end device is configured with a **static IPv4 address**, allowing predictable and controlled network communication.

## Technologies and Components

The project was developed and tested using:

* **Cisco Packet Tracer:** Version 9.0.0
* **Router:** Cisco 2911
* **Switch:** Cisco Catalyst 2960
* **End Devices:** 2 PCs and 2 Laptops
* **Network Type:** Local Area Network (LAN)
* **IP Addressing:** Static IPv4 addressing

## Network Topology

The network consists of the following devices:

```text
                 +----------------+
                 |  Cisco 2911    |
                 |     Router     |
                 +-------+--------+
                         |
                         |
                 +-------+--------+
                 |  Cisco 2960    |
                 |     Switch     |
                 +---+---+---+----+
                     |   |   |   |
                     |   |   |   |
                    PC1 PC2 Laptop1 Laptop2
```

The Cisco 2911 router provides the Layer 3 network interface, while the Cisco 2960 switch connects the four end devices within the LAN.

## Network Components

| Device              | Quantity | Purpose                                            |
| ------------------- | -------: | -------------------------------------------------- |
| Cisco 2911 Router   |        1 | Provides routing and network gateway functionality |
| Cisco 2960 Switch   |        1 | Connects the end devices within the LAN            |
| PC                  |        2 | Network end devices                                |
| Laptop              |        2 | Network end devices                                |
| Cisco Packet Tracer |        1 | Network simulation and configuration environment   |

## IP Addressing

The LAN uses **static IPv4 addressing**. Each PC and laptop is assigned an IP address manually rather than receiving an address automatically through DHCP.


## Configuration

### Router Configuration

The Cisco 2911 router is configured with an IPv4 address on the interface connected to the LAN.

A typical configuration includes:


Each PC and laptop is manually configured with:

* IP address
* Subnet mask
* Default gateway

In Cisco Packet Tracer, this can be configured through:

```text
Desktop → IP Configuration → Static
```

The appropriate values are then entered according to the project's IP addressing scheme.

## Connectivity Testing

After configuring the network, connectivity can be verified using the `ping` command.

For example:

```text
ping <Destination-IP>
```

Successful replies indicate that the source device can communicate with the destination device.

The following tests can be performed:

* PC1 → PC2
* PC1 → Laptop1
* PC1 → Laptop2
* PC2 → Laptop1
* PC2 → Laptop2
* Laptop1 → Laptop2
* End devices → Router gateway

## Verification Commands

The following Cisco IOS commands can be used to verify the network configuration:

### Check Router Interfaces

```text
show ip interface brief
```

This displays the status and IP addressing information of the router interfaces.

### Check Running Configuration

```text
show running-config
```

This displays the current active configuration of the router.

### Test Connectivity

```text
ping <IP-address>
```

This verifies IP connectivity between network devices.

### Check Switch Interfaces

```text
show interfaces status
```

This provides information about the operational status of switch ports.

## Expected Result

After completing the configuration:

* All four end devices should have valid static IPv4 addresses.
* The router interface connected to the LAN should be operational.
* The switch ports connected to the devices should be active.
* Devices on the same LAN should be able to communicate with each other.
* End devices should be able to reach the configured router gateway.
* Successful `ping` responses should confirm network connectivity.

## Advantages of Static IP Addressing

Static IP addressing provides several benefits:

* Predictable IP addresses for network devices
* Easy identification of individual devices
* Useful for small and controlled networks
* No dependency on a DHCP server
* Suitable for devices that require a consistent IP address

## Limitations

Static IP addressing also has some limitations:

* IP addresses must be configured manually.
* Configuration becomes more time-consuming as the network grows.
* Incorrect IP configuration can cause connectivity problems.
* Network administrators must manually maintain the addressing scheme.

## Learning Objectives

This project provides practical experience with:

* Designing a basic LAN topology
* Using Cisco Packet Tracer
* Understanding IPv4 addressing
* Configuring static IP addresses
* Configuring Cisco routers and switches
* Connecting PCs and laptops to a LAN
* Testing network connectivity using `ping`
* Verifying Cisco IOS configurations

## Software Requirements

* **Cisco Packet Tracer 9.0.0**

## Hardware/Network Devices

* 1 × Cisco 2911 Router
* 1 × Cisco 2960 Switch
* 2 × PCs
* 2 × Laptops
* Appropriate Ethernet connections

## Project Files

The main Cisco Packet Tracer project file should be included with this documentation.

Example:

```text
Static-IP-LAN.pkt
README.md
```

## Conclusion

This project successfully demonstrates the implementation of a basic **Static IP LAN** using Cisco Packet Tracer 9.0.0. A Cisco 2911 router and Cisco 2960 switch are used to establish the network infrastructure, while two PCs and two laptops act as end devices.

By manually assigning IPv4 addresses and configuring the appropriate network parameters, the devices can communicate across the LAN. Connectivity testing with `ping` provides a simple method for verifying that the network has been configured correctly.

The project provides a practical foundation for understanding **LAN design, IPv4 addressing, Cisco device configuration, and basic network troubleshooting**.

