.PHONY: all install clean

all:
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/LuaJIT-2.1-20230410 && $(MAKE) TARGET_STRIP=@: CCDEBUG=-g XCFLAGS='-DLUAJIT_ENABLE_LUA52COMPAT -fno-stack-check' CC=cc MACOSX_DEPLOYMENT_TARGET='12.7' PREFIX=/usr/local/openresty/luajit
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/lua-cjson-2.1.0.11 && $(MAKE) DESTDIR=$(DESTDIR) LUA_INCLUDE_DIR=/Users/chong.zhang/Documents/openresty-1.21.4.3/build/luajit-root/usr/local/openresty/luajit/include/luajit-2.1 LUA_CMODULE_DIR=/usr/local/openresty/lualib LUA_MODULE_DIR=/usr/local/openresty/lualib CJSON_CFLAGS="-g -fpic" CJSON_LDFLAGS='-bundle -undefined dynamic_lookup' CC=cc
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/lua-resty-signal-0.03 && $(MAKE) DESTDIR=$(DESTDIR) LUA_INCLUDE_DIR=/Users/chong.zhang/Documents/openresty-1.21.4.3/build/luajit-root/usr/local/openresty/luajit/include/luajit-2.1 LUA_LIB_DIR=/usr/local/openresty/lualib LDFLAGS='-bundle -undefined dynamic_lookup' CC=cc
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/lua-redis-parser-0.13 && $(MAKE) DESTDIR=$(DESTDIR) LUA_INCLUDE_DIR=/Users/chong.zhang/Documents/openresty-1.21.4.3/build/luajit-root/usr/local/openresty/luajit/include/luajit-2.1 LUA_LIB_DIR=/usr/local/openresty/lualib LDFLAGS='-bundle -undefined dynamic_lookup' CC=cc
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/lua-rds-parser-0.06 && $(MAKE) DESTDIR=$(DESTDIR) LUA_INCLUDE_DIR=/Users/chong.zhang/Documents/openresty-1.21.4.3/build/luajit-root/usr/local/openresty/luajit/include/luajit-2.1 LUA_LIB_DIR=/usr/local/openresty/lualib LDFLAGS='-bundle -undefined dynamic_lookup' CC=cc
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/nginx-1.21.4 && $(MAKE)

install: all
	mkdir -p $(DESTDIR)/usr/local/openresty/
	-cp /Users/chong.zhang/Documents/openresty-1.21.4.3/COPYRIGHT $(DESTDIR)/usr/local/openresty/
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/LuaJIT-2.1-20230410 && $(MAKE) install TARGET_STRIP=@: CCDEBUG=-g XCFLAGS='-DLUAJIT_ENABLE_LUA52COMPAT -fno-stack-check' CC=cc MACOSX_DEPLOYMENT_TARGET='12.7' PREFIX=/usr/local/openresty/luajit DESTDIR=$(DESTDIR)
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/lua-cjson-2.1.0.11 && $(MAKE) install DESTDIR=$(DESTDIR) LUA_INCLUDE_DIR=/Users/chong.zhang/Documents/openresty-1.21.4.3/build/luajit-root/usr/local/openresty/luajit/include/luajit-2.1 LUA_CMODULE_DIR=/usr/local/openresty/lualib LUA_MODULE_DIR=/usr/local/openresty/lualib CJSON_CFLAGS="-g -fpic" CJSON_LDFLAGS='-bundle -undefined dynamic_lookup' CC=cc
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/lua-resty-signal-0.03 && $(MAKE) install DESTDIR=$(DESTDIR) LUA_INCLUDE_DIR=/Users/chong.zhang/Documents/openresty-1.21.4.3/build/luajit-root/usr/local/openresty/luajit/include/luajit-2.1 LUA_LIB_DIR=/usr/local/openresty/lualib LDFLAGS='-bundle -undefined dynamic_lookup' CC=cc
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/lua-redis-parser-0.13 && $(MAKE) install DESTDIR=$(DESTDIR) LUA_INCLUDE_DIR=/Users/chong.zhang/Documents/openresty-1.21.4.3/build/luajit-root/usr/local/openresty/luajit/include/luajit-2.1 LUA_LIB_DIR=/usr/local/openresty/lualib LDFLAGS='-bundle -undefined dynamic_lookup' CC=cc
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/lua-rds-parser-0.06 && $(MAKE) install DESTDIR=$(DESTDIR) LUA_INCLUDE_DIR=/Users/chong.zhang/Documents/openresty-1.21.4.3/build/luajit-root/usr/local/openresty/luajit/include/luajit-2.1 LUA_LIB_DIR=/usr/local/openresty/lualib LDFLAGS='-bundle -undefined dynamic_lookup' CC=cc
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/lua-resty-dns-0.22 && $(MAKE) install DESTDIR=$(DESTDIR) LUA_LIB_DIR=/usr/local/openresty/lualib INSTALL=/Users/chong.zhang/Documents/openresty-1.21.4.3/build/install
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/lua-resty-memcached-0.17 && $(MAKE) install DESTDIR=$(DESTDIR) LUA_LIB_DIR=/usr/local/openresty/lualib INSTALL=/Users/chong.zhang/Documents/openresty-1.21.4.3/build/install
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/lua-resty-redis-0.30 && $(MAKE) install DESTDIR=$(DESTDIR) LUA_LIB_DIR=/usr/local/openresty/lualib INSTALL=/Users/chong.zhang/Documents/openresty-1.21.4.3/build/install
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/lua-resty-mysql-0.26 && $(MAKE) install DESTDIR=$(DESTDIR) LUA_LIB_DIR=/usr/local/openresty/lualib INSTALL=/Users/chong.zhang/Documents/openresty-1.21.4.3/build/install
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/lua-resty-string-0.15 && $(MAKE) install DESTDIR=$(DESTDIR) LUA_LIB_DIR=/usr/local/openresty/lualib INSTALL=/Users/chong.zhang/Documents/openresty-1.21.4.3/build/install
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/lua-resty-upload-0.11 && $(MAKE) install DESTDIR=$(DESTDIR) LUA_LIB_DIR=/usr/local/openresty/lualib INSTALL=/Users/chong.zhang/Documents/openresty-1.21.4.3/build/install
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/lua-resty-websocket-0.10 && $(MAKE) install DESTDIR=$(DESTDIR) LUA_LIB_DIR=/usr/local/openresty/lualib INSTALL=/Users/chong.zhang/Documents/openresty-1.21.4.3/build/install
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/lua-resty-lock-0.09 && $(MAKE) install DESTDIR=$(DESTDIR) LUA_LIB_DIR=/usr/local/openresty/lualib INSTALL=/Users/chong.zhang/Documents/openresty-1.21.4.3/build/install
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/lua-resty-lrucache-0.13 && $(MAKE) install DESTDIR=$(DESTDIR) LUA_LIB_DIR=/usr/local/openresty/lualib INSTALL=/Users/chong.zhang/Documents/openresty-1.21.4.3/build/install
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/lua-resty-core-0.1.27 && $(MAKE) install DESTDIR=$(DESTDIR) LUA_LIB_DIR=/usr/local/openresty/lualib INSTALL=/Users/chong.zhang/Documents/openresty-1.21.4.3/build/install
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/lua-resty-upstream-healthcheck-0.08 && $(MAKE) install DESTDIR=$(DESTDIR) LUA_LIB_DIR=/usr/local/openresty/lualib INSTALL=/Users/chong.zhang/Documents/openresty-1.21.4.3/build/install
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/lua-resty-limit-traffic-0.08 && $(MAKE) install DESTDIR=$(DESTDIR) LUA_LIB_DIR=/usr/local/openresty/lualib INSTALL=/Users/chong.zhang/Documents/openresty-1.21.4.3/build/install
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/lua-resty-shell-0.03 && $(MAKE) install DESTDIR=$(DESTDIR) LUA_LIB_DIR=/usr/local/openresty/lualib INSTALL=/Users/chong.zhang/Documents/openresty-1.21.4.3/build/install
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/lua-tablepool-0.02 && $(MAKE) install DESTDIR=$(DESTDIR) LUA_LIB_DIR=/usr/local/openresty/lualib INSTALL=/Users/chong.zhang/Documents/openresty-1.21.4.3/build/install
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/opm-0.0.7 && /Users/chong.zhang/Documents/openresty-1.21.4.3/build/install bin/* $(DESTDIR)/usr/local/openresty/bin/
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/resty-cli-0.29 && /Users/chong.zhang/Documents/openresty-1.21.4.3/build/install bin/* $(DESTDIR)/usr/local/openresty/bin/
	cp /Users/chong.zhang/Documents/openresty-1.21.4.3/build/resty.index $(DESTDIR)/usr/local/openresty/
	cp -r /Users/chong.zhang/Documents/openresty-1.21.4.3/build/pod $(DESTDIR)/usr/local/openresty/
	cd /Users/chong.zhang/Documents/openresty-1.21.4.3/build/nginx-1.21.4 && $(MAKE) install DESTDIR=$(DESTDIR)
	mkdir -p $(DESTDIR)/usr/local/openresty/site/lualib $(DESTDIR)/usr/local/openresty/site/pod $(DESTDIR)/usr/local/openresty/site/manifest
	ln -sf /usr/local/openresty/nginx/sbin/nginx $(DESTDIR)/usr/local/openresty/bin/openresty

clean:
	rm -rf build *.exe *.dll openresty-*
