# Maintainer: Drew Abbott <abbotta4@gmail.com>
# Contributor: Drew Abbott <abbotta4@gmail.com>

pkgname=beets-beetfs
_pkgname=beetfs
pkgver=0.10.1
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

sha256sums=('429ea41722448d543d2215b4c4d524a97f780446361a4df6d5057675861f54be')

package() {
  packagesDir="$(python -c 'import site; print(site.getsitepackages()[0])')"
  cd "${srcdir}/${_pkgname}-${pkgver}"
  install -Dm 644 beetsplug/beetfs.py -t ${pkgdir}${packagesDir}/beetsplug
}
