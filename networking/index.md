---
layout: base
title: Starbound Networking
---

# Starbound Networking

The Starbound networking protocol is based on TCP. The current protocol version is 1234.

## Resources

There are several related pages that you might want to browse:

* <span class="text-danger">Establishing a connection</span>

## Data Types

<!--
    This section describes terminology that will see use for all packets below. If a new data
    type is introduced, then document it here.
-->

* **pstr**: A length prefixed string, with a VLQ specifying the length.
* **[u]int##**: An integer, in big-endian order. "u" indicates unsiged and ## is the length, in bits. Examples: uint8, int32, etc.
* **[s]VLQ**: [Variable length quantity](https://en.wikipedia.org/wiki/Variable-length_quantity). "s" indicates signed.

## Base Packet

Each packet is wrapped in this basic package:

<table class="table">
    <thead>
        <tr>
            <th>Type</th>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>uint8</td>
            <td>Packet ID</td>
            <td>The packet identifier. The payload format changes based on this value.</td>
        </tr>
        <tr>
            <td>sVLQ</td>
            <td>Payload length</td>
            <td>The length of the payload, in bytes. If it is negative, this indicates the payload is compressed using zlib.</td>
        </tr>
        <tr>
            <td>Varies</td>
            <td>Payload</td>
            <td>Varies</td>
        </tr>
    </tbody>
</table>

## Packets

### Protocol Version
TODO
### Connect Response
TODO
### Server Disconnect
TODO
### Handshake Challenge
TODO
### Chat Received
TODO
### Universe Time Update
TODO
### Client Connect
TODO
### Client Disconnect
TODO
### Handshake Response
TODO
### Warp Command
TODO
### Chat Sent
TODO
### Client Context Update
TODO
### World Start
TODO
### World Stop
TODO
### Tile Array Update
TODO
### Tile Update
TODO
### Tile Liquid Update
TODO
### Tile Damage Update
TODO
### Tile Modification Failure
TODO
### Give Item
TODO
### Unknown
TODO
### Swap in Container Result
TODO
### Environment Update
TODO
### Entity Interact Result
TODO
### Modify Tile List
TODO
### Damage Tile
TODO
### Damage Tile Group
TODO
### Request Drop
TODO
### Spawn Entity
TODO
### Entity Interact
TODO
### Connect Wire
TODO
### Disconnect All Wires
TODO
### Open Container
TODO
### Close Container
TODO
### Swap in Container
TODO
### Item Apply in Container
TODO
### Start Crafting in Container
TODO
### Stop Crafting in Container
TODO
### Burn Container
TODO
### Clear Container
TODO
### World Update
TODO
### Entity Create
TODO
### Entity Update
TODO
### Entity Destroy
TODO
### Damage Notification
TODO
### Status Effect Request
TODO
### Update World Properties
TODO
### Heartbeat
TODO