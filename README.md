# OSI Model

The **OSI Model (Open Systems Interconnection Model)** is a conceptual networking framework used to standardize how devices communicate. It consists of **7 layers**, each with a unique function in the process of sending and receiving data. This structure ensures different systems can communicate even if they use different technologies.

---

## Layer Overview

| Layer | Name         | Function                                      |
|-------|--------------|-----------------------------------------------|
| 7     | Application  | User interaction, protocols (HTTP, DNS, SMTP) |
| 6     | Presentation | Data formatting, translation, encryption      |
| 5     | Session      | Establishes, manages, and terminates sessions |
| 4     | Transport    | Reliable/unreliable delivery (TCP/UDP)        |
| 3     | Network      | Routing, logical addressing (IP)              |
| 2     | Data Link    | MAC addressing, frame delivery                |
| 1     | Physical     | Hardware signals, cables, binary transfer     |

---

## OSI Model – Concept

The OSI model (Open Systems Interconnection) is an essential networking model.  
It defines how all networked devices send, receive, and interpret data by splitting  
communication into **seven layers**. Each layer adds its own header or information  
to the data in a process called **encapsulation**.

### Key points

- **"OSI" stands for:** Open Systems Interconnection  
- **Number of layers:** 7  
- **Key term for adding information to data:** encapsulation  

---

## Layer 1 – Physical

The **Physical Layer** references the physical components of networking hardware.  
Devices use electrical or optical signals to transfer data in a **binary** format (0s and 1s).

Examples: Ethernet cables connecting devices.

<img src="https://github.com/user-attachments/assets/b7639738-c2f3-4b1d-8650-2f99717bd260" width="350">

**Questions & Answers**

- Name of this layer: **Physical**  
- Numbering system that uses 0s and 1s: **Binary**  
- Cables used to connect devices: **Ethernet Cables**  

---

## Layer 2 – Data Link

The **Data Link Layer** focuses on **physical addressing** and frame formatting.  
It receives packets from the Network Layer and adds the physical **MAC address** of the destination.

Each network-enabled device has a **Network Interface Card (NIC)** with a unique MAC address.  
These addresses are usually burned into the hardware (though they can be spoofed).

<img src="https://github.com/user-attachments/assets/5f033849-00f1-4cb5-8563-3dc21e87c611" width="350">

**Questions & Answers**

- Name of this layer: **Data Link**  
- Hardware that networked devices come with: **Network Interface Card**  

---

## Layer 3 – Network

The **Network Layer** is responsible for **routing** and **logical addressing**.  
It chooses the most optimal route for data packets across networks.

Routing decisions are based on:
- Shortest path (fewest hops)  
- Most reliable path (fewer packet losses)  
- Fastest medium (fiber vs copper)

Common routing protocols:
- **OSPF** (Open Shortest Path First)  
- **RIP** (Routing Information Protocol)

At this layer, devices use **IP addresses** such as `192.168.1.100`.  
Routers that route IP packets are known as **Layer 3 devices**.

<img src="https://github.com/user-attachments/assets/93738d3d-335c-4cb2-84d2-8317e9a9d50a" width="350">

**Questions & Answers**

- Name of this layer: **Network**  
- Will packets take the most optimal route? **Y**  
- OSPF stands for: **Open Shortest Path First**  
- RIP stands for: **Routing Information Protocol**  
- Type of addresses used at this layer: **IP Addresses**  

---

## Layer 4 – Transport

The **Transport Layer** is responsible for end-to-end communication and reliability.  
It mainly uses two protocols:

- **TCP** – Transmission Control Protocol  
- **UDP** – User Datagram Protocol  

### TCP (Transmission Control Protocol)

- Connection-oriented  
- Ensures data is received correctly and in order  
- Performs error checking and retransmission  
- Slower, but reliable

Used for:
- Web browsing  
- Email  
- File transfers  

<img src="https://github.com/user-attachments/assets/43e462cb-2935-4237-ae05-58b7488446a3" width="350">

### UDP (User Datagram Protocol)

- Connectionless  
- No guarantee that data arrives  
- No ordering or error recovery  
- Much faster than TCP

Used for:
- Streaming video  
- Voice over IP  
- Discovery protocols (e.g., DHCP, ARP)

<img src="https://github.com/user-attachments/assets/a3d0e798-d80a-4432-961c-6ed66e856585" width="350">

**Questions & Answers**

- Name of this layer: **Transport**  
- TCP stands for: **Transmission Control Protocol**  
- UDP stands for: **User Datagram Protocol**  
- Protocol that guarantees accuracy of data: **TCP**  
- Protocol that doesn’t care if data is received: **UDP**  
- Protocol used by an email client: **TCP**  
- Protocol used to download files: **TCP**  
- Protocol used to stream video: **UDP**  

---

## Layer 5 – Session

The **Session Layer** creates, manages, and terminates sessions between applications.  
When a connection is established, a **session** is created and maintained while communication continues.

It can also use **checkpoints**, so if a connection fails, only new data must be resent instead of all data.

<img src="https://github.com/user-attachments/assets/0163fcf1-86b1-42e5-8a52-59e33130785f" width="350">

**Questions & Answers**

- Name of this layer: **Session**  
- Technical term when a connection is successfully established: **Session**  

---

## Layer 6 – Presentation

The **Presentation Layer** is responsible for **translating, formatting, compressing, and encrypting** data.

Because different software can store or represent data differently, this layer ensures that data is handled in a standard way so both sides can understand it.

Security features such as **encryption (e.g., HTTPS)** occur at this layer.

<img src="https://github.com/user-attachments/assets/4c64f3d7-0388-4dc7-b55d-0a58cce832a1" width="350">

**Questions & Answers**

- Name of this layer: **Presentation**  
- Main purpose of this layer: **Translator**  

---

## Layer 7 – Application

The **Application Layer** is the layer closest to the user.  
It defines protocols and rules for how user applications interact with the network.

Examples:
- Web browsers  
- Email clients  
- File transfer tools (e.g., FTP clients)  
- DNS (resolving domain names to IP addresses)

<img src="https://github.com/user-attachments/assets/bfce5102-77b5-4aa1-9ae3-15bf01755f6b" width="350">

**Questions & Answers**

- Name of this layer: **Application**  
- Technical term for the software interface users see: **Graphical User Interface**  

---

## OSI Model Diagram

<img src="https://github.com/user-attachments/assets/53a5f6bc-0855-4c8d-8593-1b92e7da735b" width="450">

---

## Practical – OSI Game

In the TryHackMe OSI dungeon game, you must climb the layers in the correct order to escape and obtain the flag.

**Flag:**

```text
THM{OSI_DUNGEON_ESCAPED}
