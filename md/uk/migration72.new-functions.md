---
navigation:
  - migration72.new-features.html: '" Нові можливості'
  - migration72.constants.html: Нові глобальні константи »
  - index.html: PHP Manual
  - migration72.html: Миграция с PHP 7.1.x на PHP 7.2.x
title: Нові функції
---
## Нові функції

### Ядро PHP

-   [streamisatty()](function.stream-isatty.md)
-   [sapiwindowsvt100support()](function.sapi-windows-vt100-support.md)

### [SPL](book.spl.md)

-   [splobjectid()](function.spl-object-id.md)

### [DOM](book.dom.md)

-   [DomNodeList::count()](domnodelist.count.md)
-   [DOMNamedNodeMap::count()](domnamednodemap.count.md)

### [FTP](book.ftp.md)

-   [ftpappend()](function.ftp-append.md)

### [ДД](book.image.md)

-   [imagesetclip()](function.imagesetclip.md)
-   [imagegetclip()](function.imagegetclip.md)
-   [imageopenpolygon()](function.imageopenpolygon.md)
-   [imageresolution()](function.imageresolution.md)
-   [imagecreatefrombmp()](function.imagecreatefrombmp.md)
-   [imagebmp()](function.imagebmp.md)

### [Hash](book.hash.md)

-   [hashhmacalgos()](function.hash-hmac-algos.md)

### [LDAP](book.ldap.md)

-   [ldapparseexop()](function.ldap-parse-exop.md)
-   [ldapexop()](function.ldap-exop.md)
-   [ldapexoppasswd()](function.ldap-exop-passwd.md)
-   [ldapexopwhoami()](function.ldap-exop-whoami.md)

### [Багатобайтні рядки](book.mbstring.md)

-   [мбchr()](function.mb-chr.md)
-   [мбord()](function.mb-ord.md)
-   [мбscrub()](function.mb-scrub.md)

### [Oracle OCI8](book.oci8.md)

-   [ociregistertafcallback()](function.oci-register-taf-callback.md)
-   [ociunregistertafcallback()](function.oci-unregister-taf-callback.md)

### [Сокети](book.sockets.md)

-   [socketaddrinfolookup()](function.socket-addrinfo-lookup.md)
-   [socketaddrinfoconnect()](function.socket-addrinfo-connect.md)
-   [socketaddrinfobind()](function.socket-addrinfo-bind.md)
-   [socketaddrinfoexplain()](function.socket-addrinfo-explain.md)

### [Sodium](book.sodium.md)

-   [sodiumadd()](function.sodium-add.md)
-   [sodiumbin2hex()](function.sodium-bin2hex.md)
-   [sodiumcompare()](function.sodium-compare.md)
-   [sodiumcryptoaeadaes256gcmdecrypt()](function.sodium-crypto-aead-aes256gcm-decrypt.md)
-   [sodiumcryptoaeadaes256gcmencrypt()](function.sodium-crypto-aead-aes256gcm-encrypt.md)
-   [sodiumcryptoaeadaes256gcmісavailable()](function.sodium-crypto-aead-aes256gcm-is-available.md)
-   [sodiumcryptoaeadaes256gcmkeygen()](function.sodium-crypto-aead-aes256gcm-keygen.md)
-   [sodiumcryptoaeadchacha20poly1305decrypt()](function.sodium-crypto-aead-chacha20poly1305-decrypt.md)
-   [sodiumcryptoaeadchacha20poly1305encrypt()](function.sodium-crypto-aead-chacha20poly1305-encrypt.md)
-   [sodiumcryptoaeadchacha20poly1305ietfdecrypt()](function.sodium-crypto-aead-chacha20poly1305-ietf-decrypt.md)
-   [sodiumcryptoaeadchacha20poly1305ietfencrypt()](function.sodium-crypto-aead-chacha20poly1305-ietf-encrypt.md)
-   [sodiumcryptoaeadchacha20poly1305ietfkeygen()](function.sodium-crypto-aead-chacha20poly1305-ietf-keygen.md)
-   [sodiumcryptoaeadchacha20poly1305keygen()](function.sodium-crypto-aead-chacha20poly1305-keygen.md)
-   [sodiumcryptoauthkeygen()](function.sodium-crypto-auth-keygen.md)
-   [sodiumcryptoauthverify()](function.sodium-crypto-auth-verify.md)
-   [sodiumcryptoauth()](function.sodium-crypto-auth.md)
-   [sodiumcryptoboxkeypairfromsecretkeyandpublickey()](function.sodium-crypto-box-keypair-from-secretkey-and-publickey.md)
-   [sodiumcryptoboxkeypair()](function.sodium-crypto-box-keypair.md)
-   [sodiumcryptoboxopen()](function.sodium-crypto-box-open.md)
-   [sodiumcryptoboxpublickeyfromsecretkey()](function.sodium-crypto-box-publickey-from-secretkey.md)
-   [sodiumcryptoboxpublickey()](function.sodium-crypto-box-publickey.md)
-   [sodiumcryptoboxsealopen()](function.sodium-crypto-box-seal-open.md)
-   [sodiumcryptoboxseal()](function.sodium-crypto-box-seal.md)
-   [sodiumcryptoboxsecretkey()](function.sodium-crypto-box-secretkey.md)
-   [sodiumcryptoboxseedkeypair()](function.sodium-crypto-box-seed-keypair.md)
-   [sodiumcryptobox()](function.sodium-crypto-box.md)
-   [sodiumcryptogenerichashfinal()](function.sodium-crypto-generichash-final.md)
-   [sodiumcryptogenerichashinit()](function.sodium-crypto-generichash-init.md)
-   [sodiumcryptogenerichashkeygen()](function.sodium-crypto-generichash-keygen.md)
-   [sodiumcryptogenerichashupdate()](function.sodium-crypto-generichash-update.md)
-   [sodiumcryptogenerichash()](function.sodium-crypto-generichash.md)
-   [sodiumcryptokdfderivefromkey()](function.sodium-crypto-kdf-derive-from-key.md)
-   [sodiumcryptokdfkeygen()](function.sodium-crypto-kdf-keygen.md)
-   [sodiumcryptoкксclientsessionkeys()](function.sodium-crypto-kx-client-session-keys.md)
-   [sodiumcryptoкксkeypair()](function.sodium-crypto-kx-keypair.md)
-   [sodiumcryptoкксpublickey()](function.sodium-crypto-kx-publickey.md)
-   [sodiumcryptoкксsecretkey()](function.sodium-crypto-kx-secretkey.md)
-   [sodiumcryptoкксseedkeypair()](function.sodium-crypto-kx-seed-keypair.md)
-   [sodiumcryptoкксserversessionkeys()](function.sodium-crypto-kx-server-session-keys.md)
-   [sodiumcryptopwhashscryptsalsa208sha256strverify()](function.sodium-crypto-pwhash-scryptsalsa208sha256-str-verify.md)
-   [sodiumcryptopwhashscryptsalsa208sha256str()](function.sodium-crypto-pwhash-scryptsalsa208sha256-str.md)
-   [sodiumcryptopwhashscryptsalsa208sha256()](function.sodium-crypto-pwhash-scryptsalsa208sha256.md)
-   [sodiumcryptopwhashstrverify()](function.sodium-crypto-pwhash-str-verify.md)
-   [sodiumcryptopwhashstr()](function.sodium-crypto-pwhash-str.md)
-   [sodiumcryptopwhash()](function.sodium-crypto-pwhash.md)
-   [sodiumcryptoscalarmultbase()](function.sodium-crypto-scalarmult-base.md)
-   [sodiumcryptoscalarmult()](function.sodium-crypto-scalarmult.md)
-   [sodiumcryptosecretboxkeygen()](function.sodium-crypto-secretbox-keygen.md)
-   [sodiumcryptosecretboxopen()](function.sodium-crypto-secretbox-open.md)
-   [sodiumcryptosecretbox()](function.sodium-crypto-secretbox.md)
-   [sodiumcryptoshorthashkeygen()](function.sodium-crypto-shorthash-keygen.md)
-   [sodiumcryptoshorthash()](function.sodium-crypto-shorthash.md)
-   [sodiumcryptosigndetached()](function.sodium-crypto-sign-detached.md)
-   [sodiumcryptosigned25519пктоcurve25519()](function.sodium-crypto-sign-ed25519-pk-to-curve25519.md)
-   [sodiumcryptosigned25519сктоcurve25519()](function.sodium-crypto-sign-ed25519-sk-to-curve25519.md)
-   [sodiumcryptosignkeypairfromsecretkeyandpublickey()](function.sodium-crypto-sign-keypair-from-secretkey-and-publickey.md)
-   [sodiumcryptosignkeypair()](function.sodium-crypto-sign-keypair.md)
-   [sodiumcryptosignopen()](function.sodium-crypto-sign-open.md)
-   [sodiumcryptosignpublickeyfromsecretkey()](function.sodium-crypto-sign-publickey-from-secretkey.md)
-   [sodiumcryptosignpublickey()](function.sodium-crypto-sign-publickey.md)
-   [sodiumcryptosignsecretkey()](function.sodium-crypto-sign-secretkey.md)
-   [sodiumcryptosignseedkeypair()](function.sodium-crypto-sign-seed-keypair.md)
-   [sodiumcryptosignverifydetached()](function.sodium-crypto-sign-verify-detached.md)
-   [sodiumcryptosign()](function.sodium-crypto-sign.md)
-   [sodiumcryptostreamkeygen()](function.sodium-crypto-stream-keygen.md)
-   [sodiumcryptostreamxor()](function.sodium-crypto-stream-xor.md)
-   [sodiumcryptostream()](function.sodium-crypto-stream.md)
-   [sodiumhex2bin()](function.sodium-hex2bin.md)
-   [sodiumincrement()](function.sodium-increment.md)
-   [sodiummemcmp()](function.sodium-memcmp.md)
-   [sodiummemzero()](function.sodium-memzero.md)
-   [sodiumpad()](function.sodium-pad.md)
-   [sodiumunpad()](function.sodium-unpad.md)

### [ZIP](book.zip.md)

-   [ZipArchive::count()](ziparchive.count.md)
-   [ZipArchive::setEncryptionName()](ziparchive.setencryptionname.md)
-   [ZipArchive::SetEncryptionIndex()](ziparchive.setencryptionindex.md)
