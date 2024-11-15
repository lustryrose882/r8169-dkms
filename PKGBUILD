_pkgbase=r8169
pkgname=${_pkgbase}-dkms
pkgver=next
pkgrel=1
pkgdesc="A kernel module for Realtek 8168/8169 network cards from tree (DKMS version) (betel)"
url="https://github.com/lustryrose882/$_pkgbase"
license=("GPL")
arch=('i686' 'x86_64')
depends=('glibc' 'dkms')
makedepends=()
conflicts=("${_pkgbase}" "r8168-dkms")
provides=("${_pkgbase}")
source=('dkms.conf')
sha256sums=('SKIP')

package() {
	install -Dm644 'dkms.conf' "${pkgdir}/usr/src/${_pkgbase}-${pkgver}/dkms.conf"

	sed -e "s/@PKGNAME@/${_pkgbase}/g" \
	    -e "s/@PKGVER@/${pkgver}/g" \
	    -i "${pkgdir}/usr/src/${_pkgbase}-${pkgver}/dkms.conf"

	cp -dr --no-preserve='ownership' "./${_pkgbase}" "${pkgdir}/usr/src/${_pkgbase}-${pkgver}/src"
}