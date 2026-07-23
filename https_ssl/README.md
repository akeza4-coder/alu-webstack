# HTTPS SSL

Securing the web stack traffic: DNS records for the domain's subdomains, SSL termination on HAProxy (lb-01) with a Let's Encrypt certificate obtained via certbot, and a forced redirect from HTTP to HTTPS.

## Tasks

* **0-world_wide_web** — Bash script that audits DNS A records for a domain's subdomains (`www`, `lb-01`, `web-01`, `web-02`) using `dig` and `awk`. Accepts a mandatory `domain` argument and an optional `subdomain` argument.
* **1-haproxy_ssl_termination** — HAproxy configuration file configured to handle SSL termination on port 443.
* **2-redirect_http_to_https** — HAproxy configuration file configured to return a 301 redirect for unencrypted HTTP traffic to HTTPS.
