# Maintainer Kovivchak Evgen <oneonfire@gmail.com>

pkgname=owl
pkgver=0.7.6
pkgrel=3
pkgdesc="Obfuscated Weird Language interpreter"
arch=('i686' 'x86_64')
url="http://digilander.libero.it/tonibinhome/owl"
license=('GPL')
depends=(glibc)
optdepends=(vim)
source=("http://digilander.libero.it/tonibinhome/owl/distrib/${pkgname}.${pkgver}.src.tgz")
md5sums=('4d566bdf4f40779d536ecf6741abee2f')

package() {
	cd $srcdir/$pkgname.$pkgver.src/
	make	
	install -m755 -D $pkgname $pkgdir/usr/bin/$pkgname 
	# license 	
	install -m644 -D COPYING $pkgdir/usr/share/licenses/$pkgname/COPYING
	# vim syntax
	install -m644 -D owl.vim $pkgdir/usr/share/vim/vim73/syntax/owl.vim
}

