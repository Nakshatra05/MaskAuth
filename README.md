# MaskAuth: Decentralized 2FA with ZK Proofs & AI Face Recognition

**MaskAuth** is a decentralized, privacy-first, two-factor authentication (2FA) system leveraging **Polkadot's multi-chain infrastructure**, **Zero-Knowledge Proofs (ZKPs)**, and **AI-based Face Recognition** to ensure secure and user-friendly transaction authentication for Web3 applications.

---

## 🔒 Why MaskAuth?

In Web3, losing private keys often means losing funds forever. MaskAuth introduces an **extra layer of security** that allows users to authenticate transactions securely without compromising privacy or relying on centralized systems. Using **Face Recognition** and **ZKP**, it ensures that user identity is verified anonymously, eliminating risks from traditional 2FA systems.

---

## 🚀 Features

- **Decentralized Two-Factor Authentication**: Uses AI face recognition and ZKPs to secure transactions without centralized oversight.
- **Privacy-Preserving**: No personal data is stored or shared; the process is fully anonymized through ZKPs.
- **Polkadot Integration**: Built on **Substrate**, it benefits from Polkadot's scalability, interoperability, and security.
- **Multi-Device Support**: Allows secure verification across devices via WalletConnect.
- **Custom ZK Circuits**: Uses **Circom** circuits to handle anonymous proof generation and verification.

---

## 🛠️ Architecture

### 1. **User Registration**
- Users register by:
  - Connecting their wallet using **WalletConnect**.
  - Capturing 5-6 images of their face to create a dataset for the **DeepFace AI model**.
  - A unique cryptographic key is generated and stored securely in a decentralized system.
  - The **Poseidon hash** of this key is stored on-chain for later verification.

### 2. **Transaction Verification**
- When initiating a transaction:
  - The user receives a notification on their registered device.
  - The app triggers face recognition via the **DeepFace AI model**.
  - The face data is verified through a **ZKP circuit** to prove authenticity without revealing identity.
  - The **ZKP output** determines if the transaction proceeds or is rejected.

---

## 📂 Directory Structure

```
MaskAuth/
├── client/                # React Native app for user interface
├── backend/               # Backend API for AI model and ZKP processing
├── zk-circuits/           # Circom circuits for ZKP proof generation
├── smart-contracts/       # Substrate-based smart contracts for Polkadot
├── subgraph/              # Subgraph for querying on-chain data
├── push-channel/          # Push protocol integration for notifications
├── docs/                  # Documentation, architecture diagrams, and workflows
└── README.md              # Project overview (this file)
```

---

## 📦 Installation

### Prerequisites

- Node.js and npm
- Rust (for Substrate smart contracts)
- Circom (for ZKP circuits)
- Docker (optional for running services locally)

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/MaskAuth.git
   cd MaskAuth
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Compile ZK Circuits:
   ```bash
   cd zk-circuits
   circom zkproof.circom --r1cs --wasm --sym
   ```

4. Deploy Substrate Smart Contracts:
   ```bash
   cd smart-contracts
   cargo build --release
   substrate-deploy --network=testnet
   ```

5. Start the Frontend:
   ```bash
   cd client
   npm start
   ```

6. Start the Backend:
   ```bash
   cd backend
   npm start
   ```

---

## 💻 Technologies Used

- **Blockchain**: Polkadot (Substrate framework)
- **Zero-Knowledge Proofs**: Circom and SnarkJS
- **AI Face Recognition**: DeepFace
- **Frontend**: React Native
- **Backend**: Node.js, Express
- **Push Notifications**: Push Protocol
- **Smart Contracts**: Rust, Ink!
- **Decentralized Storage**: IPFS/Filecoin

---

## 📈 Use Cases

1. **Securing Transactions**: Adds an extra layer of security for DApps, ensuring user funds are safe even if private keys are compromised.
2. **Authentication for DAOs**: Validates members during voting or proposal submissions.
3. **Decentralized Finance (DeFi)**: Secures high-value transactions in lending, staking, or trading platforms.

---

## 🛡️ Security & Privacy

- **Zero-Knowledge Proofs** ensure no sensitive data is shared.
- **Decentralized Design** removes reliance on centralized authentication servers.
- **End-to-End Encryption** for communication between devices.

---

## 🧑‍💻 Contributing

We welcome contributions! To get started:

1. Fork the repository.
2. Create a new branch for your feature/fix.
3. Submit a pull request with a detailed description.

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

## 🌐 Live Demo

A live demo will be available soon. Stay tuned for updates!

---

## 🛠️ Future Enhancements

- Multi-language support for a global audience.
- Enhanced AI model for better recognition accuracy.
- Support for biometric fallback methods like fingerprint authentication.

---

## 🙌 Acknowledgments

- **Polkadot Hackathon Team**: For providing the platform and resources.
- **Circom Community**: For their support with ZKP implementation.
- **DeepFace Contributors**: For the open-source face recognition model.

---

### 🚀 Let’s redefine transaction security together with **MaskAuth**! 🚀
