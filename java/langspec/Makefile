# Created by: Alex Dupre <ale@FreeBSD.org>
# $FreeBSD$

PORTNAME=	langspec
PORTVERSION=	3.0
CATEGORIES=	java
MASTER_SITES=	http://java.sun.com/docs/books/jls/download/

MAINTAINER=	ale@FreeBSD.org
COMMENT=	The Java Language Specification

BROKEN=		unfetchable
DEPRECATED=	Broken for more than 6 months
EXPIRATION_DATE=	2020-05-05

USES=		zip
NO_BUILD=	yes
NO_WRKSUBDIR=	yes
PORTDOCS=	*

OPTIONS_DEFINE=	DOCS

do-install:
	@${ECHO} -n ">> Installing documentation in ${DOCSDIR}..."
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
	@${CP} -R ${WRKSRC}/*.html ${WRKSRC}/*.gif ${WRKSRC}/chars \
		${STAGEDIR}${DOCSDIR}
	@${ECHO} " [ DONE ]"

.include <bsd.port.mk>
