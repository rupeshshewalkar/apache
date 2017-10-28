## SSL handsake
1. the client started the handshake with sending information like SSL version, cipher suites, and compression method.
2. The server then checks for the highest SSL version that is supported by both of them.
The server also chooses the compression method and the cipher suite from the client’s option.
After this exchange, the server sends a certificate (public key) to the client.

Certificate contain:

		a) Domain name 
        b) Public key
        c) Owner of certificate
        d) Issue of the certificate (CA)
        e) Expire date
        f) Serial Number
        
3. The client confirms the certificate, creates pre-master secret for the session, and encrypts the session with the server’s public key.

    Client check certificate status 
              a) Client submit OCSP request
              b) Client CRL database
              c) If certificate revoked, client sends error
              d) If clear then continue communication


4. The server receives pre-master secret and decrypt it with the private key.

5. Both parties agree on a single cipher suite and generate the session keys (symmetric keys) to encrypt and decrypt the information during an SSL session.

7. Once above thing happen, unique session key pair established 
8. Encryption tunnel establish with key
9. then all traffic encrypted.



