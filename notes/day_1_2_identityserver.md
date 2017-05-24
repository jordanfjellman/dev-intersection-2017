# Securing Web Apps with IdentityServer

- Bian Noyes
- Slides -> http://noyes.me/devint2017-ids

## Authentication Overview

Cookie based authentication is not Token based authentication.

Token based Authentication (STS)

### Protocals

- OAuth2
    - Just about authorization
    - Issued access token after used is authenticated "somehow"
- OpenID Connect
    - Builds on OAuth2
    - Just about authentication
    - Issed id token after presenting valid credentials 

### Terms

- Client - application requesting access to a Resource
- Resource/Relying Party - a secured API/app that client wants to call
- Resource Owner - end user using the client
- Scope - a named resource that is needed for
- Identity Provider(IDP)/STS/SSO Server/Authentication Server/Authorization Server
    - App that manages identities, authenticates users, returns ID and Access tokens for use by client
    - IdentityServer, Azure AD, ADFS, Domain Controller, Auth0 server
- JWT ("Jawt") toek format used for OpenID Connect and 0Auth2

## IdentityServer

- v4 Must be on .net core STS, v3 can be .net 4.x or core

Microsoft even recommends this as the Go-To tech for multiple clients.

## Setup

## Securing API 

## Securing App

