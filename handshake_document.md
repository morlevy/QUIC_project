**Handshake and Crypto Documenting**


![image](https://user-images.githubusercontent.com/84244797/229498511-c5d801f4-8272-4fdc-ad74-d4370ced8e62.png)     


![Screenshot 2023-04-16 at 13 18 35](https://user-images.githubusercontent.com/84244797/232295566-923ffbf5-ee93-47fd-acd8-3a0b8f71d30a.png)


solid arrows indicate packets that carry handshake data; dashed arrows show where application data can be sent. Each arrow is tagged with the encryption level used for that transmission.


**Address validation token** 

Upon receiving the client's Initial packet, the server can request address validation by sending a Retry packet containing a token. This token MUST be repeated by the client in all Initial packets it sends for that connection after it receives the Retry packet. this is in order to validate the client (prevents from ip spoofing).
As long as it is not possible for an attacker to generate a valid token for its own address and the client is able to return that token, it proves to the server that it received the token.

Note: "The anti-amplification limit only applies when an endpoint responds to packets received from an unvalidated address. The anti-amplification limit does not apply to clients when establishing a new connection or when initiating connection migration."


handshake article: https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9328313
