# Québec French — audio pack, second host

The web app downloads its pronunciation pack from GitHub Pages in ≤90 MB parts, listed in
`audio-<voice>.bin.parts.json`. A Pages site may publish at most 1 GB, and the pack is
outgrowing the first site (`mortal-dog/quebec-french-audio`, served at
`https://french.doctornova.net/`). This repository serves the parts that do not fit there,
from `site/audio/`, at:

    https://mortal-dog.github.io/quebec-french-audio-2/audio/

The parts manifest stays on the first site. Each part it lists carries a `url` when it lives
somewhere other than beside the manifest, so the app needs no second setting. Which parts go
where is decided by `pnpm split:pack` in the app repo (`scripts/tts/split-pack.mjs`).

> ⚠️ **This repository keeps exactly one commit**, like the first one: the parts are binary
> and change wholesale with every pack. Record work with `pnpm git:squash`.

Two limits, per site: 1 GB published, and a soft 100 GB/month of bandwidth.
