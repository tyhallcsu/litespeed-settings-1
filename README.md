# litespeed-settings

**Historical sibling of the canonical [tyhallcsu/litespeed-settings](https://github.com/tyhallcsu/litespeed-settings) repository.**
The owner selected that repository as canonical on October 18, 2026. Use its
[setup and behavior guide](https://github.com/tyhallcsu/litespeed-settings/blob/main/README.md)
for new work. This copy remains available for source comparison; no script has
been deleted, replaced or installed by this documentation change.

These are **Lightspeed / Vend POS browser userscripts**, not LiteSpeed web-server
settings. The original repository title above is retained.

## What is preserved here

| File | Relationship to canonical at review |
| --- | --- |
| [litespeed-settings.js](litespeed-settings.js) | Identical, metadata version 1.3 |
| [litespeed-settings.user.js](litespeed-settings.user.js) | Identical, metadata version 1.6 |
| [litespeed-toolbox.js](litespeed-toolbox.js) | Identical, metadata version 3.1 |
| [litespeed-toolbox.user.js](litespeed-toolbox.user.js) | Identical, metadata version 2.0 |
| [new_test.js](new_test.js) | Identical, metadata version 0.6 |
| [new_barcode_test.user.js](new_barcode_test.user.js) | Different experimental variant: metadata 4.3/title 4.1 here, versus 4.5/title 4.4 in canonical |

The canonical repository also contains rewards, ZIP-autofill and redirect helpers
not present here. See its [comparison record](https://github.com/tyhallcsu/litespeed-settings/blob/main/docs/variants.md).
A higher metadata version does not establish that a script works on a current POS.

## Moving future work to canonical

1. Compare the specific file you are changing against canonical.
2. Preserve any unique experimental behavior before proposing a port there.
3. Open future maintenance PRs against canonical unless intentionally documenting
   this historical variant.

Do not enable both repositories' toolbox variants on the same register. They use
overlapping event handlers and browser-storage keys. Existing saved settings and
credentials are untouched; a canonical designation does not migrate or reset them.
Several source headers retain dependency/icon placeholders, and scripts can submit
forms or contact services when enabled. Follow canonical's review-first setup.

## Local validation

```bash
for file in *.js; do
  node --check "$file" || exit 1
done
```

All six files passed syntax checking on October 18, 2026. They were not executed,
installed in a browser or tested against a live POS. Original author headers remain
unchanged; there is no license file and this guide does not supply a license grant.
