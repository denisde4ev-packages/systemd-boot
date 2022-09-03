pkgname=systemd-boot
pkgver=251.4_1
pkgrel=1
pkgdesc='Simple EFI Boot Manager' # gummiboot description
arch=(x86_64)
url='https://archlinux.org/packages/core/x86_64/systemd/'
license=(GPL2 LGPL2.1) # same as systemd pkg
makedepends=(sed)
provides=(systemd-bootx64.efi)
conflicts=(systemd)
source=(systemd-latest-x86_64.pkg.tar.zst::https://archlinux.org/packages/core/x86_64/systemd/download/)
md5sums=(SKIP)

pkgver() {
	sed -ne '/pkgver/ { s/.* //; s/-/_/gp }'  "$srcdir"/.BUILDINFO 
}

package() {
	install -D {"$srcdir","$pkgdir"}/usr/lib/systemd/boot/efi/systemd-bootx64.efi 
}
