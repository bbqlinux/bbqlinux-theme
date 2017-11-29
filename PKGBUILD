# Maintainer: Daniel Hillenbrand <codeworkx [at] bbqlinux [dot] org>

pkgname=bbqlinux-theme
pkgver=2.6.7
pkgrel=1
pkgdesc='The BBQLinux Theme (based on Numix)'
arch=('any')
url='https://github.com/bbqlinux/bbqlinux-theme'
license=('GPL3')
makedepends=('gdk-pixbuf2' 'git' 'glib2' 'libxml2' 'ruby-sass')
depends=('gtk-engine-murrine' 'gnome-colors-icon-theme' 'gnome-colors-icon-theme-extras')

source=('numix-themes::git+https://github.com/shimmerproject/Numix.git')
md5sums=('SKIP')

prepare() {
    cd ${srcdir}/numix-themes

    # Backgrounds
    grep -rl '#333333' --exclude-dir="scss" ./ | xargs -r sed -i 's/\#333333/\#444444/g'
    grep -rl '#333' --exclude-dir="scss" ./ | xargs -r sed -i 's/\#333/\#444/g'

    # Highlight
    grep -rl '#f0544c' ./ | xargs sed -i 's/#f0544c/#0381C1/g'

    sed -i 's/Numix/BBQLinux/' src/metacity-1/metacity-theme-2.xml
    sed -i 's/Numix/BBQLinux/' src/metacity-1/metacity-theme-3.xml
    sed -i "s/IconTheme=.*/IconTheme=gnome-carbonite/g" src/index.theme   
    sed -i 's/Numix/BBQLinux/' src/index.theme
    sed -i 's/Numix/BBQLinux/' Makefile
}

build() {
    cd ${srcdir}/numix-themes
    make
}

package() {
    cd ${srcdir}/numix-themes
    make DESTDIR="${pkgdir}" install
}
