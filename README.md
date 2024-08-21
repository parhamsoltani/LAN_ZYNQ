# LAN_PS

## Description
LAN_PS is a project that launches a UDP & TCP server in a LAN network on ZYNQ-7020 Processing System (PS) using the lwIP library. The project implements both UDP and TCP functionalities.

## Technologies Used
- C
- Verilog
- lwIP library
- Xilinx Vivado&SDK

## Key Features
- UDP server implementation
- TCP server implementation (echo server on port 7)
- DHCP client support
- IPv4 and IPv6 support

## Important note
The `xemacpsif_physpeed` file located in the following directory may require modifications based on the specific board and chip's part number:
>LAN_PS.sdk\standalone_bsp_0\ps7_cortexa9_0\libsrc\lwip211_v1_0\src\contrib\ports\xilinx\netif
Please ensure to review and adjust this file according to your hardware configuration for optimal performance.

## Main Components
The core of the project is the `main.c` file in the SDK section. Some key UDP-related functions include:

```c
void UDPServer_init(void);
void Send_UDP(u8 *ptr, int cnt);
void recv_callback_udp(void *arg, struct udp_pcb *upcb, struct pbuf *pkt_buf, struct ip_addr *addr, u16_t port);
