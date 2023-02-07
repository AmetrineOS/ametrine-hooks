# Maintainer: Endercass <contact@endercass.me>

pkgname=ametrine-hooks
pkgver=0.1
pkgrel=1
pkgdesc='AmetrineOS pacman hooks'
arch=('any')
license=('GPL3')
url=https://github.com/endeavouros-team/PKGBUILDS/tree/master/$pkgname
_rawurl=https://raw.githubusercontent.com/AmetrineOS/$pkgname/main
depends=(libnotify)

source=(
  $_rawurl/ametrine-os-release.hook
  $_rawurl/ametrine-lsb-release.hook
  $_rawurl/ametrine-hooks.hook
  $_rawurl/ametrine-hooks-runner
)

sha512sums=(
  'f6c776668f21bf4ade0bfcafdfc49b741ebf7f1ef1677e049b925faedab0c73253e4b348ed5816de45c158efc3dd49af01ff25313cb4a715822d02985b7360c9'
  '820af26a248a505c1d93deead37ca7ab5fe477f6688792a97682a72b7a68c843f29fbaaaceb18d0e2290afe7b62a185490cbea418ee604c39a5ca8df9a853a8d'
  '62389b5a29cd65fac707ab5ce767a083d8acd8dafcf488676f9104d8ca7e7007547b1b789a43ffb8665a5d1a33e29d45fea69cec78f303acaea1cdbff0b8b633'
  '8615128ea69827124fecba20e588c2814c8c3378748c2158af9fe2d5b95cbc01f9cf6df2cb1c026c85440fbfeee031cc4d3dca2d3ed922ba85916762bb72492a'
)

package() {
  local hooks=$pkgdir/usr/share/libalpm/hooks
  local bin=$pkgdir/usr/bin

  install -Dm644 ametrine-lsb-release.hook $hooks/eos-lsb-release.hook
  install -Dm644 ametrine-os-release.hook $hooks/eos-os-release.hook
  install -Dm644 ametrine-hooks.hook $hooks/ametrine-hooks.hook

  install -Dm755 ametrine-hooks-runner $bin/ametrine-hooks-runner
}
