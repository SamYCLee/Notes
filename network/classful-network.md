# Classful Network

## Introduction

A classful network is a network addressing architecture used in the Internet from 1981 until the introduction of Classless Inter-Domain Routing in 1993.

The method divides the IP address space for Internet Protocol version 4 (IPv4) into five address classes based on the leading four address bits.

Classes A, B, and C provide unicast addresses for networks of three different network sizes. Class D is for multicast networking and the class E address range is reserved for future or experimental purposes.

## Classful Addressing Definition

Under classful network addressing, the 32-bit IPv4 address space was partitioned into 5 classes (A-E) as shown in the following tables.

### Classes

| **Class** | **Leading bits** | **Size of network number bit field** | **Size of rest bit field** | **Number of networks** | **Addresses per network** | **Total addresses in class** | **Start address** | **End address** | **Default subnet mask** | **CIDR Notation** |
|---|---|---|---|---|---|---|---|---|---|---|
| Class A | 0 | 8 | 24 | 128 (2<sup>7</sup>) | 16,777,216  (2<sup>24</sup>) | 2,147,483,648 (2<sup>31</sup>) | 0.0.0.0 | 127.0.0.0 | 255.0.0.0 | /8 |
| Class B | 10 | 16 | 16 | 16,384 (2<sup>14</sup>) | 65,536 (2<sup>16</sup>) | 1,073,741,824 (2<sup>30</sup>) | 128.0.0.0 | 191.255.0.0 | 255.0.0.0 | /16 |
| Class C | 110 | 24 | 8 | 2,097,152  (2<sup>21</sup>) | 16,777,216 (2<sup>8</sup>) | 536,870,912  (2<sup>29</sup>) | 192.0.0.0 | 223.255.255.0 | 255.0.0.0 | /24 |
| Class D | 1110 | not defined | not defined | not defined | not defined | 268,435,456  (2<sup>28</sup>) | 224.0.0.0 | 239.255.255.255 | not defined | not defined |
| Class E | 1111 | not defined | not defined | not defined | not defined | 268,435,456  (2<sup>28</sup>) | 240.0.0.0 | 255.255.255.255 | not defined | not defined |

## Reference

- <https://en.wikipedia.org/wiki/Classful_network>