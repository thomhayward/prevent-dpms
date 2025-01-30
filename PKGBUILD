pkgname=prevent-dpms
pkgdesc="A systemd user service to prevent Display Power Management Signaling (DPMS) from activating when the system has an active sound output"
pkgver=0.0.1
pkgrel=3
arch=(any)
depends=('bash' 'libpulse' 'xorg-xset')
provides=("$pkgname")
conflicts=("$pkgname")
options=(!debug)
source=(
	prevent-dpms
	prevent-dpms.service
)
sha256sums=(
	37fcb15f1cf14c7e6cbb818abe7223dad1d70ec445c4ee4181071d9e601bede2
	8aeaf925745db706e5cd1e8e08e321ae919213921c15e61bbe7ffb9463a73311
)

package() {
	install -Dm 755 $pkgname -t "${pkgdir}/usr/bin"
	install -Dm 644 ${pkgname}.service -t "${pkgdir}/usr/lib/systemd/user"
}
