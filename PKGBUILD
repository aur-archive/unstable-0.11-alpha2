# Maintainer: Carl Mueller  archlinux at carlm e4ward com

pkgname=kdeplasma-applets-publictransport
pkgver=0.11
pkgname=unstable-0.11-alpha2
pkgrel=2
pkgdesc="Plasmoid with departure board for a given stop"
arch=('i686' 'x86_64')
url="http://www.kde-look.org/content/show.php/PublicTransport?content=106175"
license=('GPL')
conflicts=('publictransport-plasmoid')
depends=('kwebkitpart' 'kdebase-workspace')
makedepends=('git' 'cmake' 'automoc4' 'protobuf')
options=()
build() {
  git archive --format=tar --remote=git://anongit.kde.org/publictransport $pkgname > publictransport.tar
  cd $srcdir
  tar xf publictransport.tar
  mkdir build
  cd build
  cmake -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=`kde4-config --prefix` ..
  make 
  make DESTDIR="$pkgdir/" install
}
