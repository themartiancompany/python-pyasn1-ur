# Maintainer: Eric Bélanger <eric@archlinux.org>

pkgbase=python-pyasn1
pkgname=('python-pyasn1' 'python2-pyasn1')
pkgver=0.3.7
pkgrel=1
arch=('any')
url="http://sourceforge.net/projects/pyasn1/"
license=('BSD')
makedepends=('python-setuptools' 'python2-setuptools')
replaces=('pyasn1')
provides=('pyasn1')
source=(https://pypi.io/packages/source/p/pyasn1/pyasn1-$pkgver.tar.gz)
sha512sums=('0f35ca77361ee4913a280a32dfb6720244b2ae3e927620045a5f4879f2d50595e8dd5ec886b707ac76763887c178b0ab95b8a4b5184de83d7e98fe56b7b35c34')

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
