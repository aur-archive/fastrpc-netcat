# Maintainer: Tomas Kral <tomas.kral@gmail.com>
pkgname=fastrpc-netcat
pkgver=0.0.13
pkgrel=3
pkgdesc="(XML|Fast)RPC Python console (which now also supports MySQL)"
arch=("any")
url="http://opensource.seznam.cz/FastRPC-netcat/index.html"
license=("GPL3")
depends=("python2")
makedepends=()
options=()
source=("http://sourceforge.net/projects/fastrpc-netcat/files/fastrpc-netcat/${pkgver}/fastrpc-netcat-${pkgver}.tar.bz2/download" "python2.patch")
md5sums=("990cf3d9b114682256950691a282ed99" "227601e61dc830215c17e1f31d82e78f")



package() {
  cd "$srcdir/$pkgname-$pkgver"
  patch -i ${startdir}/python2.patch
  install -D -m755 fastrpc-netcat "${pkgdir}/usr/bin/fastrpc-netcat"
  install -D -m644 fastrpc-netcat.1 "${pkgdir}/usr/share/man/man1/fastrpc-netcat.1"
}


