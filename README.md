# oauth2-proxy-app

Reverse OAuth2 Proxy that handles authentication for GS web frontends.

It is build upon the [oauth2_proxy/oauth2_proxy](https://github.com/oauth2_proxy/oauth2_proxy), with the configuration:

```bash
--cookie-expire=24h0m0s
--cookie-refresh=0h60m0s
--provider=oidc
# Use Auth0 as identity provider
--oidc-issuer-url=https://giantswarm.eu.auth0.com/
--login-url=https://giantswarm.eu.auth0.com/authorize
--redeem-url=https://giantswarm.eu.auth0.com/oauth/token
--validate-url=https://giantswarm.eu.auth0.com/userinfo
```

More options can be found [here](https://github.com/bitly/oauth2_proxy#command-line-options).


## Current supported Services at Giant Swarm:
- Prometheus operator managed Prometheus and Alertmanager
- G8s-Alertmanager
- G8s-Alertmanager-Dashboard

## Add authentication/authorization to a web frontend

1. Add following annotations to the existing ingress:
    ```yaml
    annotations:
    nginx.ingress.kubernetes.io/auth-signin: https://$host/oauth2/start
    nginx.ingress.kubernetes.io/auth-url: https://$host/oauth2/auth
    ```

2. Create a new oauth2 ingress together with the existing ingress
    ```yaml
    apiVersion: extensions/v1beta1
    kind: Ingress
    metadata:
    name: {{ Your.Service.Name }}-oauth2-proxy
    namespace: kube-system
    spec:
    rules:
    - host: {{ Your.Service.URL }}
        http:
        paths:
        - path: /oauth2
            backend:
            serviceName: oauth2-proxy
            servicePort: 4180
    ```
    If SSL is enabled, add the same certificate from the existing ingress, to the oauth2 ingress.

3. Add to Service URL to the list of allowed Callback URLs in [Auth0](https://manage.auth0.com/#/):

    Navigate to the Application `OAuth2-Proxy` and enter the service URL in the
    list of allowed Callback URLs with the following scheme:
    ```
    https://{{ Your.Service.URL }}/oauth2/callback
    ```
    This has to be done for every installation separately.


