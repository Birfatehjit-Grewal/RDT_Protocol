# RDT_Protocol
This protocol implements a connection-oriented, reliable, pipelined data transfer protocol which includes flow control and congestion control mechanisms. The protocol using UDP sockets as a base and add features like 3-way hand handshake, Loss recovery through retransmission with a timeout and fast retransmission using duplicate ACKs. I also implemented a checksum in case of bit flips. The flow control is handled by reading the available buffer space in the response and limiting the sent packets to avoid overflow. I use slow-start congestion control as my congestion control mechanism.

## How to run the code
Use the latest version of python which can be downloaded from [here](https://www.python.org/downloads/)

Run the receiver.py first by running the following `python receiver.py` in the terminal or command prompt

Then Run the sender.py by running the following `python script.py <server_ip> <server_port> <listening_port>` in the terminal or command prompt after filling out the needed paramaters.

* replace <server_ip> with the ip address of the computer running the receiver.py
* replace <server_port> with the port the receiver is listening on which by default is `8080`
* replace <listening_port> with th port the sender will be listening on
