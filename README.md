# Spatially Robust LRGB PixInsight updates

This public repository contains only the PixInsight update manifest and the
versioned installation ZIP. The ZIP includes the JavaScript script installed at
`src/scripts/SpatiallyRobustLRGB/astro_lrgb.js`. No image data is distributed.

Add this repository URL in PixInsight under **Resources > Updates > Manage
Repositories**, then **Check for Updates**, apply, and restart:

```text
https://raw.githubusercontent.com/mburge/spatially-robust-lrgb-updates/main/
```

Current version: **0.1.4**. The dialog offers the original D65 Y reference
and an experimental filter/QE projection read from the selected views' RGB
SPCC and L SPFC histories. The latter now displays the recorded SPCC RGB
white-balance factors read-only and adjusts its response weights for those
factors, assuming PI applied them as channel multipliers. It remains
experimental and does not reverse background neutralization. Both choices
create linear matched-L and RGB blend views; D65 remains the default.
Version 0.1.2 also corrects the installed script's ZIP permissions so a normal
PixInsight session can read it after a privileged macOS update.

The package targets PixInsight 1.9.5 and is unsigned. See PixInsight's
[update repository specification](https://pixinsight.com/doc/docs/PIRepositoryReference/PIRepositoryReference.html).
