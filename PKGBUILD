pkgname=kfoldersync
pkgver=3.0.0
pkgrel=1
pkgdesc="Folder synchronization and backup tool for KDE"
arch=('x86_64')
url='http://kde-apps.org/content/show.php/KFolderSync?content=164092'
license=('GPL')
makedepends=('cmake' 'extra-cmake-modules')
source=("http://kde-apps.org/CONTENT/content-files/164092-${pkgname}-${pkgver}.tar.xz")
sha512sums=('7b9030fb34b50cea2972b3d2cbdbe0c6db74d62430a8a47c2056897bb3c763187155e11a853f71d8053585db005fb036cb9a7077564c8f151a67f8e7ccdc2370')

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
