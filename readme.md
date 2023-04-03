quic python implementation: https://github.com/aiortc/aioquic.git

quic packets:  https://blogs.keysight.com/blogs/tech/nwvs.entry.html/2021/07/17/looking_into_quicpa-pUtF.html

documenting1 is about several attacks in "Revisiting QUIC attacks: A comprehensive review on QUIC security
and a hands-on study." 

"Version Negotiation packets have no cryptographic protection" therefore we can do downgarde attack on the connection.

"Retry packets use a fixed key and so similarly lack confidentiality and integrity protection." (RFC 9001)

"The initial secret is determined by using HKDF-Extract (see Section 2.2 of [HKDF]) with a 
salt of 0x38762cf7f55934b34d179ae6a4c80cadccbb7f0a and the input keying material (IKM)
of the Destination Connection ID field. This produces an intermediate pseudorandom key (PRK)
that is used to derive two separate secrets for sending and receiving." (RFC 9001) this is a pseudorandom key so we could reproduce it.


<img width="1078" alt="Screenshot 2023-04-03 at 19 25 51" src="https://user-images.githubusercontent.com/84244797/229570311-055ef52b-d9a9-4ad3-ba58-272d43ca1e1d.png">


