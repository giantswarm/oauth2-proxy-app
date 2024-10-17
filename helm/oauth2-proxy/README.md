# oauth2-proxy

![Version: 2.14.1](https://img.shields.io/badge/Version-2.14.1-informational?style=flat-square) ![AppVersion: 7.7.0](https://img.shields.io/badge/AppVersion-7.7.0-informational?style=flat-square)

A reverse proxy that provides authentication with Google, Azure, OpenID Connect and many more identity providers

**Homepage:** <https://github.com/giantswarm/oauth2-proxy-app>

## Source Code

* <https://github.com/oauth2-proxy/oauth2-proxy>

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| containerSecurityContext.readOnlyRootFilesystem | bool | `true` |  |
| containerSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| global.podSecurityStandards.enforced | bool | `false` |  |
| ingress.certSecretName | string | `"oauth2-proxy"` |  |
| ingress.enabled | bool | `false` |  |
| ingress.extraAnnotations | object | `{}` |  |
| ingress.hosts | list | `[]` |  |
| ingress.ingressClassName | string | `"nginx"` |  |
| ingress.letsencrypt.enabled | bool | `true` |  |
| ingress.tls.enabled | bool | `true` |  |
| oauth2Proxy.extraArgs | list | `[]` |  |
| oauth2Proxy.extraEnv | list | `[]` |  |
| oauth2Proxy.providers[0].clientID | string | `""` |  |
| oauth2Proxy.providers[0].clientSecret | string | `""` |  |
| oauth2Proxy.providers[0].cookie.expiry | string | `"24h0m0s"` |  |
| oauth2Proxy.providers[0].cookie.name | string | `"SESSION"` |  |
| oauth2Proxy.providers[0].cookie.refresh | string | `"0h60m0s"` |  |
| oauth2Proxy.providers[0].cookie.secret | string | `""` |  |
| oauth2Proxy.providers[0].emailDomain | string | `"*"` |  |
| oauth2Proxy.providers[0].extraArgs | list | `[]` |  |
| oauth2Proxy.providers[0].extraEnv | list | `[]` |  |
| oauth2Proxy.providers[0].id | string | `"default"` |  |
| oauth2Proxy.providers[0].oidc.issuerURL | string | `""` |  |
| oauth2Proxy.providers[0].oidc.loginURL | string | `""` |  |
| oauth2Proxy.providers[0].oidc.profileURL | string | `""` |  |
| oauth2Proxy.providers[0].oidc.redeemURL | string | `""` |  |
| oauth2Proxy.providers[0].oidc.validateURL | string | `""` |  |
| oauth2Proxy.providers[0].passAccessToken | bool | `true` |  |
| oauth2Proxy.providers[0].passAuthorizationHeader | bool | `true` |  |
| oauth2Proxy.providers[0].provider | string | `"oidc"` |  |
| oauth2Proxy.providers[0].setAuthorizationHeader | bool | `true` |  |
| oauth2Proxy.providers[0].setXAuthRequest | bool | `true` |  |
| oauth2Proxy.providers[0].skipJwtBearerTokens | bool | `true` |  |
| oauth2Proxy.providers[0].skipProviderButton | bool | `true` |  |
| oauth2Proxy.providers[0].upstream | string | `""` |  |
| podSecurityContext.runAsGroup | int | `1000` |  |
| podSecurityContext.runAsNonRoot | bool | `true` |  |
| podSecurityContext.runAsUser | int | `1000` |  |
| podSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| port.name | string | `"oauth2-proxy"` |  |
| port.port | int | `4180` |  |
| registry.domain | string | `"gsoci.azurecr.io"` |  |
| serviceMonitor.enabled | bool | `true` |  |
| serviceMonitor.interval | duration | `"60s"` | Prometheus scrape interval. |
| serviceMonitor.scrapeTimeout | duration | `"45s"` | Prometheus scrape timeout. |

