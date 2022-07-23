pkgname=firmware-xiaomi-lemon
pkgver=1
pkgrel=0
pkgdesc="Firmware for Xiaomi Redmi 9T"
url="https://github.com/Kiciuk/proprietary_firmware_lemon"
arch="aarch64"
license="proprietary"
options="!check !strip !archcheck"
_commit=""
source="https://github.com/Kiciuk/proprietary_firmware_lemon/archive/$_commit.zip"
builddir="$srcdir/proprietary_firmware_lemon-$_commit"

_fwdir="/lib/firmware/postmarketos"
_wcndir="/lib/firmware/postmarketos/ath10k/WCN3990/hw1.0"
_devdir="/lib/firmware/qcom/sm6115/xiaomi-lemon/"
package() {
	# parent package is empty
	mkdir -p "$pkgdir"

	install -Dm644 ath10k/WCN3990/hw1.0/* -t "$pkgdir/$_fwdir"
	install -Dm644 modem/modem*.* -t "$pkgdir/$_devdir"
	install -Dm644 wlanmdsp*.* -t "$pkgdir/$_devdir"
	install -Dm644 cdsp*.* -t "$pkgdir/$_devdir"
	install -Dm644 ipa_fws*.* -t "$pkgdir/$_devdir"
	install -Dm644 venus.* -t "$pkgdir/$_devdir"
}
