pkgname=kfoldersync
pkgver=3.1.2
pkgrel=1
pkgdesc="Folder synchronization and backup tool for KDE"
arch=('x86_64')
url='http://kde-apps.org/content/show.php/KFolderSync?content=164092'
license=('GPL')
makedepends=('cmake' 'extra-cmake-modules')
source=("http://kde-apps.org/CONTENT/content-files/164092-${pkgname}-${pkgver}.tar.xz")
md5sums=('74ab8ed87c586bde9b5fd34b617d09e6')


prepare() {
    cd "${pkgname}-${pkgver}"
    mkdir build
}

build() {
    cd "${pkgname}-${pkgver}/build"
    cmake -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_BUILD_TYPE=Release ..
    make
}

package() {
    cd "${pkgname}-${pkgver}/build"
    make DESTDIR="${pkgdir}/" install
}
