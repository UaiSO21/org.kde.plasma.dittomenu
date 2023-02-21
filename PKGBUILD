# Maintainer: Maurício de Lima <mauriciodelima.mol@gmail.com>

pkgname=org.kde.plasma.dittomenu
_gitname=dittoMenuKDE
pkgver=$(date +%y.%m.%d)
pkgrel=$(date +%H%M)
pkgdesc="Menu de programas do UaiSO"
arch=('any')
url="https://github.com/adhec/dittoMenuKDE"
license=('GPL3')
depends=()
conflicts=('org.kde.plasma.dittomenu' 'dittomenu')
provides=("$pkgname")
source=("git+${url}.git")
md5sums=('SKIP')


package() {
  install -dm755 "${pkgdir}/usr/share/plasma/plasmoids"
  cp -r ${_gitname}/package "${pkgdir}/usr/share/plasma/plasmoids/${pkgname}"
  sh /usr/share/plasma/plasmoids/$(pkgname)/translate/build --restartplasma
}