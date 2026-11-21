# TenantSwarm.ai

**Containment for AI agent swarms.** Memory access is a capability an agent holds, not a property of where the data lives.

[![HyperBus, how it works](profile/hyperbus-motion-poster.jpg)](profile/hyperbus-motion.mp4)

*A 40-second explainer. Click the picture to watch it, or [read the script](profile/script.md).*

## How HyperBus contains a swarm

- **Tenants are walled off.** Each tenant's memory is separate.
- **Memory is cut into regions, and the region lives in the storage key.** An agent cannot even name a region it was not granted.
- **Each agent holds explicit grants:** READ, WRITE, or nothing.
- **The engine holds the database credentials** and verifies every caller. Denied requests fail closed.

When one agent is compromised, the blast radius ends at its grants.

## Public code

- [hyperbus-runtime](https://github.com/TenantSwarm-ai/hyperbus-runtime): process isolation and agent identity binding for HyperBus deployments.
