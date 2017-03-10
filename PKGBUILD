# $Id$
# Maintainer: Frede Hundewadt <fh@uex.dk>

pkgname=manjaro-appstream-data-unstable-dev
pkgver=20$(date +%y%m%d)
pkgrel=1
pkgdesc="Manjaro Linux application database for AppStream-based software centers"
arch=(any)
url="http://www.manjaro.org"
license=(GPL)
depends=()
makedepends=()
source=(https://www.uex.dk/repos/appstream/manjaro/unstable/manjaro-{core,extra,community,multilib}.xml.gz
        https://www.uex.dk/repos/appstream/manjaro/unstable/manjaro-{core,extra,community,multilib}-icons.tar.gz)
noextract=(manjaro-{core,extra,community,multilib}.xml.gz manjaro-{core,extra,community,multilib}-icons.tar.gz)
package() {
  mkdir -p "$pkgdir"/usr/share/app-info/{icons/manjaro-{core,extra,community,multilib},xmls}
  for _repo in core extra community multilib; do
   tar -xzf manjaro-$_repo-icons.tar.gz -C "$pkgdir"/usr/share/app-info/icons/manjaro-$_repo/
  done
  cp *.xml.gz "$pkgdir"/usr/share/app-info/xmls/
}
md5sums=('ae2926a4de104a4f220127a62acba0d4'
         'e8c0e9ae4a2c67a48df566eab5b567ef'
         'a426eebcadbb04389b4d5812c2831391'
         'ae2926a4de104a4f220127a62acba0d4'
         'a6c2a2fcfca2e50e4006ae12294e2fb0'
         'a6c2a2fcfca2e50e4006ae12294e2fb0'
         'a6c2a2fcfca2e50e4006ae12294e2fb0'
         'a6c2a2fcfca2e50e4006ae12294e2fb0')
