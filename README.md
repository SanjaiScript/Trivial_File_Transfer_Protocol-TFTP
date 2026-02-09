# Custom TFTP Client-Server Implementation

A robust implementation of the Trivial File Transfer Protocol (TFTP) written in C. This project demonstrates reliable file transfer over UDP, featuring custom block sizes and cross-platform text translation.

##  Features
- **Operation Support:** Full implementation of `RRQ` (Read) and `WRQ` (Write).
- **Mode Selection:**
    - **Netascii (Mode 0):** Automatic translation between Unix (`\n`) and Network (`\r\n`) newlines.
    - **Default (Mode 1):** Standard 512-byte block transfers.
    - **Octet (Mode 2):** Custom 1-byte block transfers for specific data integrity testing.
- **Reliability:** Stop-and-wait acknowledgment (ACK) system.
- **Clean Exit:** Graceful client disconnection and socket cleanup.

## Client Menu
1. **Connect:** Initialize the socket to the server.
2. **Mode:** Select between Netascii (0), Default (1), or Octet (2).
3. **Put:** Upload a local file to the server.
4. **Get:** Download a file from the server.
5. **Exit:** Disconnect and close the program.

## Project Structure
- `server.c`: Main server logic and request handling.
- `client.c`: User interface and file transfer initiation.

## 🛠️ Compilation
Compile both components using `gcc` from your terminal:

```bash
# Compile Server
gcc server.c -o tftp_server

# Compile Client
gcc client.c -o tftp_client
```
## Author
    Sanjai Kumar M

## LICENSE
    This project is licensed under the MIT License.
