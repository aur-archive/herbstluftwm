# Maintainer: thorsten w. <p@thorsten-wissmann.de>
pkgname=herbstluftwm
pkgver=0.6.2
pkgrel=1
pkgdesc="Manual tiling window manager for X"
arch=('i686' 'x86_64')
url="http://wwwcip.cs.fau.de/~re06huxa/herbstluftwm"
license=('BSD')
depends=( 'glib2>=2.24' libx11 libxinerama )
optdepends=(
        'bash: needed by most scripts'
        'xterm: used by the default autostart'
        'dmenu: needed by some scripts'
        'dzen2-git: needed by panel.sh'
        'dzen2-xft-xpm-xinerama-svn: view icons as tags'
    )
makedepends=( )
provides=( )
conflicts=( herbstluftwm-git )
backup=( )
source=( http://wwwcip.cs.fau.de/~re06huxa/herbstluftwm/tarballs/$pkgname-$pkgver.tar.gz )
md5sums=( '8bfbbdb16cf88821c8dacd5165590fd2' )

build() {
  cd $srcdir/herbstluftwm-$pkgver
  make PREFIX=/usr DESTDIR="$pkgdir" || return 1
}

package() {
  cd $srcdir/herbstluftwm-$pkgver
  make PREFIX=/usr DESTDIR="$pkgdir" install || return 1
}
