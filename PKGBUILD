pkgname=he-tunnel
pkgver=0.1.1
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
sha512sums=('49b4970ca50bd6858111edaa756f31b860e02cbbe336691b28f69dd0cdd74b818d43c4a16a3c272834c4f056bcbb65eb78bfbc3bdac236684f1311918a8114f6'
            '731da391fac056b108e7db0191fb227785d46616866f08111a028914df3faef23433dd4dc881efad7ccc9beb0d04fdbca2c73fae70932213661c6baf735cf1af'
            '11073404bc2f62ea0f104e03858777793079edad657571c9ab8893a50acfbbe64648d126d8625592cef464f25b9304bd04e2d381f630e320a01cccd61b3c039b')

package() {
  install -Dm 0600 config.default "${pkgdir}/etc/default/he-tunnel"
  install -Dm 0644 he-tunnel.service "${pkgdir}/etc/systemd/system/he-tunnel.service"
  install -Dm 0755 he-tunnel "${pkgdir}/usr/bin/he-tunnel"
}
