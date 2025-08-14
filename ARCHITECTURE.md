# P.O.P.S. Architecture Overview

P.O.P.S. (One Page Center) is designed as a modular, offline-first AI ecosystem with a decentralized supply chain. Here's a bird’s-eye view to guide newcomers and contributors alike.

## 1. Purpose & Scope
- Enable rapid, offline-capable AI UI with panels, assistant, and caching  
- Resilient across devices—from a bootable USB to a hybrid edge mesh network  
- Integrates AI (Roger), cache (Snake Eyes), emulator, and content (AppDrops)

## 2. High-Level Module Map
POPS/
├── core/
├── network/
├── cache/
├── panels/
├── roger/
├── appdrops/
├── cdn/
├── themes/
└── index.html


## 3. Key Components

- **core/**  
  Underpins the system: emulator, panel parsing, storage logic

- **network/**  
  Handles P2P sync, GitHub mirrors, IPFS fallback

- **cache/**  
  Manages hot/warm/cold data lifecycle: fast access and eviction logic

- **panels/**  
  UI modules for Scroll Catalog, browser, favorites, etc.

- **roger/**  
  Local assistant: intent parsing, suggestions, fallback strategies

- **appdrops/**  
  Bundles (JSON/WASM/HTML) representing installable units

- **cdn/**  
  Mirror list, prioritized edge sources

- **themes/**  
  Visual overlays: flat, quantum, minimal

- **index.html**  
  Bootstraps offline execution—ideal for USB or SD environments

## 4. Offline-First Data Flow
- UI reads entirely from local cache  
- Request → Snake Eyes → Core → Emulator → AppDrop  
- If offline: fallback to warm/cold cache or queued queue for sync when online:contentReference[oaicite:2]{index=2}

## 5. Sync & Conflict Resolution
- **Hot Sync**: immediate local updates, queued for sync  
- **Warm Sync**: staged for later bundling  
- **Cold Sync**: archive log and historical replay  
- Conflict resolution via oldest-timestamp-wins or user-driven merge

## 6. Security & Trust
- Emulator performs pre-launch hash validation—like Git integrity  
- Every AppDrop is signed, sandboxed, and verified
- Roger’s models are hardened, local, and audited regularly:contentReference[oaicite:3]{index=3}

## 7. Architecture Philosophy
- Keep architecture docs high-level and stable, not source-detailed:contentReference[oaicite:4]{index=4}  
- Focus on component relationships, module intents, and owner mapping

## 8. How to Explore
- Drill in per-directory for functionality maps  
- Use mermaid or UML visuals if desired  
- Prioritize clarity over exhaustiveness

This is your map—let it guide you.
