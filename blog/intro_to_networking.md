https://ciscolicense.com/wp-content/uploads/2021/06/Cisco-Networking-Licenses.jpg

$$img-end$$

# Introduction to Networking

## 1. What is a Network?

**A network** is a group of **devices** that can communicate with each other over **links**. Each device is called a host. Each host has a unique **address**.

## 2. The Internet :globe_with_meridians:

**The internet** is a network of networks. On the internet, each host has an address of the form n/h where n is the network number and h is the number of the host on network n. As long as all of the networks in the internet have unique network numbers, combining the network number and host number will give unique global names. Therefore from the outside an internet looks like a single network!.

## 3. How To Study Computer Networking?

The field of computer networks is very large and has a few overlapping areas of study. One coarse breakdown of the field into topics is:

| Area                                                         | Topics                                                                         |
| :----------------------------------------------------------- | :----------------------------------------------------------------------------- |
| Data Transmission                                            | Hardware, Physical media (e.g., wireless, optical fiber) & How data is encoded |
| Packet Switching                                             | Packet formats, Packet flow within a network & Routing between networks        |
| Network Architecture                                         | Internetwork Topologies, Protocols, OSI & TCP/IP Models                        |
| Network Applications                                         | Well known apps (Email, DNS, FTP, Web..) & Client-server vs. P2P applications  |


## 4. Layers

In order to be understood by humans, complex systems must be designed in a hierarchical fashion, with clear separation of concerns between layers. Internets are complex. A commonly accepted approach to network design is the four layer model:

![four_layer_model](https://i.postimg.cc/tgMqyQx7/layers.png)

Conceptually, each layer talks to the corresponding layer on the other host via some sort of protocol. Within a host, layers talk only to the layer just below or above. And they don’t care how any of the other layers are implemented; they use inter-layer APIs (e.g. the link library provides services that the network library invokes).

![layers_connection](https://i.postimg.cc/nrnwPMhm/layers-connection.png)

So, the layers are (yes I know they are “out of order”):

* **Application**: Applications are programs like the World Wide Web, BitTorrent, or Skype. Applications on different computers talk to each other as if there is a (generally) reliable, bi-directional byte stream to communicate over. Applications use protocols like HTTP to talk to each other. Applications don’t know or care how the data gets from one host to another. Even though applications only see streams, the data is (behind the scenes) actually delivered in packets.
* **Link**: The job of the link layer is to get packets across a single link. How this happens is determined by hardware and other physical characteristics.
* **Network**: The network layer’s job is to get packets all the way across the network from the source host to the destination host. It reads the header in each packet to see where it is going and consults routing tables in the routers to see where to send it next. It uses the services of the link layer to send it one link at a time. It does not care how the link layer works (or whether it is Ethernet or WiFi or DSL or 4G or whatever.) Generally the network layer makes no guarantees that the packets will arrive in order, makes no guarantees they will not be duplicated, and makes no guarantees they will even arrive at all!
* **Transport**: This layer is responsible for (if desired) retransmitting and reordering packets to provide reliability on top of the unreliable network layer, and handles congestion. (TCP does this, UDP does not). While the network layer is concerned with routing packets to the right destination host, the transport layer gets data to the right application running on the host.
