# Maintainer: Anuj More <anujmorex@gmail.com>

pkgname=navicat-premium
pkgver=11.0.17
_pkgver=${pkgver%.*}
pkgrel=1
pkgdesc="A fast, reliable and affordable Database Administration tool purpose-built for simplifying database management and reducing administration costs."
url="http://www.navicat.com"
license=('custom')
arch=('any')
source=(http://download.navicat.com/download/navicat110_premium_en.tar.gz
        navicat.desktop
        navicat)
md5sums=('494a2988afa10a531731f225f62e40c6'
         '1bb01bb9a6f5850ecdf019ce61dea63d'
         'a7f10a4d9c2c3901829c35c5bf9aae97')

build() {
  mkdir -p ${pkgdir}/opt/navicat
  mkdir -p ${pkgdir}/usr/bin
  mkdir -p ${pkgdir}/usr/share/applications
  cp -R ${srcdir}/navicat${_pkgver/./}_premium_en/* ${pkgdir}/opt/navicat/
  cp ${srcdir}/navicat ${pkgdir}/usr/bin/
  chmod +x ${pkgdir}/usr/bin/navicat
  cp ${srcdir}/navicat.desktop ${pkgdir}/usr/share/applications/
}
