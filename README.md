# prvis-ai — step-ca (PKI)

Stripped step-ca for prvis-ai. Private CA with ACME, SSH certs, SCEP for MDM enrollment, Keycloak OIDC.

## What was removed
- examples, debian packaging, test suite, build scripts, contrib docs

## What was added
- `prvis/ca.json` — prvis CA config with ACME + SSHPOP + SCEP (FleetDM) + OIDC (Keycloak)
- `prvis/docker-compose.yml` — 256M RAM limit, agent-network

## Provisioners
- ACME — for services to auto-renew TLS certs
- SSHPOP — SSH certificate authority for deploy-vm and Hetzner
- SCEP — MDM device certificate enrollment via FleetDM
- OIDC (Keycloak) — user certificate issuance after SSO login

## Resource requirements
- 256M RAM, 0.25 CPU — very lightweight
