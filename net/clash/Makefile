# $FreeBSD$

PORTNAME=	clash
DISTVERSIONPREFIX=	v
DISTVERSION=	0.18.0
CATEGORIES=	net

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	Rule-based tunnel in Go

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

USES=		go:modules
USE_GITHUB=	yes
GH_ACCOUNT=	Dreamacro
GH_TUPLE=	\
		Dreamacro:go-shadowsocks2:v0.1.5:dreamacro_go_shadowsocks2/vendor/github.com/Dreamacro/go-shadowsocks2 \
		davecgh:go-spew:v1.1.1:davecgh_go_spew/vendor/github.com/davecgh/go-spew \
		eapache:channels:v1.1.0:eapache_channels/vendor/gopkg.in/eapache/channels.v1 \
		eapache:queue:v1.1.0:eapache_queue/vendor/github.com/eapache/queue \
		go-chi:chi:v4.0.3:go_chi_chi/vendor/github.com/go-chi/chi \
		go-chi:cors:v1.0.0:go_chi_cors/vendor/github.com/go-chi/cors \
		go-chi:render:v1.0.1:go_chi_render/vendor/github.com/go-chi/render \
		go-yaml:yaml:v2.2.8:go_yaml_yaml/vendor/gopkg.in/yaml.v2 \
		gofrs:uuid:v3.2.0:gofrs_uuid/vendor/github.com/gofrs/uuid \
		golang:crypto:1d94cc7ab1c6:golang_crypto/vendor/golang.org/x/crypto \
		golang:net:16171245cfb2:golang_net/vendor/golang.org/x/net \
		golang:sync:cd5d95a43a6e:golang_sync/vendor/golang.org/x/sync \
		golang:sys:c709ea063b76:golang_sys/vendor/golang.org/x/sys \
		gorilla:websocket:v1.4.1:gorilla_websocket/vendor/github.com/gorilla/websocket \
		konsorten:go-windows-terminal-sequences:v1.0.1:konsorten_go_windows_terminal_sequences/vendor/github.com/konsorten/go-windows-terminal-sequences \
		miekg:dns:v1.1.27:miekg_dns/vendor/github.com/miekg/dns \
		oschwald:geoip2-golang:v1.4.0:oschwald_geoip2_golang/vendor/github.com/oschwald/geoip2-golang \
		oschwald:maxminddb-golang:v1.6.0:oschwald_maxminddb_golang/vendor/github.com/oschwald/maxminddb-golang \
		pmezard:go-difflib:v1.0.0:pmezard_go_difflib/vendor/github.com/pmezard/go-difflib \
		sirupsen:logrus:v1.4.2:sirupsen_logrus/vendor/github.com/sirupsen/logrus \
		stretchr:testify:v1.4.0:stretchr_testify/vendor/github.com/stretchr/testify

PLIST_FILES=	bin/${PORTNAME}

PORTSCOUT=	limit:^[0-9\.]*$$

pre-patch:
	@cd ${WRKSRC} && ${CP} proxy/redir/tcp_linux.go proxy/redir/tcp_freebsd.go

.include <bsd.port.mk>
