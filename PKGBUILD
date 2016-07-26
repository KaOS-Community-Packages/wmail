pkgname=wmail
pkgver=1.3.5
pkgrel=1
pkgdesc="The missing desktop client for Gmail & Google Inbox"
arch=('x86_64')
url="https://github.com/Thomas101/wmail"
license=('MIT')
source=("https://github.com/Thomas101/wmail/releases/download/v${pkgver}/WMail_1_3_5_linux64.zip" "wmail.png" "wmail.desktop")
depends=("gtk2" "gconf" "nss" "libnotify" "alsa-lib")
options=(!strip)
md5sums=('3cf53e79912ea70b2f71201698c4c0b2'
         '2da07d7b2da2cddc51a9c16491acb3cd'
         '7b9a03232809da53600251b02f03969e')

package() {
	install -dm755 $pkgdir/usr/share/wmail
	cp -r * $pkgdir/usr/share/wmail
	install -Dm644 wmail.desktop $pkgdir/usr/share/applications/wmail.desktop
	install -Dm644 wmail.png $pkgdir/usr/share/pixmaps/wmail.png
	install -dm755 $pkgdir/usr/bin
	ln -s /usr/share/wmail/WMail $pkgdir/usr/bin/wmail
    rm   $pkgdir/usr/share/wmail/{WMail_1_3_5_linux64.zip,wmail.desktop,wmail.png}
}
