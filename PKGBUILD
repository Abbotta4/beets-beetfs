# Maintainer: Drew Abbott <abbotta4@gmail.com>
# Contributor: Drew Abbott <abbotta4@gmail.com>

pkgname=beets-beetfs
_pkgname=beetfs
pkgver=0.9.2
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

sha256sums=('3dd284002b2590e78072b96ce5f3fb7754e3f995f1efa44a0a8010f5c0a62210')

package() {
  packagesDir="$(python -c 'import site; print(site.getsitepackages()[0])')"
  cd "${srcdir}/${_pkgname}-${pkgver}"
  install -Dm 644 beetsplug/beetfs.py -t ${pkgdir}${packagesDir}/beetsplug
}
