# Custom TFTP Client-Server Implementation

A robust implementation of the Trivial File Transfer Protocol (TFTP) written in C. This project demonstrates reliable file transfer over UDP, featuring custom block sizes and cross-platform text translation.

## 🚀 Features
- **Operation Support:** Full implementation of `RRQ` (Read) and `WRQ` (Write).
- **Mode Selection:**
    - **Octet (Mode 2):** Supports 1-byte block transfers (custom requirement).
    - **Netascii (Mode 0):** Automatic translation between Unix (`\n`) and Network (`\r\n`) newlines.
- **Reliability:** Stop-and-wait acknowledgment (ACK) system.
- **Socket Management:** Port reuse logic (`SO_REUSEADDR`) for immediate server restarts.
- **Clean Exit:** Graceful client disconnection and socket cleanup.

## 🛠️ Compilation
Compile both components using `gcc` from your terminal:

```bash
# Compile Server
gcc server.c -o tftp_server

# Compile Client
gcc client.c -o tftp_client
