# 🧾 TrustLedger: Tuple-Based Trust Economy

## 🌐 Overview
**TrustLedger** is a protocol for making effort visible, trust verifiable, and skills transferable. It uses compact, signed tuples to log who did what, when, and why — without relying on centralized credentials or revealing personal information.

## 📦 Structure

- `chaincode/`: Tools to generate, encode, and reference identity blobs (chaincodes)
- `eventcode/`: Action tuples that link actors, events, intent, and outcomes
- `db/`: Schema files, mapping tables, enums, and registries
- `docs/`: Vision, architecture, format specs, and design thinking
- `poc/`: Proofs of concept and local test utilities

## 📌 Highlights

- 64-byte identity chaincodes
- 32-byte action tuples
- 4-byte hashed references for linking and proof
- Supports offline-first logging and delayed sync
- Enables pseudonymous proof of effort, skill, and presence

## 🧠 Design Philosophy

- Proof of effort > proof of permission
- Trying counts — outcomes just provide context
- Trust is earned by action, not application
- Identity is optional, but reputation is inevitable

## 🛠️ Get Started

```bash
# Create a chaincode from JSON
python3 chaincode/encode_chaincode.py --json jdplumbing.json
```

## 🔒 Security Note

Chaincodes do not store PPID. They are only as identifiable as you choose to make them. Only the 4-byte hash is shared in tuples unless otherwise authorized.

---

Built by plumbers, nerds, and anyone tired of proving themselves to paper.
