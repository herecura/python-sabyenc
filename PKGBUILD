# Maintainer: Ben Ruijl <benruyl@gmail.com>

pkgname=python2-sabyenc
pkgver=4.0.2
pkgrel=1
pkgdesc="Python2 yEnc package optimized for use within SABnzbd"
url="https://github.com/sabnzbd/sabyenc"
arch=('x86_64')
license=("GPL")
depends=("python")
makedepends=("python-setuptools")

source=("https://github.com/sabnzbd/sabyenc/archive/v${pkgver}.tar.gz")
sha512sums=('88e8b47b1438ca55b51dbf8a407c33ec335f0604abf8a3dcbc45853b6dadadf9932d97cf3f0adabd71a9405e2deaeff2777483d9ea692c9d3cbab99dfbfbc901')

build() {
  cd "${srcdir}/sabyenc-${pkgver}"
  python setup.py build
}

package() {
  cd "${srcdir}/sabyenc-${pkgver}"
  python setup.py install --root="${pkgdir}" --optimize=1
}
