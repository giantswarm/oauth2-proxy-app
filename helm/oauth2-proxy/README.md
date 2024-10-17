# oauth2-proxy

![Version: 2.14.2](https://img.shields.io/badge/Version-2.14.2-informational?style=flat-square) ![AppVersion: 7.7.0](https://img.shields.io/badge/AppVersion-7.7.0-informational?style=flat-square)

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
| oauth2Proxy.extraArgs[0] | string | `"--cookie-expire=24h0m0s"` |  |
| oauth2Proxy.extraArgs[10] | string | `"--skip-provider-button=true"` |  |
| oauth2Proxy.extraArgs[1] | string | `"--cookie-name=session"` |  |
| oauth2Proxy.extraArgs[2] | string | `"--cookie-refresh=0h60m0s"` |  |
| oauth2Proxy.extraArgs[3] | string | `"--cookie-secure=true"` |  |
| oauth2Proxy.extraArgs[4] | string | `"--email-domain=*"` |  |
| oauth2Proxy.extraArgs[5] | string | `"--pass-access-token=true"` |  |
| oauth2Proxy.extraArgs[6] | string | `"--pass-authorization-header=true"` |  |
| oauth2Proxy.extraArgs[7] | string | `"--set-authorization-header=true"` |  |
| oauth2Proxy.extraArgs[8] | string | `"--set-xauthrequest=true"` |  |
| oauth2Proxy.extraArgs[9] | string | `"--skip-jwt-bearer-tokens=true"` |  |
| oauth2Proxy.extraEnv | list | `[]` |  |
| oauth2Proxy.providers[0].clientID | string | `""` |  |
| oauth2Proxy.providers[0].clientSecret | string | `""` |  |
| oauth2Proxy.providers[0].cookieSecret | string | `""` |  |
| oauth2Proxy.providers[0].extraArgs | list | `[]` |  |
| oauth2Proxy.providers[0].extraEnv | list | `[]` |  |
| oauth2Proxy.providers[0].id | string | `"default"` |  |
| oauth2Proxy.providers[0].provider | string | `"oidc"` |  |
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

