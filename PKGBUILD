# Maintainer: Florian Bruhin (The Compiler) <archlinux.org@the-compiler.org>

pkgname=diylc
pkgver=3.28.0
pkgrel=1
arch=('any')
pkgdesc='diy-layout-creator is a free multi-platform electronic schematic, layout and guitar wiring diagram editor'
depends=('java-runtime' 'bash')
url='https://code.google.com/p/diy-layout-creator/'
license=('GPL3')
source=("https://diy-layout-creator.googlecode.com/files/${pkgname}-${pkgver}.zip"
        'diylc.png::https://code.google.com/p/diy-layout-creator/logo'
        'diylc'
        'diylc.desktop'
        'diylc.install')
sha1sums=('1d0382eca07e491da329d68232ab53295b91bd5a'
          '52be299e2d301c29951adcc8e3515ff82094d818'
          'c4ae43d2c38d0d63d4fd79238b2db26a8275bf89'
          'b9f85b2a7a660617d5fd2249e0c842beaac7116d'
          'd69df3f88929f74cdcaea0dcd9047bdbf2b1db7e')

package() {
  install -dm 755 "${pkgdir}/usr/share/${pkgname}"
  install -dm 755 "${pkgdir}/usr/share/"{pixmaps,applications}
  install -dm 755 "${pkgdir}/usr/share/${pkgname}/"{templates,themes}

  install -m 644 "${srcdir}"/update.xml "${pkgdir}/usr/share/${pkgname}"
  install -m 644 "${srcdir}"/diylc.l4j.ini "${pkgdir}/usr/share/${pkgname}"
  install -m 644 "${srcdir}/templates"/* "${pkgdir}/usr/share/${pkgname}/templates"
  install -m 644 "${srcdir}/themes"/* "${pkgdir}/usr/share/${pkgname}/themes"

  install -dm 755 "${pkgdir}/usr/share/java/${pkgname}"
  install -dm 755 "${pkgdir}/usr/share/java/${pkgname}/"{lib,library}

  install -m 644 "${srcdir}/diylc.jar" "${pkgdir}/usr/share/java/${pkgname}"
  install -m 644 "${srcdir}/lib"/*.jar "${pkgdir}/usr/share/java/${pkgname}/lib"
  install -m 644 "${srcdir}/library"/*.jar "${pkgdir}/usr/share/java/${pkgname}/library"

  install -dm 755 "${pkgdir}/usr/bin"
  install -m 755 "${srcdir}/diylc" "${pkgdir}/usr/bin"

  install -m 755 "${srcdir}/diylc.png" "${pkgdir}/usr/share/pixmaps"
  install -m 755 "${srcdir}/diylc.desktop" "${pkgdir}/usr/share/applications"
}

# vim:set ts=2 sw=2 et:
