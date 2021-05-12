# Hero Banner Demo

Hero banner demo for the blog article that show how well implemented hero banner
could improve LCP and ~~CLS~~ Core Web Vital's metrics

## Running the demo

```shell
docker run -p 8080:80 -v $(pwd):/usr/share/caddy -v $(pwd)/Caddyfile:/etc/caddy/Caddyfile caddy:2.3.0-alpine
```

## Results

All measurements are done on [github.io](https://pixboost.github.io/hero-banner-demo/) version of the page. We measured the performance on
each iteration and tagged the repo, so you can explore changes and results.

Chrome info:

```
Google Chrome	90.0.4430.93 (Official Build) (64-bit)
Revision	4df112c29cfe9a2c69b14195c0275faed4e997a7-refs/branch-heads/4430@{#1348}
OS	Linux
JavaScript	V8 9.0.257.23
User agent	Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.93 Safari/537.36
Command Line	/usr/bin/google-chrome-stable --flag-switches-begin --flag-switches-end --origin-trial-disabled-features=SecurePaymentConfirmation
```

* Network Throttle: Fast 3G
* Disable Cache
* Incognito mode
* Device emulation - Moto G4

Full lighthouse result could be found in [lighthouse.json](lighthouse.json) file.

| Tag                | LCP on Performance Tab (ms) | LCP Lighthouse |
| ------------------ | --------------------------- | -------------- |
| 2-background-image | 7500.8                      | 3.1s           |
