# IPNS-Link frontdesk

1. A free domain name and hosting: https://ipns-link.herokuapp.com
2. Path-based. Has no subdomains.
3. Redirects requests with paths : `/ipns/*`, `/ipfs/*` and `/?ipns-link-gateway=<keyID or dnslink or *.ipns>/*` to subdomain IPNS-Link-gateways selected randomly from the curated list in https://github.com/ipns-link/gateway-registry.
4. Advantage: Gateway owners can afford to let old domain names expire and buy new cheap domain names.
5. Checks whether the destination gateway is up with a HEAD request before redirecting. If it is down, creates an issue in the https://github.com/ipns-link/gateway-registry repo.