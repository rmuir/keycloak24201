# Repro for keycloak LDAP bug

This is a reproducer for https://github.com/keycloak/keycloak/issues/24201

## How to reproduce

clone this repo, then `docker-compose up`.

## How it works

It brings up a Samba AD, then keycloak.

After both are healthy, then ansible playbook runs that:
1. creates an LDAP user federation
2. adds a test user
3. attempts to disable said test user: FAILS
