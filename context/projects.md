# System Architecture

## Services Overview

| Service | Role | Repo |
|---------|------|------|
| A | ... | repo-A |
| B | ... | repo-B |
| C | ... | repo-C |
| U | upstream — ... | repo-U |
| V | upstream — ... | repo-V |
| W | downstream — ... | repo-W |

## Service Relationships

```
U ──→ A ──→ W
      │
      ↓
      B ──→ C
```

[Describe data flow and dependencies here]

## Cross-Service Conventions

- Communication protocol: [gRPC / REST / Kafka / ...]
- Event naming convention: [e.g. `{service}.{entity}.{action}`]
- Auth between services: [e.g. service tokens, mTLS]
- Shared data ownership rules: [e.g. each service owns its DB, no cross-DB queries]

## Key Constraints

[Anything that affects architectural decisions — SLAs, compliance, legacy systems]
