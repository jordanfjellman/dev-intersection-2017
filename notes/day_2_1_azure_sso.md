# Azure AD SSO Deep Dive

- Tim Warner
- Slides - http://timw.info/itt

## Password Syncronization

Basic password sync is a primary consideration when picking structure.

- Tool -> IdFix
    - Will look for duplicates, or other hangups with sync, and the options to correct errors.

## Federated Identity

- http://timw.info/adcon

Only _true_ on SSO.
Authenticated locally only, then the SAAS application trusts the AD on premesis.

- Federated Identity Architecture - http://timw.info/adfsarch

- AD FS SSO Example - http://timw.info/sso2

## Third-Party IdP Options

Most are open source, with paid support tiers (e.g. Red Hat).

- OpenID Connect/OAuth 2.0
- IdentityServer
- Shibboleth
- WS02
- Octa (given by person in class)

## Connect Windows 10 Directly to Azure

With a combination of In-Tune, this may allow you to connect directly to azure