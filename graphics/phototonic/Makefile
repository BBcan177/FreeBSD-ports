PORTNAME=	phototonic
DISTVERSIONPREFIX=	v
DISTVERSION=	2.1-136
DISTVERSIONSUFFIX=	-g12552ec
PORTREVISION=	1
CATEGORIES=	graphics

MAINTAINER=	eduardo@FreeBSD.org
COMMENT=	Image viewer and organizer
WWW=		https://github.com/oferkv/phototonic

LICENSE=	GPLv3
LICENSE_FILE=	${WRKSRC}/COPYING

DEPRECATED=	Abandonware, upstream repo archived Oct 4, 2023. Consider migrating to graphics/geeqie
EXPIRATION_DATE=2025-02-28

LIB_DEPENDS=	libexiv2.so:graphics/exiv2

USES=		compiler:c++11-lang desktop-file-utils gettext gl qmake qt:5
USE_GITHUB=	yes
GH_ACCOUNT=	oferkv
USE_GL=		gl
USE_QT=		core gui imageformats svg widgets buildtools:build

PORTSCOUT=	skipv:list

post-patch:
	${REINPLACE_CMD} -e 's|%%PREFIX%%|${PREFIX}|g' \
		${WRKSRC}/phototonic.pro

.include <bsd.port.mk>
