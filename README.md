# rsa-encryption-demo - RSA Cryptography with Large Primes

This project demonstrates a full implementation of RSA encryption and decryption using large prime numbers. It includes key generation, message segmentation, encryption, and decryption.

## 📌 Features

- Generation of large prime numbers with reproducibility via seed
- RSA key generation (public and private)
- Encryption using ASCII-to-integer conversion
- Decryption back to readable text
- Handles long messages by splitting them into segments

## 🔧 Technologies

- Python 3.x
- `sympy` for number theory operations like primality and modular inverse

## ▶️ Example: "Hello, RSA!"

This example shows the complete RSA process for the message `"Hello, RSA!"`:

- **Prime p:** 2251799813685269  
- **Prime q:** 1125899906842679  
- **RSA modulus m:** 2535301200456606295881202795651  
- **Euler's totient φ(m):** 2535301200456602918181482267704  
- **Public exponent e:** 65537  
- **Private key d:** 1998662381884895399054675700153  

### ✅ Message Processing

- **Encoded message (ASCII):**  
  `[72, 101, 108, 108, 111, 44, 32, 82, 83, 65, 33]`

- **Encrypted message:**  
  `[28061120901895275953930945051, 226259574571602256390986652872, 2037095814340179368710037137923, 2037095814340179368710037137923, 591495336882847421521612954506, 1190257826825461609359848970238, 1660002791670398877016213770352, 1179923768638546129452659395401, 2429645561199500518734365795377, 1429246960225544498142162066864, 2278792458201052045102816374404]`

- **Decrypted message (ASCII):**  
  `[72, 101, 108, 108, 111, 44, 32, 82, 83, 65, 33]`

- **Decoded message:**  
  `Hello, RSA!`

## 📂 File Structure

- `rsa_crypto.py`: Main Python script
- `requirements.txt`: List of required packages
- `README.md`: Project documentation

## 💻 How to Run

1. **Clone the repository:**
```bash
git clone https://github.com/Undead6687/rsa-large-prime-crypto.git
cd rsa-large-prime-crypto
```

2. (Optional) Create a virtual environment:
```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate'
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Run the script:
```bash
python rsa_crypto.py
```

## 🧠 Key Concepts

- **Prime Generation:** Uses `sympy.nextprime()` seeded with random values for reproducibility.
- **RSA Encryption:** Encrypts using `ciphertext = (message^e) mod n`.
- **Message Segmentation:** Long plaintext is split into 10-word chunks for encryption.
- **ASCII Packing:** Characters are encoded into integers using zero-padded ASCII.

## 🛡 Security Note

This project is for educational and experimental purposes only. It does not implement secure padding schemes (e.g., OAEP) and is not safe for production use.

## 📜 License

[MIT License](https://choosealicense.com/licenses/mit/)

---

> Made with ❤️ by Miran Shaikh
