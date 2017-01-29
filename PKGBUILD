pkgname=kfoldersync
pkgver=3.4.1
pkgrel=1
pkgdesc="Folder synchronization and backup tool for KDE"
arch=('x86_64')
url="https://www.linux-apps.com/content/show.php/KFolderSync?content=164092"
license=('GPL')
depends=('kcoreaddons' 'kdbusaddons' 'ki18n' 'kio' 'knotifications' 'kxmlgui' 'hicolor-icon-theme')
makedepends=('cmake' 'extra-cmake-modules' 'gettext')
source=("https://dl.opendesktop.org/api/files/download/id/1485353737/${pkgname}-${pkgver}.tar.xz")
md5sums=('33e049d7065cb27382eb7bcb6432b41b')

build() {
    mkdir -p build
    cd build
    cmake ../${pkgname}-${pkgver} \
          -DCMAKE_INSTALL_PREFIX=/usr \
          -DCMAKE_BUILD_TYPE=Release
    make
}

package() {
    cd "${srcdir}/build"
    make DESTDIR="${pkgdir}/" install
}