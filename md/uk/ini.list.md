---
navigation:
  - ini.md: « Директиви php.ini
  - ini.sections.md: Список розділів php.ini »
  - index.md: PHP Manual
  - ini.md: Директиви php.ini
title: Список директив php.ini
---
## Список директив php.ini

Цей список включає директиви php.ini, які можна використовувати для налаштування PHP.

Стовпець "Місце зміни" показує, коли і де може бути встановлена ​​директива. Для отримання інформації про значення цих директив дивіться розділ ["Где може бути встановлена ​​директива?"](configuration.changes.modes.md)

**Параметри конфігурації**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [allowurlfopen](filesystem.configuration.md#ini.allow-url-fopen) | "1" | PHPINISYSTEM |  |
| [allowurlinclude](filesystem.configuration.md#ini.allow-url-include) | "0" | PHPINISYSTEM | Оголошено застарілим у PHP 7.4.0. |
| [argseparator.input](ini.core.md#ini.arg-separator.input) | "&" | PHPINIPERDIR |  |
| [argseparator.output](ini.core.md#ini.arg-separator.output) | "&" | PHPINIALL |  |
| [assert.active](info.configuration.md#ini.assert.active) | "1" | PHPINIALL |  |
| [assert.bail](info.configuration.md#ini.assert.bail) | "0" | PHPINIALL |  |
| [assert.callback](info.configuration.md#ini.assert.callback) | NULL | PHPINIALL |  |
| [assert.exception](info.configuration.md#ini.assert.exception) | "0" | PHPINIALL |  |
| [assert.quieteval](info.configuration.md#ini.assert.quiet-eval) | "0" | PHPINIALL | Видалено, починаючи з PHP 8.0.0 |
| [assert.warning](info.configuration.md#ini.assert.warning) | "1" | PHPINIALL |  |
| [autoappendfile](ini.core.md#ini.auto-append-file) | NULL | PHPINIPERDIR |  |
| [autodetectlineendings](filesystem.configuration.md#ini.auto-detect-line-endings) | "0" | PHPINIALL |  |
| [autoglobalsjit](ini.core.md#ini.auto-globals-jit) | "1" | PHPINIPERDIR |  |
| [autoprependfile](ini.core.md#ini.auto-prepend-file) | NULL | PHPINIPERDIR |  |
| [bcmath.scale](bc.configuration.md#ini.bcmath.scale) | "0" | PHPINIALL |  |
| [browscap](misc.configuration.md#ini.browscap) | NULL | PHPINISYSTEM |  |
| [cgi.checkshebangline](ini.core.md#ini.cgi.check-shebang-line) | "1" | PHPINISYSTEM |  |
| [cgi.discardpath](ini.core.md#ini.cgi.discard-path) | "0" | PHPINISYSTEM |  |
| [cgi.fixpathinfo](ini.core.md#ini.cgi.fix-pathinfo) | "1" | PHPINISYSTEM |  |
| [cgi.forceredirect](ini.core.md#ini.cgi.force-redirect) | "1" | PHPINISYSTEM |  |
| [cgi.nph](ini.core.md#ini.cgi.nph) | "0" | PHPINIALL |  |
| [cgi.redirectstatusenv](ini.core.md#ini.cgi.redirect-status-env) | NULL | PHPINISYSTEM |  |
| [cgi.rfc2616headers](ini.core.md#ini.cgi.rfc2616-headers) | "0" | PHPINIALL |  |
| [childterminate](apache.configuration.md#ini.child-terminate) | "0" | PHPINIALL |  |
| [cli.pager](readline.configuration.md#ini.cli.pager) | "" | PHPINIALL |  |
| [cli.prompt](readline.configuration.md#ini.cli.prompt) | "в > " | PHPINIALL |  |
| [cliserver.color](features.commandline.ini.md#ini.cli-server.color) | "0" | PHPINIALL |  |
| [com.allowdcom](com.configuration.md#ini.com.allow-dcom) | "0" | PHPINISYSTEM |  |
| [com.autoregistertypelib](com.configuration.md#ini.com.autoregister-typelib) | "0" | PHPINIALL |  |
| [com.autoregisterverbose](com.configuration.md#ini.com.autoregister-verbose) | "0" | PHPINIALL |  |
| [com.autoregistercasesensitive](com.configuration.md#ini.com.autoregister-casesensitive) | "1" | PHPINIALL |  |
| [com.codepage](com.configuration.md#ini.com.code-page) | "" | PHPINIALL |  |
| [com.dotnetversion](com.configuration.md#ini.com.dotnet-version) | "" | PHPINISYSTEM | Починаючи з PHP 8.0.0 |
| [com.typelibfile](com.configuration.md#ini.com.typelib-file) | "" | PHPINISYSTEM |  |
| [curl.cainfo](curl.configuration.md#ini.curl.cainfo) | NULL | PHPINISYSTEM |  |
| [date.defaultlatitude](datetime.configuration.md#ini.date.default-latitude) | "31.7667" | PHPINIALL |  |
| [date.defaultlongitude](datetime.configuration.md#ini.date.default-longitude) | "35.2333" | PHPINIALL |  |
| [date.sunrisezenith](datetime.configuration.md#ini.date.sunrise-zenith) | "90.583333" | PHPINIALL |  |
| [date.sunsetzenith](datetime.configuration.md#ini.date.sunset-zenith) | "90.583333" | PHPINIALL |  |
| [date.timezone](datetime.configuration.md#ini.date.timezone) | "UTC" | PHPINIALL |  |
| [dba.defaulthandler](dba.configuration.md#ini.dba.default_handler) | DBADEFAULT | PHPINIALL |  |
| [defaultcharset](ini.core.md#ini.default-charset) | "UTF-8" | PHPINIALL | За замовчуванням "UTF-8". |
| [inputencoding](ini.core.md#ini.input-encoding) | "" | PHPINIALL |  |
| [outputencoding](ini.core.md#ini.output-encoding) | "" | PHPINIALL |  |
| [internalencoding](ini.core.md#ini.internal-encoding) | "" | PHPINIALL |  |
| [defaultmimetype](ini.core.md#ini.default-mimetype) | "text/html" | PHPINIALL |  |
| [defaultsockettimeout](filesystem.configuration.md#ini.default-socket-timeout) | "60" | PHPINIALL |  |
| [disableclasses](ini.core.md#ini.disable-classes) | "" | Тільки php.ini |  |
| [disablefunctions](ini.core.md#ini.disable-functions) | "" | Тільки php.ini |  |
| [displayerrors](errorfunc.configuration.md#ini.display-errors) | "1" | PHPINIALL |  |
| [displaystartuperrors](errorfunc.configuration.md#ini.display-startup-errors) | "1" | PHPINIALL | До PHP 8.0.0 значення за промовчанням було `"0"` |
| [docrefext](errorfunc.configuration.md#ini.docref-ext) | "" | PHPINIALL |  |
| [docrefroot](errorfunc.configuration.md#ini.docref-root) | "" | PHPINIALL |  |
| [docroot](ini.core.md#ini.doc-root) | NULL | PHPINISYSTEM |  |
| [enableдл](info.configuration.md#ini.enable-dl) | "1" | PHPINISYSTEM | Ця можливість застаріла та *буде* обов'язково *видалено* в майбутньому. |
| [enablepostdatareading](ini.core.md#ini.enable-post-data-reading) | Він | PHPINIPERDIR |  |
| [engine](apache.configuration.md#ini.engine) | "1" | PHPINIALL |  |
| [errorappendstring](errorfunc.configuration.md#ini.error-append-string) | NULL | PHPINIALL |  |
| [errorlog](errorfunc.configuration.md#ini.error-log) | NULL | PHPINIALL |  |
| [errorprependstring](errorfunc.configuration.md#ini.error-prepend-string) | NULL | PHPINIALL |  |
| [errorreporting](errorfunc.configuration.md#ini.error-reporting) | NULL | PHPINIALL |  |
| [exif.encodeunicode](exif.configuration.md#ini.exif.encode-unicode) | "ISO-8859-15" | PHPINIALL |  |
| [exif.decodeunicodemotorola](exif.configuration.md#ini.exif.decode-unicode-motorola) | "UCS-2BE" | PHPINIALL |  |
| [exif.decodeunicodeintel](exif.configuration.md#ini.exif.decode-unicode-intel) | "UCS-2LE" | PHPINIALL |  |
| [exif.encodejis](exif.configuration.md#ini.exif.encode-jis) | "" | PHPINIALL |  |
| [exif.decodejismotorola](exif.configuration.md#ini.exif.decode-jis-motorola) | "JIS" | PHPINIALL |  |
| [exif.decodejisintel](exif.configuration.md#ini.exif.decode-jis-intel) | "JIS" | PHPINIALL |  |
| [exitвінtimeout](ini.core.md#ini.exit-on-timeout) | "" | PHPINIALL |  |
| [expect.timeout](expect.configuration.md#ini.expect.timeout) | "10" | PHPINIALL |  |
| [expect.loguser](expect.configuration.md#ini.expect.loguser) | "1" | PHPINIALL |  |
| [expect.logfile](expect.configuration.md#ini.expect.logfile) | "" | PHPINIALL |  |
| [expect.matchmax](expect.configuration.md#ini.expect.match-max) | "" | PHPINIALL |  |
| [exposephp](ini.core.md#ini.expose-php) | "1" | Тільки php.ini |  |
| [extension](ini.core.md#ini.extension) | NULL | Тільки php.ini |  |
| [extensiondir](ini.core.md#ini.extension-dir) | "/path/to/php" | PHPINISYSTEM |  |
| [fastcgi.impersonate](ini.core.md#ini.fastcgi.impersonate) | "0" | PHPINISYSTEM |  |
| [fastcgi.logging](ini.core.md#ini.fastcgi.logging) | "1" | PHPINISYSTEM |  |
| [fileuploads](ini.core.md#ini.file-uploads) | "1" | PHPINISYSTEM |  |
| [filter.default](filter.configuration.md#ini.filter.default) | "unsaferaw" | PHPINIPERDIR | Параметр застарів, починаючи з PHP 8.1.0. |
| [filter.defaultflags](filter.configuration.md#ini.filter.default-flags) | NULL | PHPINIPERDIR |  |
| [from](filesystem.configuration.md#ini.from) | "" | PHPINIALL |  |
| [gd.jpegignorewarning](image.configuration.md#ini.gd.jpeg-ignore-warning) | "1" | PHPINIALL |  |
| [geoip.customdirectory](geoip.configuration.md#ini.geoip.custom-directory) | "" | PHPINIALL |  |
| hardtimeout | "2" | PHPINISYSTEM | Доступно з PHP 7.1.0. |
| [highlight.comment](misc.configuration.md#ini.syntax-highlighting) | "#FF8000" | PHPINIALL |  |
| [highlight.default](misc.configuration.md#ini.syntax-highlighting) | "#0000BB" | PHPINIALL |  |
| [highlight.html](misc.configuration.md#ini.syntax-highlighting) | "#000000" | PHPINIALL |  |
| [highlight.keyword](misc.configuration.md#ini.syntax-highlighting) | "#007700" | PHPINIALL |  |
| [highlight.string](misc.configuration.md#ini.syntax-highlighting) | "#DD0000" | PHPINIALL |  |
| [htmlerrors](errorfunc.configuration.md#ini.html-errors) | "1" | PHPINIALL |  |
| [ibase.allowpersistent](ibase.configuration.md#ini.ibase.allow-persistent) | "1" | PHPINISYSTEM |  |
| [ibase.maxpersistent](ibase.configuration.md#ini.ibase.max-persistent) | "-1" | PHPINISYSTEM |  |
| [ibase.maxlinks](ibase.configuration.md#ini.ibase.max-links) | "-1" | PHPINISYSTEM |  |
| [ibase.defaultдб](ibase.configuration.md#ini.ibase.default-db) | NULL | PHPINISYSTEM |  |
| [ibase.defaultuser](ibase.configuration.md#ini.ibase.default-user) | NULL | PHPINIALL |  |
| [ibase.defaultpassword](ibase.configuration.md#ini.ibase.default-password) | NULL | PHPINIALL |  |
| [ibase.defaultcharset](ibase.configuration.md#ini.ibase.default-charset) | NULL | PHPINIALL |  |
| [ibase.timestampformat](ibase.configuration.md#ini.ibase.timestampformat) | "%Y-%m-%d %H:%M:%S" | PHPINIALL |  |
| [ibase.dateformat](ibase.configuration.md#ini.ibase.dateformat) | "%Y-%m-%d" | PHPINIALL |  |
| [ibase.timeformat](ibase.configuration.md#ini.ibase.timeformat) | "%H:%M:%S" | PHPINIALL |  |
| [ibmdb2.binmode](ibm-db2.configuration.md#ini.ibm-db2.binmode) | "1" | PHPINIALL |  |
| [ibmdb2.i5allpconnect](ibm-db2.configuration.md#ini.ibm-db2.i5-all-pconnect) | "0" | PHPINISYSTEM | Доступно з ibmdb2 1.6.5. |
| [ibmdb2.i5allowcommit](ibm-db2.configuration.md#ini.ibm-db2.i5-allow-commit) | "0" | PHPINISYSTEM | Доступно з ibmdb2 1.4.9. |
| [ibmdb2.i5dbcsalloc](ibm-db2.configuration.md#ini.ibm-db2.i5-dbcs-alloc) | "0" | PHPINISYSTEM | Доступно з ibmdb2 1.5.0. |
| [ibmdb2.instancename](ibm-db2.configuration.md#ini.ibm-db2.instance-name) | NULL | PHPINISYSTEM | Доступно з ibmdb2 1.0.2. |
| [ibmdb2.i5ignoreuserid](ibm-db2.configuration.md#ini.ibm-db2.i5-ignore-userid) | "0" | PHPINISYSTEM | Доступно з ibmdb2 1.8.0. |
| [iconv.inputencoding](iconv.configuration.md#ini.iconv.input-encoding) | "" | PHPINIALL | Застаріло з PHP 5.6.0. |
| [iconv.outputencoding](iconv.configuration.md#ini.iconv.output-encoding) | "" | PHPINIALL | Застаріло з PHP 5.6.0. |
| [iconv.internalencoding](iconv.configuration.md#ini.iconv.internal-encoding) | "" | PHPINIALL | Застаріло з PHP 5.6.0. |
| [ignorerepeatederrors](errorfunc.configuration.md#ini.ignore-repeated-errors) | "0" | PHPINIALL |  |
| [ignorerepeatedsource](errorfunc.configuration.md#ini.ignore-repeated-source) | "0" | PHPINIALL |  |
| [ignoreuserabort](misc.configuration.md#ini.ignore-user-abort) | "0" | PHPINIALL |  |
| [implicitflush](outcontrol.configuration.md#ini.implicit-flush) | "0" | PHPINIALL |  |
| [includepath](ini.core.md#ini.include-path) | ".:/path/to/php/pear" | PHPINIALL |  |
| [intl.defaultlocale](intl.configuration.md#ini.intl.default-locale) |  | PHPINIALL |  |
| [intl.errorlevel](intl.configuration.md#ini.intl.error-level) |  | PHPINIALL |  |
| [intl.useexceptions](intl.configuration.md#ini.intl.use-exceptions) |  | PHPINIALL | Доступно з PECL 3.0.0a1 |
| [lastmodified](apache.configuration.md#ini.last-modified) | "0" | PHPINIALL |  |
| [ldap.maxlinks](ldap.configuration.md#ini.ldap.max_links) | "-1" | PHPINISYSTEM |  |
| [logerrors](errorfunc.configuration.md#ini.log-errors) | "0" | PHPINIALL |  |
| [logerrorsmaxlen](errorfunc.configuration.md#ini.log-errors-max-len) | "1024" | PHPINIALL |  |
| [mail.addзheader](mail.configuration.md#ini.mail.add-x-header) | "0" | PHPINIPERDIR |  |
| mail.forceextraparameters | NULL | Тільки php.ini |  |
| [mail.log](mail.configuration.md#ini.mail.log) | "" | PHPINIPERDIR |  |
| [maxexecutiontime](info.configuration.md#ini.max-execution-time) | "30" | PHPINIALL |  |
| [maxinputnestinglevel](info.configuration.md#ini.max-input-nesting-level) | "64" | PHPINIPERDIR |  |
| [maxinputvars](info.configuration.md#ini.max-input-vars) |  | PHPINIPERDIR |  |
| [maxinputtime](info.configuration.md#ini.max-input-time) | "-1" | PHPINIPERDIR |  |
| [mbstring.language](mbstring.configuration.md#ini.mbstring.language) | "neutral" | PHPINIALL |  |
| [mbstring.detectorder](mbstring.configuration.md#ini.mbstring.detect-order) | NULL | PHPINIALL |  |
| [mbstring.httpinput](mbstring.configuration.md#ini.mbstring.http-input) | "pass" | PHPINIALL | Застаріла |
| [mbstring.httpoutput](mbstring.configuration.md#ini.mbstring.http-output) | "pass" | PHPINIALL | Застаріла |
| [mbstring.internalencoding](mbstring.configuration.md#ini.mbstring.internal-encoding) | NULL | PHPINIALL | Застаріла |
| [mbstring.substitutecharacter](mbstring.configuration.md#ini.mbstring.substitute-character) | NULL | PHPINIALL |  |
| [mbstring.funcoverload](mbstring.configuration.md#ini.mbstring.func-overload) | "0" | PHPINISYSTEM | Оголошено застарілим у PHP 7.2.0; видалено з PHP 8.0.0. |
| [mbstring.encodingtranslation](mbstring.configuration.md#ini.mbstring.encoding-translation) | "0" | PHPINIPERDIR |  |
| [mbstring.httpoutputconvmimetypes](mbstring.configuration.md#ini.mbstring.http-output-conv-mimetypes) | "^(text/ | application/xhtml+xml)" | PHPINIALL |
| [mbstring.strictdetection](mbstring.configuration.md#ini.mbstring.strict-detection) | "0" | PHPINIALL |  |
| [mcrypt.algorithmsdir](mcrypt.configuration.md#ini.mcrypt.algorithms-dir) | **`null`** | PHPINIALL |  |
| [mcrypt.modesdir](mcrypt.configuration.md#ini.mcrypt.modes-dir) | **`null`** | PHPINIALL |  |
| [memcache.allowfailover](memcache.ini.md#ini.memcache.allow-failover) | "1" | PHPINIALL | Доступно з memcache 2.0.2. |
| [memcache.maxfailoverattempts](memcache.ini.md#ini.memcache.max-failover-attempts) | "20" | PHPINIALL | Доступно з memcache 2.1.0. |
| [memcache.chunksize](memcache.ini.md#ini.memcache.chunk-size) | "8192" | PHPINIALL | Доступно з memcache 2.0.2. |
| [memcache.defaultport](memcache.ini.md#ini.memcache.default-port) | "11211" | PHPINIALL | Доступно з memcache 2.0.2. |
| [memcache.hashstrategy](memcache.ini.md#ini.memcache.hash-strategy) | "standard" | PHPINIALL | Доступно з memcache 2.2.0. |
| [memcache.hashfunction](memcache.ini.md#ini.memcache.hash-function) | "crc32" | PHPINIALL | Доступно з memcache 2.2.0. |
| [memcache.protocol](memcache.ini.md#ini.memcache.protocol) | ascii | \>PHPINIALL | Підтримується з memcache 3.0.0 |
| [memcache.redundancy](memcache.ini.md#ini.memcache.redundancy) |  | \>PHPINIALL | Підтримується з memcache 3.0.0 |
| [memcache.sessionredundancy](memcache.ini.md#ini.memcache.session-redundancy) |  | \>PHPINIALL | Підтримується з memcache 3.0.0 |
| [memcache.compressthreshold](memcache.ini.md#ini.memcache.compress-threshold) |  | \>PHPINIALL | Підтримується з memcache 3.0.3 |
| [memcache.locktimeout](memcache.ini.md#ini.memcache.lock-timeout) |  | \>PHPINIALL | Підтримується з memcache 3.0.4 |
| [memorylimit](ini.core.md#ini.memory-limit) | "128M" | PHPINIALL |  |
| [mysql.allowlocalinfile](mysql.configuration.md#ini.mysql.allow-local-infile) | "1" | PHPINISYSTEM |  |
| [mysql.allowpersistent](mysql.configuration.md#ini.mysql.allow-persistent) | "1" | PHPINISYSTEM |  |
| [mysql.maxpersistent](mysql.configuration.md#ini.mysql.max-persistent) | "-1" | PHPINISYSTEM |  |
| [mysql.maxlinks](mysql.configuration.md#ini.mysql.max-links) | "-1" | PHPINISYSTEM |  |
| [mysql.tracemode](mysql.configuration.md#ini.mysql.trace-mode) | "0" | PHPINIALL |  |
| [mysql.defaultport](mysql.configuration.md#ini.mysql.default-port) | NULL | PHPINIALL |  |
| [mysql.defaultsocket](mysql.configuration.md#ini.mysql.default-socket) | NULL | PHPINIALL |  |
| [mysql.defaulthost](mysql.configuration.md#ini.mysql.default-host) | NULL | PHPINIALL |  |
| [mysql.defaultuser](mysql.configuration.md#ini.mysql.default-user) | NULL | PHPINIALL |  |
| [mysql.defaultpassword](mysql.configuration.md#ini.mysql.default-password) | NULL | PHPINIALL |  |
| [mysql.connecttimeout](mysql.configuration.md#ini.mysql.connect-timeout) | "60" | PHPINIALL |  |
| [mysqli.allowlocalinfile](mysqli.configuration.md#ini.mysqli.allow-local-infile) | "0" | PHPINISYSTEM | До PHP 7.2.16 та 7.3.3 значенням за умовчанням було "1". |
| [mysqli.localinfiledirectory](mysqli.configuration.md#ini.mysqli.local-infile-directory) |  | PHPINISYSTEM | Доступно з PHP 8.1.0. |
| [mysqli.allowpersistent](mysqli.configuration.md#ini.mysqli.allow-persistent) | "1" | PHPINISYSTEM |  |
| [mysqli.maxpersistent](mysqli.configuration.md#ini.mysqli.max-persistent) | "-1" | PHPINISYSTEM |  |
| [mysqli.maxlinks](mysqli.configuration.md#ini.mysqli.max-links) | "-1" | PHPINISYSTEM |  |
| [mysqli.defaultport](mysqli.configuration.md#ini.mysqli.default-port) | "3306" | PHPINIALL |  |
| [mysqli.defaultsocket](mysqli.configuration.md#ini.mysqli.default-socket) | NULL | PHPINIALL |  |
| [mysqli.defaulthost](mysqli.configuration.md#ini.mysqli.default-host) | NULL | PHPINIALL |  |
| [mysqli.defaultuser](mysqli.configuration.md#ini.mysqli.default-user) | NULL | PHPINIALL |  |
| [mysqli.defaultпв](mysqli.configuration.md#ini.mysqli.default-pw) | NULL | PHPINIALL |  |
| [mysqli.reconnect](mysqli.configuration.md#ini.mysqli.reconnect) | "0" | PHPINISYSTEM |  |
| [mysqli.rollbackвінcachedplink](mysqli.configuration.md#ini.mysqli.rollback-on-cached-plink) | "0" | PHPINISYSTEM |  |
| [mysqlnd.collectstatistics](mysqlnd.config.md#ini.mysqlnd.collect-statistics) | "1" | PHPINISYSTEM |  |
| [mysqlnd.collectmemorystatistics](mysqlnd.config.md#ini.mysqlnd.collect-memory-statistics) | "0" | PHPINISYSTEM |  |
| [mysqlnd.debug](mysqlnd.config.md#ini.mysqlnd.debug) | "" | PHPINISYSTEM |  |
| [mysqlnd.logmask](mysqlnd.config.md#ini.mysqlnd.log-mask) |  | PHPINIALL |  |
| [mysqlnd.mempooldefaultsize](mysqlnd.config.md#ini.mysqlnd.mempool-default-size) |  | PHPINIALL |  |
| [mysqlnd.netreadtimeout](mysqlnd.config.md#ini.mysqlnd.net-read-timeout) | "86400" | PHPINIALL | До PHP 7.2.0 значенням за промовчанням "31536000", а місцем зміни було **`PHP_INI_SYSTEM`** |
| [mysqlnd.netcmdbuffersize](mysqlnd.config.md#ini.mysqlnd.net-cmd-buffer-size) | 5.3.0 - "2048"; 5.3.1 - "4096" | PHPINISYSTEM |  |
| [mysqlnd.netreadbuffersize](mysqlnd.config.md#ini.mysqlnd.net-read-buffer-size) | "32768" | PHPINISYSTEM |  |
| [mysqlnd.sha256serverpublickey](mysqlnd.config.md#ini.mysqlnd.sha256-server-public-key) | "" | PHPINIPERDIR |  |
| [mysqlnd.tracealloc](mysqlnd.config.md#ini.mysqlnd.trace-alloc) | "" | PHPINISYSTEM |  |
| [mysqlnd.fetchdatacopy](mysqlnd.config.md#ini.mysqlnd.fetch_data_copy) |  | PHPINIALL |  |
| [oci8.connectionclass](oci8.configuration.md#ini.oci8.connection-class) | "" | PHPINIALL | Доступна з версії PECL OCI8 1.3. |
| [oci8.defaultprefetch](oci8.configuration.md#ini.oci8.default-prefetch) | "100" | PHPINISYSTEM | Доступна з версії PECL OCI8 1.1. |
| [oci8.events](oci8.configuration.md#ini.oci8.events) | Off | PHPINISYSTEM | Доступна з версії PECL OCI8 1.3. |
| [oci8.maxpersistent](oci8.configuration.md#ini.oci8.max-persistent) | "-1" | PHPINISYSTEM | Доступна з версії PECL OCI8 1.1. Оголошена застарілою починаючи з PHP 8.1.0. |
| [oci8.oldociclosesemantics](oci8.configuration.md#ini.oci8.old-oci-close-semantics) | Off | PHPINISYSTEM | Доступна з версії PECL OCI8 1.1. |
| [oci8.persistenttimeout](oci8.configuration.md#ini.oci8.persistent-timeout) | "-1" | PHPINISYSTEM | Доступна з версії PECL OCI8 1.1. |
| [oci8.pinginterval](oci8.configuration.md#ini.oci8.ping-interval) | "60" | PHPINISYSTEM | Доступна з версії PECL OCI8 1.1. |
| [oci8.prefetchlobsize](oci8.configuration.md#ini.oci8.prefetch-lob-size) | "0" | PHPINISYSTEM | Доступна з версії PECL OCI8 3.2. |
| [oci8.privilegedconnect](oci8.configuration.md#ini.oci8.privileged-connect) | Off | PHPINISYSTEM | Доступна з версії PECL OCI8 1.1. |
| [oci8.statementcachesize](oci8.configuration.md#ini.oci8.statement-cache-size) | "20" | PHPINISYSTEM | Доступна з версії PECL OCI8 1.1. |
| [odbc.defaultдб](odbc.configuration.md#ini.uodbc.default-db) | NULL | PHPINIALL |  |
| [odbc.defaultuser](odbc.configuration.md#ini.uodbc.default-user) | NULL | PHPINIALL |  |
| [odbc.defaultпв](odbc.configuration.md#ini.uodbc.default-pw) | NULL | PHPINIALL |  |
| [odbc.allowpersistent](odbc.configuration.md#ini.uodbc.allow-persistent) | "1" | PHPINISYSTEM |  |
| [odbc.checkpersistent](odbc.configuration.md#ini.uodbc.check-persistent) | "1" | PHPINISYSTEM |  |
| [odbc.maxpersistent](odbc.configuration.md#ini.uodbc.max-persistent) | "-1" | PHPINISYSTEM |  |
| [odbc.maxlinks](odbc.configuration.md#ini.uodbc.max-links) | "-1" | PHPINISYSTEM |  |
| [odbc.defaultlrl](odbc.configuration.md#ini.uodbc.defaultlrl) | "4096" | PHPINIALL |  |
| [odbc.defaultbinmode](odbc.configuration.md#ini.uodbc.defaultbinmode) | "1" | PHPINIALL |  |
| [odbc.defaultcursortype](odbc.configuration.md#ini.uodbc.defaultcursortype) | "3" | PHPINIALL |  |
| [opcache.enable](opcache.configuration.md#ini.opcache.enable) | "1" | PHPINIALL |  |
| [opcache.enablecli](opcache.configuration.md#ini.opcache.enable-cli) | "0" | PHPINISYSTEM | У версіях з PHP 7.1.2 до 7.1.6 включно, значення за замовчуванням "1" (включено) |
| [opcache.memoryconsumption](opcache.configuration.md#ini.opcache.memory-consumption) | "128" | PHPINISYSTEM |  |
| [opcache.internedstringsbuffer](opcache.configuration.md#ini.opcache.interned-strings-buffer) | "8" | PHPINISYSTEM |  |
| [opcache.maxacceleratedfiles](opcache.configuration.md#ini.opcache.max-accelerated-files) | "10000" | PHPINISYSTEM |  |
| [opcache.maxwastedpercentage](opcache.configuration.md#ini.opcache.max-wasted-percentage) | "5" | PHPINISYSTEM |  |
| [opcache.usecwd](opcache.configuration.md#ini.opcache.use-cwd) | "1" | PHPINISYSTEM |  |
| [opcache.validatetimestamps](opcache.configuration.md#ini.opcache.validate-timestamps) | "1" | PHPINIALL |  |
| [opcache.revalidatefreq](opcache.configuration.md#ini.opcache.revalidate-freq) | "2" | PHPINIALL |  |
| [opcache.revalidatepath](opcache.configuration.md#ini.opcache.revalidate-path) | "0" | PHPINIALL |  |
| [opcache.savecomments](opcache.configuration.md#ini.opcache.save-comments) | "1" | PHPINISYSTEM |  |
| [opcache.fastshutdown](opcache.configuration.md#ini.opcache.fast-shutdown) | "0" | PHPINISYSTEM |  |
| [opcache.enablefileoverride](opcache.configuration.md#ini.opcache.enable-file-override) | "0" | PHPINISYSTEM |  |
| [opcache.optimizationlevel](opcache.configuration.md#ini.opcache.optimization-level) | "0x7FFEBFFF" | PHPINISYSTEM | До PHP 7.3.0 було 0x7FFFBFFF |
| [opcache.inheritedhack](opcache.configuration.md#ini.opcache.inherited-hack) | "1" | PHPINISYSTEM | Вилучено у PHP 7.3.0 |
| [opcache.dupsfix](opcache.configuration.md#ini.opcache.dups-fix) | "0" | PHPINIALL |  |
| [opcache.blacklistfilename](opcache.configuration.md#ini.opcache.blacklist-filename) | "" | PHPINISYSTEM |  |
| [opcache.maxfilesize](opcache.configuration.md#ini.opcache.max-file-size) | "0" | PHPINISYSTEM |  |
| [opcache.consistencychecks](opcache.configuration.md#ini.opcache.consistency-checks) | "0" | PHPINIALL |  |
| [opcache.forcerestarttimeout](opcache.configuration.md#ini.opcache.force-restart-timeout) | "180" | PHPINISYSTEM |  |
| [opcache.errorlog](opcache.configuration.md#ini.opcache.error-log) | "" | PHPINISYSTEM |  |
| [opcache.logverbositylevel](opcache.configuration.md#ini.opcache.log-verbosity-level) | "1" | PHPINISYSTEM |  |
| [opcache.recordwarnings](opcache.configuration.md#ini.opcache.record-warnings) | "0" | PHPINISYSTEM | Доступно з PHP 8.0.0. |
| [opcache.preferredmemorymodel](opcache.configuration.md#ini.opcache.preferred-memory-model) | "" | PHPINISYSTEM |  |
| [opcache.protectmemory](opcache.configuration.md#ini.opcache.protect-memory) | "0" | PHPINISYSTEM |  |
| [opcache.mmapbase](opcache.configuration.md#ini.opcache.mmap-base) | **`null`** | PHPINISYSTEM |  |
| [opcache.restrictapi](opcache.configuration.md#ini.opcache.restrict-api) | "" | PHPINISYSTEM |  |
| [opcache.fileupdateprotection](opcache.configuration.md#ini.opcache.file_update_protection) | "2" | PHPINIALL |  |
| [opcache.hugecodepages](opcache.configuration.md#ini.opcache.huge_code_pages) | "0" | PHPINISYSTEM |  |
| [opcache.lockfilepath](opcache.configuration.md#ini.opcache.lockfile_path) | "/tmp" | PHPINISYSTEM |  |
| [opcache.optdebuglevel](opcache.configuration.md#ini.opcache.opt_debug_level) | "0" | PHPINISYSTEM | Доступно з PHP 7.1.0 |
| [opcache.filecache](opcache.configuration.md#ini.opcache.file-cache) | NULL | PHPINISYSTEM |  |
| [opcache.filecacheonly](opcache.configuration.md#ini.opcache.file-cache-only) | "0" | PHPINISYSTEM |  |
| [opcache.filecacheconsistencychecks](opcache.configuration.md#ini.opcache.file-cache-consistency-checks) | "1" | PHPINISYSTEM |  |
| [opcache.filecachefallback](opcache.configuration.md#ini.opcache.file-cache-fallback) | "1" | PHPINISYSTEM |  |
| [opcache.validatepermission](opcache.configuration.md#ini.opcache.validate-permission) | "0" | PHPINISYSTEM | Доступно з PHP 7.0.14 |
| [opcache.validateroot](opcache.configuration.md#ini.opcache.validate-root) | "0" | PHPINISYSTEM | Доступно з PHP 7.0.14 |
| [opcache.preload](opcache.configuration.md#ini.opcache.preload) | "" | PHPINISYSTEM | Доступно з PHP 7.4.0 |
| [opcache.preloaduser](opcache.configuration.md#ini.opcache.preload-user) | "" | PHPINISYSTEM | Доступно з PHP 7.4.0 |
| [opcache.cacheід](opcache.configuration.md#ini.opcache.cache-id) | "" | PHPINISYSTEM | Тільки Windows. Доступно з PHP 7.4.0 |
| [opcache.jit](opcache.configuration.md#ini.opcache.jit) | "tracing" | PHPINIALL | Доступно з PHP 8.0.0 |
| [opcache.jitbuffersize](opcache.configuration.md#ini.opcache.jit-buffer-size) | "0" | PHPINISYSTEM | Доступно з PHP 8.0.0 |
| [opcache.jitdebug](opcache.configuration.md#ini.opcache.jit-debug) | "0" | PHPINIALL | Доступно з PHP 8.0.0 |
| [opcache.jitbisectlimit](opcache.configuration.md#ini.opcache.jit-bisect-limit) | "0" | PHPINIALL | Доступно з PHP 8.0.0 |
| [opcache.jitprofthreshold](opcache.configuration.md#ini.opcache.jit-prof-threshold) | "0.005" | PHPINIALL | Доступно з PHP 8.0.0 |
| [opcache.jitmaxroottraces](opcache.configuration.md#ini.opcache.jit-max-root-traces) | "1024" | PHPINISYSTEM | Доступно з PHP 8.0.0 |
| [opcache.jitmaxsidetraces](opcache.configuration.md#ini.opcache.jit-max-side-traces) | "128" | PHPINISYSTEM | Доступно з PHP 8.0.0 |
| [opcache.jitmaxexitcounters](opcache.configuration.md#ini.opcache.jit-max-exit-counters) | "8192" | PHPINISYSTEM | Доступно з PHP 8.0.0 |
| [opcache.jithotloop](opcache.configuration.md#ini.opcache.jit-hot-loop) | "64" | PHPINISYSTEM | Доступно з PHP 8.0.0 |
| [opcache.jithotfunc](opcache.configuration.md#ini.opcache.jit-hot-func) | "127" | PHPINISYSTEM | Доступно з PHP 8.0.0 |
| [opcache.jithotreturn](opcache.configuration.md#ini.opcache.jit-hot-return) | "8" | PHPINISYSTEM | Доступно з PHP 8.0.0 |
| [opcache.jithotsideexit](opcache.configuration.md#ini.opcache.jit-hot-side-exit) | "8" | PHPINISYSTEM | Доступно з PHP 8.0.0 |
| [opcache.jitblacklistroottrace](opcache.configuration.md#ini.opcache.jit-blacklist-root-trace) | "16" | PHPINIALL | Доступно з PHP 8.0.0 |
| [opcache.jitblacklistsidetrace](opcache.configuration.md#ini.opcache.jit-blacklist-side-trace) | "8" | PHPINIALL | Доступно з PHP 8.0.0 |
| [opcache.jitmaxloopunrolls](opcache.configuration.md#ini.opcache.jit-max-loop-unrolls) | "8" | PHPINIALL | Доступно з PHP 8.0.0 |
| [opcache.jitmaxrecursivecalls](opcache.configuration.md#ini.opcache.jit-max-recursive-calls) | "2" | PHPINIALL | Доступно з PHP 8.0.0 |
| [opcache.jitmaxrecursivereturns](opcache.configuration.md#ini.opcache.jit-max-recursive-return) | "2" | PHPINIALL | Доступно з PHP 8.0.0 |
| [opcache.jitmaxpolymorphiccalls](opcache.configuration.md#ini.opcache.jit-max-polymorphic-calls) | "2" | PHPINIALL | Доступно з PHP 8.0.0 |
| [openbasedir](ini.core.md#ini.open-basedir) | NULL | PHPINIALL |  |
| [outputbuffering](outcontrol.configuration.md#ini.output-buffering) | "0" | PHPINIPERDIR |  |
| [outputhandler](outcontrol.configuration.md#ini.output-handler) | NULL | PHPINIPERDIR |  |
| [pcre.backtracklimit](pcre.configuration.md#ini.pcre.backtrack-limit) | "1000000" | PHPINIALL |  |
| [pcre.recursionlimit](pcre.configuration.md#ini.pcre.recursion-limit) | "100000" | PHPINIALL |  |
| [pcre.jit](pcre.configuration.md#ini.pcre.jit) | "1" | PHPINIALL |  |
| [pdo.dsn.](pdo.configuration.md#ini.pdo.dsn) |  | тільки php.ini |  |
| [pdoodbc.connectionpooling](ref.pdo-odbc.md#ini.pdo-odbc.connection-pooling) | "strict" | PHPINIALL |  |
| [pdoodbc.db2instancename](ref.pdo-odbc.md#ini.pdo-odbc.db2-instance-name) | NULL | PHPINISYSTEM | Ця можливість застаріла та *буде* обов'язково *видалено* в майбутньому. |
| [pgsql.allowpersistent](pgsql.configuration.md#ini.pgsql.allow-persistent) | "1" | PHPINISYSTEM |  |
| [pgsql.maxpersistent](pgsql.configuration.md#ini.pgsql.max-persistent) | "-1" | PHPINISYSTEM |  |
| [pgsql.maxlinks](pgsql.configuration.md#ini.pgsql.max-links) | "-1" | PHPINISYSTEM |  |
| [pgsql.autoresetpersistent](pgsql.configuration.md#ini.pgsql.auto-reset-persistent) | "0" | PHPINISYSTEM |  |
| [pgsql.ignorenotice](pgsql.configuration.md#ini.pgsql.ignore-notice) | "0" | PHPINIALL |  |
| [pgsql.lognotice](pgsql.configuration.md#ini.pgsql.log-notice) | "0" | PHPINIALL |  |
| [phar.readonly](phar.configuration.md#ini.phar.readonly) | "1" | PHPINIALL |  |
| [phar.requirehash](phar.configuration.md#ini.phar.require-hash) | "1" | PHPINIALL |  |
| [phar.cachelist](phar.configuration.md#ini.phar.cache-list) | "" | PHPINISYSTEM |  |
| [postmaxsize](ini.core.md#ini.post-max-size) | "8M" | PHPINIPERDIR |  |
| [precision](ini.core.md#ini.precision) | "14" | PHPINIALL |  |
| [realpathcachesize](ini.core.md#ini.realpath-cache-size) | "16K" | PHPINISYSTEM |  |
| [realpathcachettl](ini.core.md#ini.realpath-cache-ttl) | "120" | PHPINISYSTEM |  |
| [registerargcargv](ini.core.md#ini.register-argc-argv) | "1" | PHPINIPERDIR |  |
| [reportmemleaks](errorfunc.configuration.md#ini.report-memleaks) | "1" | PHPINIALL |  |
| reportzenddebug | "1" | PHPINIALL |  |
| [requestorder](ini.core.md#ini.request-order) | "" | PHPINIPERDIR |  |
| [runkit.superglobal](runkit7.configuration.md#ini.runkit7.superglobal) | "" | PHPINIPERDIR |  |
| [runkit.internaloverride](runkit7.configuration.md#ini.runkit7.internal-override) | "0" | PHPINISYSTEM |  |
| [sendmailfrom](mail.configuration.md#ini.sendmail-from) | NULL | PHPINIALL |  |
| [sendmailpath](mail.configuration.md#ini.sendmail-path) | "/usr/sbin/sendmail -t -i" | PHPINISYSTEM |  |
| [serializeprecision](ini.core.md#ini.serialize-precision) | "-1" | PHPINIALL | До PHP 7.1.0, значення за промовчанням 17. |
| [session.savepath](session.configuration.md#ini.session.save-path) | "" | PHPINIALL |  |
| [session.name](session.configuration.md#ini.session.name) | "PHPSESSID" | PHPINIALL |  |
| [session.savehandler](session.configuration.md#ini.session.save-handler) | "files" | PHPINIALL |  |
| [session.autostart](session.configuration.md#ini.session.auto-start) | "0" | PHPINIPERDIR |  |
| [session.gcprobability](session.configuration.md#ini.session.gc-probability) | "1" | PHPINIALL |  |
| [session.gcdivisor](session.configuration.md#ini.session.gc-divisor) | "100" | PHPINIALL |  |
| [session.gcmaxlifetime](session.configuration.md#ini.session.gc-maxlifetime) | "1440" | PHPINIALL |  |
| [session.serializehandler](session.configuration.md#ini.session.serialize-handler) | "php" | PHPINIALL |  |
| [session.cookielifetime](session.configuration.md#ini.session.cookie-lifetime) | "0" | PHPINIALL |  |
| [session.cookiepath](session.configuration.md#ini.session.cookie-path) | "/" | PHPINIALL |  |
| [session.cookiedomain](session.configuration.md#ini.session.cookie-domain) | "" | PHPINIALL |  |
| [session.cookiesecure](session.configuration.md#ini.session.cookie-secure) | "0" | PHPINIALL | До PHP 7.2.0 значення за промовчанням було `""` |
| [session.cookiehttponly](session.configuration.md#ini.session.cookie-httponly) | "0" | PHPINIALL | До PHP 7.2.0 значення за промовчанням було `""` |
| [session.cookiesamesite](session.configuration.md#ini.session.cookie-samesite) | "" | PHPINIALL | Доступна з PHP 7.3.0. |
| [session.usestrictmode](session.configuration.md#ini.session.use-strict-mode) | "0" | PHPINIALL |  |
| [session.usecookies](session.configuration.md#ini.session.use-cookies) | "1" | PHPINIALL |  |
| [session.useonlycookies](session.configuration.md#ini.session.use-only-cookies) | "1" | PHPINIALL |  |
| [session.referercheck](session.configuration.md#ini.session.referer-check) | "" | PHPINIALL |  |
| [session.cachelimiter](session.configuration.md#ini.session.cache-limiter) | "nocache" | PHPINIALL |  |
| [session.cacheexpire](session.configuration.md#ini.session.cache-expire) | "180" | PHPINIALL |  |
| [session.usetranssid](session.configuration.md#ini.session.use-trans-sid) | "0" | PHPINIALL |  |
| [session.transsidtags](session.configuration.md#ini.session.trans-sid-tags) | "a=href,area=href,frame=src,form=" | PHPINIALL | Доступна з PHP 7.1.0. |
| [session.transsidhosts](session.configuration.md#ini.session.trans-sid-hosts) | `$_SERVER['HTTP_HOST']` | PHPINIALL | Доступна з PHP 7.1.0. |
| [session.sidlength](session.configuration.md#ini.session.sid-length) | "32" | PHPINIALL | Доступна з PHP 7.1.0. |
| [session.sidbitspercharacter](session.configuration.md#ini.session.sid-bits-per-character) | "4" | PHPINIALL | Доступна з PHP 7.1.0. |
| [session.uploadprogress.enabled](session.configuration.md#ini.session.upload-progress.enabled) | "1" | PHPINIPERDIR |  |
| [session.uploadprogress.cleanup](session.configuration.md#ini.session.upload-progress.cleanup) | "1" | PHPINIPERDIR |  |
| [session.uploadprogress.prefix](session.configuration.md#ini.session.upload-progress.prefix) | "uploadprogress" | PHPINIPERDIR |  |
| [session.uploadprogress.name](session.configuration.md#ini.session.upload-progress.name) | "PHPSESSIONUPLOADPROGRESS" | PHPINIPERDIR |  |
| [session.uploadprogress.freq](session.configuration.md#ini.session.upload-progress.freq) | "1%" | PHPINIPERDIR |  |
| [session.uploadprogress.minfreq](session.configuration.md#ini.session.upload-progress.min-freq) | "1" | PHPINIPERDIR |  |
| [session.lazywrite](session.configuration.md#ini.session.lazy-write) | "1" | PHPINIALL |  |
| [session.hashfunction](session.configuration.md#ini.session.hash-function) | "0" | PHPINIALL | Видалено в PHP 7.1.0. |
| [session.hashbitspercharacter](session.configuration.md#ini.session.hash-bits-per-character) | "4" | PHPINIALL | Видалено в PHP 7.1.0. |
| [session.entropyfile](session.configuration.md#ini.session.entropy-file) | "" | PHPINIALL | Видалено в PHP 7.1.0. |
| [session.entropylength](session.configuration.md#ini.session.entropy-length) | "0" | PHPINIALL | Видалено в PHP 7.1.0 |
| [shortopentag](ini.core.md#ini.short-open-tag) | "1" | PHPINIPERDIR |  |
| [SMTP](mail.configuration.md#ini.smtp) | "localhost" | PHPINIALL |  |
| [smtpport](mail.configuration.md#ini.smtp-port) | "25" | PHPINIALL |  |
| [soap.wsdlcacheenabled](soap.configuration.md#ini.soap.wsdl-cache-enabled) |  | PHPINIALL |  |
| [soap.wsdlcachedir](soap.configuration.md#ini.soap.wsdl-cache-dir) | /tmp | PHPINIALL |  |
| [soap.wsdlcachettl](soap.configuration.md#ini.soap.wsdl-cache-ttl) |  | PHPINIALL |  |
| [soap.wsdlcache](soap.configuration.md#ini.soap.wsdl-cache) |  | PHPINIALL |  |
| [soap.wsdlcachelimit](soap.configuration.md#ini.soap.wsdl-cache-limit) |  | PHPINIALL |  |
| [sql.safemode](ini.core.md#ini.sql.safe-mode) | "0" | PHPINISYSTEM |  |
| [sqlite3.extensiondir](sqlite3.configuration.md#ini.sqlite3.extension-dir) | "" | PHPINISYSTEM |  |
| [sqlite3.defensive](sqlite3.configuration.md#ini.sqlite3.defensive) |  | PHPINISYSTEM | Доступно з PHP 7.2.17 та 7.3.4 для libsqlite ≥ 3.26.0. |
| [syslog.facility](errorfunc.configuration.md#ini.syslog.facility) | "LOGUSER" | PHPINISYSTEM | Доступно, починаючи з PHP 7.3.0. |
| [syslog.filter](errorfunc.configuration.md#ini.syslog.filter) | "no-ctrl" | PHPINIALL | Доступно, починаючи з PHP 7.3.0. |
| [syslog.ident](errorfunc.configuration.md#ini.syslog.ident) | "php" | PHPINISYSTEM | Доступно, починаючи з PHP 7.3.0. |
| systempdir | "" | PHPINISYSTEM |  |
| [sysvshm.initmem](sem.configuration.md#ini.sysvshm.init-mem) |  | PHPINISYSTEM |  |
| [tidy.defaultconfig](tidy.configuration.md#ini.tidy.default-config) | "" | PHPINISYSTEM |  |
| [tidy.cleanoutput](tidy.configuration.md#ini.tidy.clean-output) | "0" | PHPINIUSER |  |
| [trackerrors](errorfunc.configuration.md#ini.track-errors) | "0" | PHPINIALL | Оголошено застарілим у PHP 7.2.0, видалено у PHP 8.0.0. |
| [unserializecallbackfunc](var.configuration.md#ini.unserialize-callback-func) | NULL | PHPINIALL |  |
| uploadprogress.file.filenametemplate | "/tmp/upt%s.txt" | PHPINIALL |  |
| [uploadmaxfilesize](ini.core.md#ini.upload-max-filesize) | "2M" | PHPINIPERDIR |  |
| [maxfileuploads](ini.core.md#ini.max-file-uploads) |  | PHPINISYSTEM |  |
| [uploadtmpdir](ini.core.md#ini.upload-tmp-dir) | NULL | PHPINISYSTEM |  |
| [urlrewriter.tags](outcontrol.configuration.md#ini.url-rewriter.tags) | "a=href,area=href,frame=src,form=,fieldset=" | PHPINIALL |  |
| [useragent](filesystem.configuration.md#ini.user-agent) | NULL | PHPINIALL |  |
| [userdir](ini.core.md#ini.user-dir) | NULL | PHPINISYSTEM |  |
| [userini.cachettl](ini.core.md#ini.user-ini.cache-ttl) | "300" | PHPINISYSTEM |  |
| [userini.filename](ini.core.md#ini.user-ini.filename) | ".user.ini" | PHPINISYSTEM |  |
| [uopz.disable](uopz.configuration.md#ini.uopz.disable) | "0" | PHPINISYSTEM | Доступно з uopz 5.0.2 |
| [uopz.exit](uopz.configuration.md#ini.uopz.exit) | "0" | PHPINISYSTEM | Доступно з uopz 6.0.1 |
| [uopz.overloads](uopz.configuration.md#ini.uopz.overloads) | "1" | PHPINISYSTEM | Доступно з uopz 2.0.2. Видалено з uopz 5.0.0. |
| [variablesorder](ini.core.md#ini.variables-order) | "EGPCS" | PHPINIPERDIR |  |
| vld.active | "0" | PHPINISYSTEM |  |
| vld.execute | "1" | PHPINISYSTEM | Доступно з vld 0.8.0. |
| vld.skipappend | "0" | PHPINISYSTEM | Доступно з vld 0.8.0. |
| vld.skipprepend | "0" | PHPINISYSTEM | Доступно з vld 0.8.0. |
| [windows.showcrtwarning](ini.core.md#ini.windows-show-crt-warning) | "0" | PHPINIALL |  |
| [xbithack](apache.configuration.md#ini.xbithack) | "0" | PHPINIALL |  |
| [xmlrpcerrors](errorfunc.configuration.md#ini.xmlrpc-errors) | "0" | PHPINISYSTEM |  |
| [xmlrpcerrornumber](errorfunc.configuration.md#ini.xmlrpc-error-number) | "0" | PHPINIALL |  |
| yaz.keepalive | "120" | PHPINIALL |  |
| yaz.logmask | NULL | PHPINIALL | Доступно починаючи з yaz 1.0.3. |
| [zend.assertions](ini.core.md#ini.zend.assertions) | "1" | PHPINIALL |  |
| [zend.detectunicode](ini.core.md#ini.zend.detect-unicode) | "1" | PHPINIALL |  |
| [zend.enableгк](info.configuration.md#ini.zend.enable-gc) | "1" | PHPINIALL |  |
| [zend.multibyte](ini.core.md#ini.zend.multibyte) | "0" | PHPINIPERDIR |  |
| [zend.scriptencoding](ini.core.md#ini.zend.script-encoding) | NULL | PHPINIALL |  |
| [zend.signalcheck](ini.core.md#ini.zend.signal-check) | "0" | PHPINISYSTEM |  |
| [zendextension](ini.core.md#ini.zend-extension) | NULL | Тільки php.ini |  |
| [zlib.outputcompression](zlib.configuration.md#ini.zlib.output-compression) | "0" | PHPINIALL |  |
| [zlib.outputcompressionlevel](zlib.configuration.md#ini.zlib.output-compression-level) | "-1" | PHPINIALL |  |
| [zlib.outputhandler](zlib.configuration.md#ini.zlib.output-handler) | "" | PHPINIALL |  |
