# Maintainer: Jesse Spangenberger <azulephoenix at gmail.com>

pkgname=xen-tools
pkgver=4.3.1
pkgrel=4
_pkgrel=1
arch=('i686' 'x86_64')
pkgdesc="xen-tools is a collection of simple perl scripts which allow you to easily create new guest Xen domains"
license=('GPL')
url="http://www.xen-tools.org/software/xen-tools/"
conficts=('xen-tools-git')
provides=('xen-tools')
depends=('perl-file-slurp' 'perl-text-template' 'perl-config-ini') 
source=("http://ftp.us.debian.org/debian/pool/main/x/xen-tools/xen-tools_4.3.1-1_all.deb")
md5sums=('2d4f4d6479820fc91821fb45a32e2fc5')

prepare() {
  install -dm755 ${srcdir}/data
  
  ar x ${pkgname}_${pkgver}-${_pkgrel}_all.deb
  tar xzf data.tar.gz -C ${srcdir}/data
}

package() {
  install -dm755 ${pkgdir}/{etc,usr}
  
  cp -r ${srcdir}/data/* ${pkgdir}/
}
