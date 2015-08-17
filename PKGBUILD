# Contributor: Anonymous
# Generator  : CPANPLUS::Dist::Arch 1.23

pkgname='perl-moosex-storage'
pkgver='0.31'
pkgrel='1'
pkgdesc="A serialization framework for Moose classes"
arch=('any')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl-moose>=0.99' 'perl-string-rewriteprefix')
makedepends=('perl-test-deep' 'perl-test-fatal' 'perl-test-requires>=0.05')
url='http://search.cpan.org/dist/MooseX-Storage'
source=('http://search.cpan.org/CPAN/authors/id/B/BO/BOBTFISH/MooseX-Storage-0.31.tar.gz')
md5sums=('bb31e6e5c0849960f618f9ef90c42dc3')
sha512sums=('4e9f9295ac0474903bd42a73e720d0a63095f1087ad11f6b6e8099debd0f7bb34a85c8a7183efdc0cdc90b0ae473b7b749d99fb7da7a54c82a1e6cd7d85ab0db')
_distdir="${srcdir}/MooseX-Storage-0.31"

build() {
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""                 \
      PERL_AUTOINSTALL=--skipdeps                            \
      PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'"     \
      PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
      MODULEBUILDRC=/dev/null

    cd "$_distdir"
    /usr/bin/perl Makefile.PL
    make
  )
}

check() {
  cd "$_distdir"
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""
    make test
  )
}

package() {
  cd "$_distdir"
  make install
  find "$pkgdir" -name .packlist -o -name perllocal.pod -delete
}

# Local Variables:
# mode: shell-script
# sh-basic-offset: 2
# End:
# vim:set ts=2 sw=2 et:
