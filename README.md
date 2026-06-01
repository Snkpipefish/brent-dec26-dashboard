# Brent Dec-26 (CBZ26) — overvåkingsdashboard

Et lite, statisk dashboard som følger Brent Dec-26-kontrakten (CBZ26) som
inngangssignal i en trade-plan: når Dec-26 fortsetter oppover fra ~$86,
bekrefter markedet at det repriser varigheten av en Hormuz-forstyrrelse.

- **Live:** se GitHub Pages-URL-en for dette repoet.
- `index.html` — selvstendig dashboard (ren JS + inline SVG), leser `dec26_log.js`.
- `dec26_log.js` / `dec26_log.json` — tidsserie-logg, oppdateres av et lokalt
  henteskript (`dec26_monitor.py`) som kjører én gang per handledag og pusher hit.

Tallene hentes fra Barchart + oilprice (kryssjekket). Aldri gjettede priser:
feiler en henting logges N/A med årsak, og dashboardet viser siste gyldige verdi.
