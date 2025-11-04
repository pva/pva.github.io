# Pouch Go Module Archives

Pre-generated archives for packages used in the
[pouch](https://github.com/pva/pouch) Gentoo overlay. It currently hosts
dependency bundles (go-mod directories) for ebuilds using `go-module.eclass`.

All dependency archives are attached as release assets to the single release tagged v1.0.
New or updated archives will be added to this same release over time.

## Usage

Upload dependencies bundle:
```bash
gh release upload v1.0 package-vX.Y.Z-deps.tar.xz
```

Reference a release asset directly in your ebuild, for example:
```bash
SRC_URI="https://github.com/pva/pva.github.io/releases/download/v1.0/${P}-deps.tar.xz"
```

## Notes

* Assets are generated from official upstream Go modules in accordance with
  `go-module.eclass` instructions.
* Verify licenses of all statically linked dependencies (dev-go/lichen helps check).
