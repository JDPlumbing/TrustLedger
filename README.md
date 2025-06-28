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
# Generate a chaincode from JSON

# 1. Create a descriptor file (example):
cat <<EOF > chaincode/my_entity.json
{
  "entity_type": "person",
  "org_name": "Example Co.",
  "ein": "00-0000000",
  "license": "ABC123",
  "state": "CA",
  "address": "1234 Sample St, Cityville, CA 90210"
}
EOF

# 2. Run the encoder
python3 chaincode/encode_chaincode.py --json chaincode/my_entity.json

```
## 🧩 Submodules

- [`chaincode/`](./chaincode) – Identity encoding + reference hash generator
- [`eventcode/`](./eventcode) – (Coming soon) Tuple generator for actions/events
- [`docs/`](./docs) – Format specs, system architecture


## 🔒 Security Note

Chaincodes do not store PPID. They are only as identifiable as you choose to make them. Only the 4-byte hash is shared in tuples unless otherwise authorized.

---

Built by plumbers, nerds, and anyone tired of proving themselves to paper.
