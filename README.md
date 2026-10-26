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

The package is advertised for PixInsight 1.9.4–1.9.5 (any revision/build) and
is unsigned. Installation and execution have been verified locally on 1.9.5;
the 1.9.4 installation and script behavior still need a user-side test.
**Signature: Unavailable** is therefore expected. PixInsight must permit
unsigned update repositories in its security preferences. PixInsight bundles
its repository specification at `doc/docs/PIRepositoryReference/PIRepositoryReference.html`
relative to the installation directory.

If the repository description appears but **Available packages** is zero,
check **Help > About PixInsight** for the version, then **Resources > Updates >
View Installed Updates** for an existing 0.1.4 installation. PixInsight does
not offer a package twice. Run **Check for Updates** again after changing the
repository or updating PixInsight. If the version is 1.9.5, 0.1.4 is not
installed, and unsigned repositories are permitted, send the exact update
console/log message to the maintainer.
