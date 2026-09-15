# penstemon_color_images

Image storage for the flower color scoring tool.

Nothing here is source code. These are iNaturalist photos downloaded via GBIF,
mirrored so the scoring page can read pixel values from them, and published to GitHub
Pages so they're served from the same domain as the tool.

## Provenance and licensing

All photos are research-grade iNaturalist observations obtained through GBIF under
CC0, CC BY, or CC BY-NC licenses. Photographer and license for every image are
recorded per observation in `batch_metadata.csv`.
Filenames are GBIF occurrence IDs, which is what links an image to its record,
coordinates, and attribution.

GBIF doi for P. davidsonii set:
https://doi.org/10.15468/dl.46ng67

GBIF doi for P. newberryi set:
https://doi.org/10.15468/dl.kwyerh

## Moving to the next batch

Don't delete anything. Set the new batch number in `fetch_batch.R` and run it.
It downloads only the new images and adds them alongside the existing ones.
`manifest.json` in the website repo controls which images students actually see,
so the older files sit here unused.

Push images before pushing the manifest, or you might get broken images while
Pages deploys.

## Clearing this out

After a few batches this gets large. GitHub Pages has a soft limit of 1 GB for a
published site, and the repo gets slow to clone before that.

When that happens, keep one copy of the images on disk storage, then replace this
repo entirely.