**Handshake and Crypto Documenting**


![image](https://user-images.githubusercontent.com/84244797/229498511-c5d801f4-8272-4fdc-ad74-d4370ced8e62.png)

Initial Packet (Clienthello and Serverhello) {

  Header Form (1) = 1,
  
  Fixed Bit (1) = 1,
  
  Long Packet Type (2) = 0,
  
  Reserved Bits (2),
  
  Packet Number Length (2),
  
  Version (32),
  
  Destination Connection ID Length (8),
  
  Destination Connection ID (0..160),
  
  Source Connection ID Length (8),
  
  Source Connection ID (0..160),
  
  Token Length (i),
  
  Token (..),
  
  Length (i),
  
  Packet Number (8..32),
  
  Packet Payload (8..),
}

It carries the first CRYPTO frames sent by the client and server to
perform key exchange, and it carries ACK frames in either direction.
