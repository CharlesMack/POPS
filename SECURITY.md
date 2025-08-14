# P.O.P.S. Security Overview

Security is non-negotiable. Here’s how P.O.P.S. safeguards integrity, privacy, and trust—designed for air-gapped and offline-first environments.

## 1. Threat Mitigation

### Tampering & Integrity
- All AppDrops and binaries validated via cryptographic hashes  
- Mirror repos must provide signed logs; emulator verifies origin

### Model Poisoning & Trust
- Roger’s models are sandboxed and immutable—no untrusted third-party bundles allowed  
- Model changes are version-controlled and auditable

### Auditability & Logging
- Every user interaction (thread, prompt, UI state) is logged locally  
- Mirror logs with Git-like history for transparency and inspection

## 2. Offline & Air-Gapped Resilience
- No hidden cloud callbacks, telemetry, or external pings by default:contentReference[oaicite:6]{index=6}  
- All inference and decision-making happens locally  
- Bodies of logs stay on device unless intuitively shared

## 3. Sync & Verification
- Mirrors must provide trust anchors and verify content before activation  
- Emulator enforces sandbox policy—only validated bundles run

## 4. User-Controlled Privacy
- Data stays local unless explicitly shared by the user  
- Remote wipe via signed garbage collection commands supported

## 5. Published Audit Logs
- Example logs live in `security/audit-examples/`, tracking:
  - Launch requests
  - Emulator verifications
  - Sync events

## 6. Staying Transparent
- Security docs evolve openly—trust is built via clarity, not opacity  
- Contributions and audits welcome

Safe, verifiable, yours.
