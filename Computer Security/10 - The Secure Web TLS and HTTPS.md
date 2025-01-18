# Diffie-Hellman Key Exchange
- First published public-key algorithm
- Practical method to exchange a secret key securely that can then be used for subsequent encryption of messages
- Security relies on difficulty of computing discrete logarithms

# The Heartbleed Exploit
- Exploits the bug in TLS Heartbeat
- Sends a small data with false length field
- the implementation did not validate the length properly
- therefore copying data in memory that could contain sensitive data such as secret key
