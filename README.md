# Token Radar (token-radar-01)

A pre-token protocol radar for the make.fun token-radar-01 bounty.

`main.ts` (Node 22, standard library only) reads `/input/snapshot.json`, scores every
pre-token protocol with the model in `lib/model.ts`, writes the ranked board to
`/output/board.json`, writes `data.js` for the static dashboard, copies `dashboard/`
and `screenshots/` to `/output`, and writes `/output/dossier.json` with `buildDossier`
from `vendor/makefun-board.ts`.

Run locally: `mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts --input ../input/snapshot.json`

The dashboard is a static dark-themed page (no framework, no network) that renders the
ranked board, category/chain filters, sortable columns, and a per-protocol detail view
with the model's inputs and the farm plan.

SPDX-License-Identifier: MIT
