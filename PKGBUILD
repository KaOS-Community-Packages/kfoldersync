pkgname=kfoldersync
pkgver=3.1.4
pkgrel=1
pkgdesc="Folder synchronization and backup tool for KDE"
arch=('x86_64')
url='http://kde-apps.org/content/show.php/KFolderSync?content=164092'
license=('GPL')
depends=('kcoreaddons' 'kdbusaddons' 'ki18n' 'kio' 'knotifications' 'kxmlgui' 'hicolor-icon-theme')
makedepends=('cmake' 'extra-cmake-modules' 'gettext')
source=("http://kde-apps.org/CONTENT/content-files/164092-${pkgname}-${pkgver}.tar.xz")
md5sums=('de588dd3ad633b1531252a126aa0c9d9')


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
