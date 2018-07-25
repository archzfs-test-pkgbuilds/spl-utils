# Maintainer: Jan Houben <jan@nexttrex.de>
# Contributor: Jesus Alvarez <jeezusjr at gmail dot com>
#
# This PKGBUILD was generated by the archzfs build scripts located at
#
# http://github.com/archzfs/archzfs
#
pkgname="spl-utils-common"

pkgver=0.7.9
pkgrel=2
pkgdesc="Solaris Porting Layer kernel module support files."
arch=("x86_64")
url="http://zfsonlinux.org/"
source=("https://github.com/zfsonlinux/zfs/releases/download/zfs-0.7.9/spl-0.7.9.tar.gz")
sha256sums=("49832e446a5abce0b55ba245c9b5f94959604d44378320fdffae0233bf1e8c00")
groups=("archzfs-linux")
license=("GPL")
provides=("spl-utils")
makedepends=()
conflicts=('spl-utils-common-git' 'spl-utils-linux-git' 'spl-utils-linux' 'spl-utils-linux-lts' 'spl-utils-linux-lts-git')
replaces=("spl-utils-linux", "spl-utils-linux-lts")

build() {
    cd "${srcdir}/spl-0.7.9"
    ./autogen.sh
    ./configure --prefix=/usr --libdir=/usr/lib --sbindir=/usr/bin --with-config=user
    make
}

package() {
    cd "${srcdir}/spl-0.7.9"
    make DESTDIR="${pkgdir}" install
}
