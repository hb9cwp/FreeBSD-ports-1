# Created by: Ditesh Shashikant Gathani <ditesh@gathani.org>
# $FreeBSD$

PORTNAME=	shape
PORTVERSION=	0.9.2
PORTREVISION=	2
CATEGORIES=	devel pear
MASTER_SITES=	http://pecl.php.net/get/
PKGNAMEPREFIX=	pecl-
DIST_SUBDIR=	PECL

MAINTAINER=	ports@FreeBSD.org
COMMENT=	PECL extension that wraps libshape

DEPRECATED=	Works only with EOL php 5.5
EXPIRATION_DATE=	2016-10-20

LICENSE=	PHP30

LIB_DEPENDS=	libshp.so:devel/shapelib

USES=		php:ext tar:tgz
PHP_MODNAME=	shp
IGNORE_WITH_PHP=	56 70

CONFIGURE_ARGS+=	--with-shp=${LOCALBASE}

post-patch:
	@${REINPLACE_CMD} -e 's|include/libshp|include|g' ${WRKSRC}/config.m4
	@${REINPLACE_CMD} -e 's|-ldl||g' ${WRKSRC}/config.m4
	@${REINPLACE_CMD} -e 's|include "libshp/|include "|g' ${WRKSRC}/php_shp.h

.include <bsd.port.mk>
