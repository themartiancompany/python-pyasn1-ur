# Maintainer: Eric Bélanger <eric@archlinux.org>
# Contributor: Jesse Young <com gmail jesse.young>

pkgbase=python-pyasn1
pkgname=('python-pyasn1' 'python2-pyasn1')
pkgver=0.1.2
pkgrel=3
arch=('any')
url="http://sourceforge.net/projects/pyasn1/"
license=('BSD')
makedepends=('python-distribute' 'python2-distribute')
replaces=('pyasn1')
provides=('pyasn1')
source=(http://downloads.sourceforge.net/sourceforge/pyasn1/pyasn1-${pkgver}.tar.gz)
sha1sums=('4438226c5d38db582442241fc574a2001b685613')

package_python-pyasn1() {
  pkgdesc="ASN.1 library for Python 3"
  depends=('python')

  cd "${srcdir}/pyasn1-${pkgver}"
  python setup.py install --root="${pkgdir}"
  install -D -m 644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}

package_python2-pyasn1() {
  pkgdesc="ASN.1 library for Python 2"
  depends=('python2')

  cd "${srcdir}/pyasn1-${pkgver}"
  python2 setup.py install --root="${pkgdir}"
  install -D -m 644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
