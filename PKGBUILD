# Maintainer: Eric Bélanger <eric@archlinux.org>

pkgbase=python-pyasn1
pkgname=('python-pyasn1' 'python2-pyasn1')
pkgver=0.2.3
pkgrel=1
arch=('any')
url="http://sourceforge.net/projects/pyasn1/"
license=('BSD')
makedepends=('python-setuptools' 'python2-setuptools')
replaces=('pyasn1')
provides=('pyasn1')
source=(https://pypi.io/packages/source/p/pyasn1/pyasn1-$pkgver.tar.gz)
sha1sums=('e30253a024d1388a96be8e84245a0d38f47467ff')

check() {
  cd pyasn1-${pkgver}
  python2 setup.py test
  python setup.py test
}

package_python-pyasn1() {
  pkgdesc="ASN.1 library for Python 3"
  depends=('python')

  cd pyasn1-${pkgver}
  python setup.py install --root="${pkgdir}"
  install -D -m 644 LICENSE.rst "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}

package_python2-pyasn1() {
  pkgdesc="ASN.1 library for Python 2"
  depends=('python2')

  cd pyasn1-${pkgver}
  python2 setup.py install --root="${pkgdir}"
  install -D -m 644 LICENSE.rst "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
