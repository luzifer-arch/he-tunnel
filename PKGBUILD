pkgname=he-tunnel
pkgver=0.1.0
pkgrel=1
pkgdesc="Tunnel setup script and service"
arch=(any)
backup=('etc/default/he-tunnel')
license=('MIT')
depends=('curl' 'iproute2')
source=(
  config.default
  he-tunnel
  he-tunnel.service
)
sha512sums=(
  '49b4970ca50bd6858111edaa756f31b860e02cbbe336691b28f69dd0cdd74b818d43c4a16a3c272834c4f056bcbb65eb78bfbc3bdac236684f1311918a8114f6'
  '78e3c2fbedba6b106eb682d0e493a7169787fba4c4b03f3d9e6fe32d14e25348cc5bb6c3cf95da7f551802b25f819c524daeea9e9f696fe3256d9b38585c75b8'
  '11073404bc2f62ea0f104e03858777793079edad657571c9ab8893a50acfbbe64648d126d8625592cef464f25b9304bd04e2d381f630e320a01cccd61b3c039b'
)

package() {
  install -Dm 0600 config.default "${pkgdir}/etc/default/he-tunnel"
  install -Dm 0644 he-tunnel.service "${pkgdir}/etc/systemd/system/he-tunnel.service"
  install -Dm 0755 he-tunnel "${pkgdir}/usr/bin/he-tunnel"
}
