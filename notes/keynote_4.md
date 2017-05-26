# Angular Applications: Large Scale, Across Large Teams, with Large Results

- Stephen Fluin (@stephenfluin)

## PWA (Progressive Web Application)

ServiceWorker Proxies Requests

- Grants reliability for offline and usable connections
- Push Notifications
- Add to homescreen (app-like experiance)

## Cross Platform

- Tool -> Electron (installed like an .exe or .dmg)


## Things to like

1. Opinionated
    - reactive by nature

```
let data = http.get('/my/api').map(res => res.json()).startsWith(cachedData);
```

    - databases (less opinionated)
        - GraphQL

2. Trustworthy
    - SemVer
    - Predictable Release Cadence
3. Familiar
4. Ecosystem
5. Scaled

## Upgrade to Angular from AngularJS

- Tool -> ngUpgrade
