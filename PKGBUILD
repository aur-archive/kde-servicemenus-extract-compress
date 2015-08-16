# Maintainer:  Hyacinthe Cartiaux <hyacinthe.cartiaux at free.fr>
# Contributor: Nick B <Shirakawasuna at gmail _dot_com>

pkgname=kde-servicemenus-extract-compress
pkgver=1.4.4
pkgrel=2
pkgdesc="Extract and compress servicemenus for KDE"
arch=('any')
url="http://www.kde-apps.org/content/show.php/Extract+And+Compress+KDE4?content=84206"
license=('GPL')
depends=('bash' 'kdebase-workspace')
optdepends=('tar: tarball support'
	    'gzip: gunzip support'
	    'bzip2: bzip2 support'
	    'p7zip: 7Zip support'
	    'rar: RAR compression support'
	    'unrar: RAR extraction support'
	    'zip: ZIP compression support'
	    'unzip: ZIP extraction support'
	    'unace: ACE extraction support')
conflicts=('extract-compress-servicemenu-kde4')
replaces=('extract-compress-servicemenu-kde4')
source=("http://www.kde-apps.org/CONTENT/content-files/84206-ExtractAndCompress_v${pkgver}.tar.gz")
md5sums=('d30b44172912a4223d885520a73ad7d8')

package() {
  install -d ${pkgdir}/usr/{bin,share/kde4/services/ServiceMenus}

  for _i in ExtractAndCompress_v$pkgver/src/*.desktop; do
    install -D -m644 $_i ${pkgdir}/usr/share/kde4/services/ServiceMenus/
  done

  for _i in ExtractAndCompress_v$pkgver/src/*.sh; do
    install -D -m755 $_i ${pkgdir}/usr/bin/
  done

  for _i in ExtractAndCompress_v$pkgver/src/dialogs/*.sh; do
    install -D -m755 $_i ${pkgdir}/usr/bin/
  done
}
