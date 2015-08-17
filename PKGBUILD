# Maintainer: OmeGa <omega at mailoo dot org>
# Contributor: Guilherme "nirev" Nogueira <guilherme@nirev.org>

pkgname=ruby-rhc
_gemname=rhc
pkgver=1.5.13
pkgrel=1
pkgdesc="The client tools for the OpenShift platform that allow for application management."
arch=('any')
url="https://openshift.redhat.com/community/paas"
license=('Apache')
depends=('ruby' 'ruby-archive-tar-minitar' 'ruby-commander' 'ruby-highline' 
         'ruby-httpclient' 'ruby-net-ssh' 'ruby-open4')
makedepends=('rubygems')
source=(http://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('ed27a6db85f5ad5d51a5ea102bc1d452f5c72af4')

package() {
  cd "$srcdir"
  local _gemdir="$(ruby -rubygems -e'puts Gem.default_dir')"
  gem install --no-user-install --ignore-dependencies -i "$pkgdir$_gemdir" \
    -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
}

# vim:set ts=2 sw=2 et:
