# Submitter: Rafael Fontenelle <rafaeff@gnome.org>
# Maintainer: Martin Minka <martin.minka@gmail.com>

_name=jsmin
pkgname=python-jsmin
pkgbase=python-$_name
pkgver=3.0.1
pkgrel=1
pkgdesc="JavaScript minifier"
arch=(any)
url="https://pypi.org/pypi/$_name"
license=('MIT')
depends=('python')
makedepends=('python-setuptools')
source=("https://pypi.org/packages/source/${_name:0:1}/$_name/$_name-$pkgver.tar.gz")
sha256sums=('c0959a121ef94542e807a674142606f7e90214a2b3d1eb17300244bbb5cc2bfc')

build() {
  cd "$srcdir/$_name-$pkgver"
  python setup.py build
}

package() {
  cd "$srcdir/$_name-$pkgver"
  python setup.py install --root="$pkgdir/" --optimize=1 --skip-build
  install -Dm644 LICENSE.txt "$pkgdir/usr/share/licenses/$pkgname/LICENSE.txt"
}
