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
  '221cc47fb7cd29ad80eb3062592e54736619c8ca2e2fc7f2fe94d22b729b6cfa324ef09a765a5f79d2e3c43878dbc62356005a71f729a3a538fbeeb6c933a418'
  '295afd2ac54f84e0f56459920015368690273d904e06dc74a1d60cbe60bd8d11be2d1a10af010dce02df21d6ca4a5ee6c59954afe4334f0b73f6dd7d37e90d0c'
  '5e5d5fd8e7d2f77a3665fd9416f732a5a908fb2daeb0a870d1b5d4acadddbbf0a267259ab7f3a2321a80fc113125aabcb204177d595e1c8e4fd9e9867c7477df'
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
