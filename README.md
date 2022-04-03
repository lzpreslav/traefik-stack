# traefik-stack

Traefik stack used for self-hosting services. Setup towards using with Cloudflare as DNS provider, Let's Encrypt as SSL certificate provider and Google OAuth as authentication for services.

Required ENV vars with their description:

| Var                                                 | Description                                                                                                                                            |
| --------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| CF_DNS_API_TOKEN                                    | Cloudflare API token with DNS:Edit permission for the configured domain                                                                                |
| CF_DOMAIN                                           | Domain/subdomain name which this Traefik instance will be responsible for, e.g. test.myhome.net will be accessible via *.test.myhome.net               |
| CF_EMAIL                                            | Cloudflare email/account name, used for the DNS challenge                                                                                              |
| CF_ZONE_API_TOKEN                                   | Cloudflare API token with Zone:Edit permission for the configured domain                                                                               |
| TRAEFIK_FORWARD_AUTH_COOKIE_DOMAIN                  | Domain to set auth cookie on, can be set multiple times, see [thomseddon/traefik-forward-auth](https://github.com/thomseddon/traefik-forward-auth)     |
| TRAEFIK_FORWARD_AUTH_HOSTNAME                       | Hostname for the Forward Auth provider                                                                                                                 |
| TRAEFIK_FORWARD_AUTH_PROVIDERS_GOOGLE_CLIENT_ID     | Google OAuth Client ID, see [Provider setup](https://github.com/thomseddon/traefik-forward-auth/wiki/Provider-Setup)                                   |
| TRAEFIK_FORWARD_AUTH_PROVIDERS_GOOGLE_CLIENT_SECRET | Google OAuth Client Secret, see [Provider setup](https://github.com/thomseddon/traefik-forward-auth/wiki/Provider-Setup)                               |
| TRAEFIK_FORWARD_AUTH_SECRET                         | Secret used for signing the Forward Auth provider cookie, see [thomseddon/traefik-forward-auth](https://github.com/thomseddon/traefik-forward-auth)    |
| TRAEFIK_FORWARD_AUTH_WHITELIST                      | Only allow given email addresses, can be set multiple times, see [thomseddon/traefik-forward-auth](https://github.com/thomseddon/traefik-forward-auth) |
| TRAEFIK_DASHBOARD_HOSTNAME                          | Hostname for the Traefik dashboard                                                                                                                     |
