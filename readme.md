quic python implementation: https://github.com/aiortc/aioquic.git

quic packets:  https://blogs.keysight.com/blogs/tech/nwvs.entry.html/2021/07/17/looking_into_quicpa-pUtF.html

documenting1 is about several attacks in "Revisiting QUIC attacks: A comprehensive review on QUIC security
and a hands-on study." 

"Version Negotiation packets have no cryptographic protection" therefore we can do downgarde attack on the connection.

"Retry packets use a fixed key and so similarly lack confidentiality and integrity protection." (RFC 9001)
