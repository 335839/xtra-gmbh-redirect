# xtra-gmbh-redirect

Serves the bare domain **xtra-gmbh.eu** on GitHub Pages and sends every visitor
to the same path on **https://www.xtra-gmbh.eu** (the real site, on Cloudflare
Pages; source in the private `xtragmbh` repo).

The DNS for xtra-gmbh.eu stays at Host Europe (AutoDNS), which has no domain
forwarding, so the apex A records point here instead:

    185.199.108.153
    185.199.109.153
    185.199.110.153
    185.199.111.153

`index.html` and `404.html` are the same page, so any path is forwarded
(`/impressum` → `https://www.xtra-gmbh.eu/impressum`), query string and anchor
included. Without JavaScript it falls back to the www home page.
