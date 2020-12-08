# Maintainer: NexAdn
pkgname=obs-spectralizer
pkgver=1.2
_obsver=23.0.2
pkgrel=1
pkgdesc="Audio visualization for obs-studio using fftw, based on cli-visualizer."
arch=("x86_64")
url="https://github.com/univrsal/spectralizer"
license=("GPL")
provides=("obs-spectralizer")
conflicts=("obs-spectralizer")
depends=(
	"obs-studio>=${_obsver}"
)
optdepends=()
source=(
    "https://github.com/univrsal/spectralizer/releases/download/v${pkgver}/spectralizer.v${pkgver}.linux.ubuntu.64.zip"
)
sha256sums=('090d2dda2bc99ac1213c7ad05aa91749bfd94ed1a3005c4ddd35e0e303e28d53')
package() {
    cd ${srcdir}/plugin
    install -d ${pkgdir}/usr/lib/obs-plugins/
    install -d ${pkgdir}/usr/share/obs/obs-plugins/obs-spectralizer/
    install -Dm755 ./bin/64bit/* ${pkgdir}/usr/lib/obs-plugins/
    cp -R ./data/* ${pkgdir}/usr/share/obs/obs-plugins/obs-spectralizer/
}
