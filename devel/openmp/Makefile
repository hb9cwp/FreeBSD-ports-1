# $FreeBSD$

PORTNAME=	openmp
PORTVERSION=	3.9.0
DISTVERSIONSUFFIX=	.src
CATEGORIES=	devel
MASTER_SITES=	http://llvm.org/releases/${PORTVERSION}/

MAINTAINER=	bapt@FreeBSD.org
COMMENT=	Support for the OpenMP language

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE.txt

ONLY_FOR_ARCHS=	amd64 # i386

USES=		cmake compiler:c++11-lib perl5 tar:xz
USE_PERL5=	build
USE_LDCONFIG=	yes
PLIST_FILES=	include/omp.h \
		lib/libgomp.so \
		lib/libiomp5.so \
		lib/libomp.so.0 \
		lib/libomp.so

.include <bsd.port.mk>
