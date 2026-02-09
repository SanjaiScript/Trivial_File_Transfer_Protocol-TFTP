# Custom TFTP Client-Server Implementation

A robust implementation of the Trivial File Transfer Protocol (TFTP) written in C. This project demonstrates reliable file transfer over UDP, featuring custom block sizes and cross-platform text translation.

## Features
- **Operation Support:** Full implementation of `RRQ` (Read) and `WRQ` (Write).
- **Mode Selection:**
    - **Default (Mode 1):** Supports 512-bytes block transfers(custom requirement).
    - **Octet (Mode 2):** Supports 1-byte block transfers.
    - **Netascii (Mode 3):** Automatic translation between Unix (`\n`) and Network (`\r\n`) newlines.
- **Reliability:** Stop-and-wait acknowledgment (ACK) system.
- **Clean Exit:** Graceful client disconnection and socket cleanup.

## Client Menu
    - Connect: Initialize the socket to the server.
    - Mode: Select between Default(1) Octet(2) or Netascii (0).
    - Put: Upload a local file to the server.
    - Get: Download a file from the server.
    - Exit: Disconnect and close the program.

## Project Structure
    - server.c: Main server logic and request handling.
    - client.c: User interface and file transfer initiation.

## Compilation
Compile both components using `gcc` from your terminal:

```bash
# Compile Server
gcc server.c -o tftp_server

# Compile Client
gcc client.c -o tftp_client

## Author
    Sanjai Kumar M

## LICENSE
    - This project is licensed under the MIT License.

