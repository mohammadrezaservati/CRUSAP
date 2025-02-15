## Analysis and Implementation of Security Attack on CRUSAP Protocol in RFID-Based MIoT

### Introduction
CRUSAP protocol is introduced as an ultra-lightweight authentication method for RFID systems in Medical Internet of Things (MIoT). Using the Cro(·) operation, it aims to ensure the security of transmitted data, but this project demonstrates its significant security vulnerabilities.

### CRUSAP Protocol Vulnerabilities
The analysis revealed that the Cro(·) operation is linear and reversible, allowing attackers to easily extract the secret values used in computations. Leveraging this weakness, a Secret Disclosure Attack was implemented, successfully exposing key values with a 100% success rate in a single protocol run.

### Attack Details
The Secret Disclosure Attack captures transmitted messages between the tag and reader, reversing the Cro(·) operation to obtain the shared key KR. Once KR is obtained, the attacker can also derive KT, compromising the entire authentication system.

### Implementation in C#
The attacks are implemented in C# and include:
- **Calculating main CRUSAP protocol messages**
- **Reversing the Cro(·) operation**
- **Extracting KR and KT key values**
- **Verifying the attack using initial values**

### How to Run
1. Run the provided code in Visual Studio.
2. Set initial values such as RIDS, KR, and KT.
3. Execute the attack and observe the extracted key values.

### Conclusion
This project highlights the vulnerability of the CRUSAP protocol due to the linear nature of Cro(·), making it susceptible to Secret Disclosure Attacks that compromise system security.

### Article Link
[Cryptanalysis of Two Recent Ultra-Lightweight Authentication Protocols](https://doi.org/10.3390/math10234611)

### License
This project is licensed under the [Creative Commons Attribution (CC BY)](https://creativecommons.org/licenses/by/4.0/).

