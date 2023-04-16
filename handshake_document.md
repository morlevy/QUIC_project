**Handshake and Crypto Documenting**


![image](https://user-images.githubusercontent.com/84244797/229498511-c5d801f4-8272-4fdc-ad74-d4370ced8e62.png)     
<img width="579" alt="Screenshot 2023-04-03 at 17 02 26" src="https://user-images.githubusercontent.com/84244797/229532849-8951309d-00e2-4b89-ad1d-9183903dce85.png">


<img width="587" alt="Screenshot 2023-04-03 at 17 01 11" src="https://user-images.githubusercontent.com/84244797/229532549-912d9706-281f-4908-a9d2-ed1b63b37817.png">

It carries the first CRYPTO frames sent by the client and server to
perform key exchange, and it carries ACK frames in either direction.


Client                                                    Server
======                                                    ======

Get Handshake
                     Initial ------------->
Install tx 0-RTT keys
                     0-RTT - - - - - - - ->
                                              Handshake Received
                                                   Get Handshake
                     <------------- Initial
                                           Install rx 0-RTT keys
                                          Install Handshake keys
                                                   Get Handshake
                     <----------- Handshake
                                           Install tx 1-RTT keys
                     <- - - - - - - - 1-RTT

Handshake Received (Initial)
Install Handshake keys
Handshake Received (Handshake)
Get Handshake
                     Handshake ----------->
Handshake Complete
Install 1-RTT keys
                     1-RTT - - - - - - - ->
                                              Handshake Received
                                              Handshake Complete
                                             Handshake Confirmed
                                           Install rx 1-RTT keys
                     <--------------- 1-RTT
                           (HANDSHAKE_DONE)
Handshake Confirmed


solid arrows indicate packets that carry handshake data; dashed arrows show where application data can be sent. Each arrow is tagged with the encryption level used for that transmission.
