# LAN_PS

## Description
LAN_PS is a project that launches a UDP & TCP server in a LAN network on ZYNQ-7020 Processing System (PS) using the lwIP library. The project implements both UDP and TCP functionalities, with a focus on UDP server operations.

## Technologies Used
- C
- Verilog
- lwIP library
- Xilinx SDK

## Key Features
- UDP server implementation
- TCP server implementation (echo server on port 7)
- DHCP client support
- IPv4 and IPv6 support

## Main Components
The core of the project is the `main.c` file in the SDK section. Key UDP-related functions include:

```c
void UDPServer_init(void);
void Send_UDP(u8 *ptr, int cnt);
void recv_callback_udp(void *arg, struct udp_pcb *upcb, struct pbuf *pkt_buf, struct ip_addr *addr, u16_t port);
