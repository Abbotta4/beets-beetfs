# Maintainer: Drew Abbott <abbotta4@gmail.com>
# Contributor: Drew Abbott <abbotta4@gmail.com>

pkgname=beets-beetfs
_pkgname=beetfs
pkgver=0.8.0
pkgrel=1
pkgdesc='A beets plugin for mounting a FUSE filesystem of audio items'
arch=(any)
url=https://github.com/abbotta4/beetfs
license=(MIT)
depends=(
  beets
  python-pyfuse3
)
source=(
  https://github.com/Abbotta4/beetfs/archive/refs/tags/v${pkgver}.tar.gz
)

sha256sums=('43d033d91e6b4901f553cff472fb01de355e6bbdac14d27a2b1a7a3ff703e83f')

package() {
  packagesDir="$(python -c 'import site; print(site.getsitepackages()[0])')"
  cd "${srcdir}/${_pkgname}-${pkgver}"
  install -Dm 644 beetsplug/beetfs.py -t ${pkgdir}${packagesDir}/beetsplug
}