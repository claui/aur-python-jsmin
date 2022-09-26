# Submitter: Rafael Fontenelle <rafaeff@gnome.org>
# Maintainer: Martin Minka <martin.minka@gmail.com>

_name=jsmin
pkgname=python-jsmin
pkgbase=python-$_name
pkgver=3.0.0
pkgrel=2
pkgdesc="JavaScript minifier"
arch=(any)
url="https://pypi.org/pypi/$_name"
license=('MIT')
depends=('python')
makedepends=('python-setuptools')
source=("https://pypi.org/packages/source/${_name:0:1}/$_name/$_name-$pkgver.tar.gz")
sha256sums=('88fc1bd6033a47c5911dbcada7d279c7a8b7ad0841909590f6a742c20c4d2e08')

build() {
  cd "$srcdir/$_name-$pkgver"
  python setup.py build
}

package() {
  cd "$srcdir/$_name-$pkgver"
  python setup.py install --root="$pkgdir/" --optimize=1 --skip-build
  install -Dm644 LICENSE.txt "$pkgdir/usr/share/licenses/$pkgname/LICENSE.txt"
}
