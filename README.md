# Wryko Status

External uptime monitoring for the Wryko platform — [status.wryko.com](https://status.wryko.com).

Runs [Upptime](https://upptime.js.org): GitHub Actions probe the endpoints in
`.upptimerc.yml` every 5 minutes, write results to `history/`, and rebuild the
status site. A failing probe opens an issue labelled `uptime`; recovery closes it.

This lives in its own repository on purpose. Upptime needs only a list of URLs,
not the application source, and Actions minutes are free for public repositories —
so the monitoring can stay public and free while the Wryko source repository is
private.

Probed surfaces are declared in `.upptimerc.yml`. Each must be an externally
routable endpoint whose response actually reflects platform health; do not add a
URL that would stay green while the thing behind it is down.
