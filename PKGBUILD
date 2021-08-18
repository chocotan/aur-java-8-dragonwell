# Maintainer:  chocotan < loli at linux.com>

pkgname='java-8-dragonwell'
pkgver='8.7.7'; _build='8'; _hash='f411702ca7704a54a79ead0c2e0942a3';
_major="${pkgver%%.*}"
_jdkdir='/usr/lib/jvm'
pkgrel='1'
pkgdesc="Alibaba Java ${_major} Development Kit"
arch=('x86_64')
url='http://dragonwell-jdk.io/'
license=('custom')
depends=('java-runtime-common>=3')
provides=(
  "java-environment=${_major}"
  "java-environment-jdk=${_major}"
  "jdk=${pkgver}"
)
source=(
  "https://github.com/alibaba/dragonwell8/releases/download/dragonwell-${pkgver}_jdk8u292-ga/Alibaba_Dragonwell_${pkgver}_x64_linux.tar.gz"
)

md5sums=('7fa87e6802978c6cfbf5110165294bee')
sha256sums=('799b336da16e4b4c1e25a332e457ed396ef575579f5e9cfcf0332ad29e2ca4e8')

package() {
    # Install
    install -d "${pkgdir}/${_jdkdir}/${pkgname}"
    cd "${srcdir}/jdk8u292-b01"
    cp -a jre lib man sample bin include THIRD_PARTY_README LICENSE ASSEMBLY_EXCEPTION release "${pkgdir}/${_jdkdir}/${pkgname}/"
    mv "src.zip" "${pkgdir}/${_jdkdir}/${pkgname}/lib/"
}
