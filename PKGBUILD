# $Id$
# Maintainer: Oliver Bestwalter <oliver@bestwalter.de>
pkgname=i3configger
pkgver=0.7.1
pkgrel=2
pkgdesc='i3 config manipulation tool'
arch=('any')
url='http://oliver.bestwalter.de/i3configger/'
makedepends=('python' 'python-setuptools')
# python-docutils is a actually python-daemon dependency (bug already filed)
depends=('python' 'python-setuptools' 'python-psutil' 'python-daemon' 'python-docutils')
license=('MIT')
source=("https://pypi.io/packages/source/i/i3configger/i3configger-${pkgver}.tar.gz")
sha256sums=('d06819771438d48966ad7c138dc3332b4edeffd432956d8ae4f71873629183bf')

package() {
    cd "$srcdir"/i3configger-$pkgver
    python setup.py install --prefix=/usr --root="$pkgdir" --optimize=1
    install -D -m644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
