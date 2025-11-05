 Explanation:

Symmetric encryption uses one key for both encryption and decryption.

Fast and efficient but risky to share the same key.

Example algorithms: AES, DES, 3DES


Asymmetric encryption uses two keys — a public key (to encrypt) and a private key (to decrypt).

Slower but more secure for key exchange.

Example algorithms: RSA, ECC



Real-world Example:

WhatsApp uses asymmetric encryption to exchange a session key, then symmetric encryption (AES) for fast message encryption.



---

🔹 4.2 Hashing (MD5, SHA, bcrypt)

File name: lesson4-2-hashing-algorithms.md

Explanation:
Hashing is a one-way encryption used to verify data integrity or store passwords securely.
Once hashed, data can’t be reversed.

Algorithm	Strength	Use Case

MD5	Weak	File integrity (avoid using for passwords)
SHA-256	Strong	Modern secure hashing
bcrypt	Very Strong	Password storage (with salting)


Example:
When you create a password:

Password: P@ssw0rd
Hash (SHA-256): 56a0f9dff9e2...

Websites store only the hash, not the real password.

Try it:
Use CyberChef or the Linux command:

echo -n "P@ssw0rd" | sha256sum


---

🔹 4.3 Public Key Infrastructure (PKI)

File name: lesson4-3-public-key-infrastructure.md

Explanation:
PKI is a system that manages digital certificates and keys to enable trust online.
It includes:

Certificate Authority (CA) – verifies identity (like a passport office)

Public/Private Keys – used to encrypt or sign data

Digital Certificates – bind an identity to a public key


Example:
When you visit https://, your browser checks the site’s certificate (via PKI) before connecting.

Key Concept:
PKI = Trust + Identity + Encryption


---

🔹 4.4 SSL/TLS & HTTPS Certificates

File name: lesson4-4-ssl-tls-and-https.md

Explanation:

SSL/TLS encrypts data between your device and a website.

HTTPS = HTTP + SSL/TLS → secure web communication.


Example:
If you log in to https://gcash.com, your password is encrypted before being sent.

Check It Yourself:
Click 🔒 icon beside any site URL → View Certificate → See “Issued by” (CA) and “Valid until.”

Tip:
Always use sites with HTTPS — never enter passwords on plain http://.
