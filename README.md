Docker Compose stack to help testing OIDC scenarios in Synapse.

This deploys:

 - two Element Web, one on <http://localhost:8081/>, the other on <http://localhost:8082/>
 - a PG database for Keycloak
 - a Keycloak instance on <http://localhost:8080>. Admin credentials: `admin` / `admin`

Keycloak can access the host via `host.docker.internal`, so whenever Keycloak needs direct access to Synapse (like when sending OIDC Back-Channel Logout tokens) it should use that address.
