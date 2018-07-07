# Contributor: Oleksiy Zakharov <alexzkhr@gmail.com>
pkgname=VC4C
pkgver=0.4.0
pkgrel=5
pkgdesc="Compiler for the VC4CL OpenCL implementation (raspberi-pi)."

provides=('VC4C')
arch=('i686' 'x86_64' 'arm' 'armv6h' 'armv7h' 'aarch64')
url="git://github.com/doe300/VC4C"

license=('MIT')
depends=(llvm clang VC4CLStdLib)
makedepends=(cmake)
source=(git://github.com/doe300/VC4C)        
md5sums=('SKIP')

build() {
  cd $srcdir/VC4C
  cmake -DCMAKE_INSTALL_PREFIX=/usr -DBUILD_DEBUG=OFF -DBUILD_DEB_PACKAGE=OFF
  make
}

package() {
  cd $srcdir/VC4C
  make DESTDIR="$pkgdir/" install  
}
