# Maintainer: Minhmc2007 <quangminh21072010@gmail.com>
pkgname=bal-plymouth-theme
pkgver=1.0
pkgrel=1
pkgdesc="A custom Plymouth boot theme for Blue Archive Linux"
arch=('any')
url="https://github.com/minhmc2007/bal-plymouth-theme"
license=('MIT')
depends=('plymouth')


source=('bal.plymouth'
        'bal.script'
        'LICENSE'
        'README.md')

sha256sums=('SKIP'
            'SKIP'
            'SKIP'
            'SKIP')

package() {
  local _themedir="${pkgdir}/usr/share/plymouth/themes/bal"
  install -d "${_themedir}"

  install -m644 "${srcdir}/bal.plymouth" "${_themedir}/bal.plymouth"
  install -m644 "${srcdir}/bal.script" "${_themedir}/bal.script"

  cp -r "${startdir}/images" "${_themedir}/"

  chmod -R 644 "${_themedir}/images"
  chmod 755 "${_themedir}/images"

  install -Dm644 "${srcdir}/LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
  install -Dm644 "${srcdir}/README.md" "${pkgdir}/usr/share/doc/${pkgname}/README.md"
}
