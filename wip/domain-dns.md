
## Cryptography (Signatures, Challenges, encryptions, ...)

I have a good understanding of cryptographical concepts.  
Among them, I have worked a lot with certificates (public and internal).

I know how self-signed certificates work and how to use them.

Wildcard certificates don't work on the first level, e.g. `*.mydomain` will not be validated by a browser for security reasons.
But `*.sub.mydomain` will work.

## DNS

CNAME are not aliases, they must be unique per name. This is why we cannot have a CNAME at the APEX: Because they conflict with the NS records.
DNS are used for DNS-challenges upon certificate generation, especially when using multiple SAN or wildcard certificates.
