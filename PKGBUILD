# Maintainer: Daniel Hillenbrand <codeworkx [at] bbqlinux [dot] org>

pkgname=bbqlinux-theme
pkgver=1.0.0
pkgrel=1
pkgdesc="BBQLinux Theme"
arch=('any')
url="https://github.com/bbqlinux/bbqlinux-theme"
license=('GPL')
depends=('gtk-engines' 'gtk-engine-murrine' 'numix-themes' 'gnome-colors-icon-theme' 'gnome-colors-icon-theme-extras')
conflicts=('gtk-theme-bbqlinux')

build () {
	mkdir -p $pkgdir/usr/share/themes/
	cp -r $srcdir/BBQLinux $pkgdir/usr/share/themes/
}
