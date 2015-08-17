# Contributor: Daniel Strandberg <esodax!nospam!@gmail.com>

_relname=pyliblzma
pkgname=python-$_relname
pkgver=0.5.3
pkgrel=3
pkgdesc='Python bindings for liblzma'
arch=('i686' 'x86_64')
url='http://pypi.python.org/pypi/pyliblzma'
license=('LGPL3')
depends=('python2' 'xz')
makedepends=('python2-distribute')
source=(http://pypi.python.org/packages/source/p/$_relname/$_relname-$pkgver.tar.bz2)
md5sums=('500f61116ee1ab4063b49c121786863a')

build() {
  cd $srcdir/$_relname-$pkgver
  python2 setup.py build || return 1
  python2 setup.py clean
}

package() {
  cd $srcdir/$_relname-$pkgver
  python2 setup.py install --root=$pkgdir --prefix=/usr || return 1
}

# vim:ts=2:sw=2:et:
