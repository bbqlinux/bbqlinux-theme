# Maintainer: Daniel Hillenbrand <codeworkx [at] bbqlinux [dot] org>

pkgname=bbqlinux-theme
pkgver=1.1.1
pkgrel=1
pkgdesc="The BBQLinux Theme (based on Numix)"
arch=('any')
url="https://github.com/bbqlinux/bbqlinux-theme"
license=('GPL')
makedepends=('gdk-pixbuf2' 'git' 'glib2' 'libxml2' 'ruby-sass')
depends=('gtk-engine-murrine' 'gnome-colors-icon-theme' 'gnome-colors-icon-theme-extras')
conflicts=('gtk-theme-bbqlinux')

build() {
  cd $srcdir/BBQLinux

  make
}

package () {
	cd $srcdir/BBQLinux
    
    make DESTDIR="${pkgdir}" install
}
