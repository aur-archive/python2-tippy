# Maintainer: TDY <tdy@archlinux.info>

pkgname=python2-tippy
pkgver=0.1
pkgrel=1
pkgdesc="Toolbox for Image Processing in PYthon (based on OpenCV)"
arch=('any')
url="https://pypi.python.org/pypi/Tippy"
license=('BSD')
depends=('python2' 'opencv')
source=(https://pypi.python.org/packages/source/T/Tippy/Tippy-$pkgver.tar.gz)
sha256sums=('617297d0b6c8c22be4b64eab9c6c1af964adc40299702de01b27d3f0a541c1b8')

build() {
  cd "$srcdir/Tippy-$pkgver"
  python2 setup.py build
}

package() {
  cd "$srcdir/Tippy-$pkgver"
  python2 setup.py install --root="$pkgdir/" --optimize=1
  install -Dm644 LICENSE.txt "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

# vim:set ts=2 sw=2 et:
