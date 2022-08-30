Нові функції

-   [" Нові можливості](migration72.new-features.html)
    
-   [Новые глобальные константы »](migration72.constants.html)
    
-   [PHP Manual](index.html)
    
-   [Миграция с PHP 7.1.x на PHP 7.2.x](migration72.html)
    
-   Нові функції
    

## Нові функції

### Ядро PHP

-   [streamisatty()](function.stream-isatty.html)
-   [sapiwindowsvt100support()](function.sapi-windows-vt100-support.html)

### [SPL](book.spl.html)

-   [splobjectid()](function.spl-object-id.html)

### [DOM](book.dom.html)

-   [DomNodeList::count()](domnodelist.count.html)
-   [DOMNamedNodeMap::count()](domnamednodemap.count.html)

### [FTP](book.ftp.html)

-   [ftpappend()](function.ftp-append.html)

### [ДД](book.image.html)

-   [imagesetclip()](function.imagesetclip.html)
-   [imagegetclip()](function.imagegetclip.html)
-   [imageopenpolygon()](function.imageopenpolygon.html)
-   [imageresolution()](function.imageresolution.html)
-   [imagecreatefrombmp()](function.imagecreatefrombmp.html)
-   [imagebmp()](function.imagebmp.html)

### [Hash](book.hash.html)

-   [hashhmacalgos()](function.hash-hmac-algos.html)

### [LDAP](book.ldap.html)

-   [ldapparseexop()](function.ldap-parse-exop.html)
-   [ldapexop()](function.ldap-exop.html)
-   [ldapexoppasswd()](function.ldap-exop-passwd.html)
-   [ldapexopwhoami()](function.ldap-exop-whoami.html)

### [Многобайтные строки](book.mbstring.html)

-   [мбchr()](function.mb-chr.html)
-   [мбord()](function.mb-ord.html)
-   [мбscrub()](function.mb-scrub.html)

### [Oracle OCI8](book.oci8.html)

-   [ociregistertafcallback()](function.oci-register-taf-callback.html)
-   [ociunregistertafcallback()](function.oci-unregister-taf-callback.html)

### [Сокеты](book.sockets.html)

-   [socketaddrinfolookup()](function.socket-addrinfo-lookup.html)
-   [socketaddrinfoconnect()](function.socket-addrinfo-connect.html)
-   [socketaddrinfobind()](function.socket-addrinfo-bind.html)
-   [socketaddrinfoexplain()](function.socket-addrinfo-explain.html)

### [Sodium](book.sodium.html)

-   [sodiumadd()](function.sodium-add.html)
-   [sodiumbin2hex()](function.sodium-bin2hex.html)
-   [sodiumcompare()](function.sodium-compare.html)
-   [sodiumcryptoaeadaes256gcmdecrypt()](function.sodium-crypto-aead-aes256gcm-decrypt.html)
-   [sodiumcryptoaeadaes256gcmencrypt()](function.sodium-crypto-aead-aes256gcm-encrypt.html)
-   [sodiumcryptoaeadaes256gcmісavailable()](function.sodium-crypto-aead-aes256gcm-is-available.html)
-   [sodiumcryptoaeadaes256gcmkeygen()](function.sodium-crypto-aead-aes256gcm-keygen.html)
-   [sodiumcryptoaeadchacha20poly1305decrypt()](function.sodium-crypto-aead-chacha20poly1305-decrypt.html)
-   [sodiumcryptoaeadchacha20poly1305encrypt()](function.sodium-crypto-aead-chacha20poly1305-encrypt.html)
-   [sodiumcryptoaeadchacha20poly1305ietfdecrypt()](function.sodium-crypto-aead-chacha20poly1305-ietf-decrypt.html)
-   [sodiumcryptoaeadchacha20poly1305ietfencrypt()](function.sodium-crypto-aead-chacha20poly1305-ietf-encrypt.html)
-   [sodiumcryptoaeadchacha20poly1305ietfkeygen()](function.sodium-crypto-aead-chacha20poly1305-ietf-keygen.html)
-   [sodiumcryptoaeadchacha20poly1305keygen()](function.sodium-crypto-aead-chacha20poly1305-keygen.html)
-   [sodiumcryptoauthkeygen()](function.sodium-crypto-auth-keygen.html)
-   [sodiumcryptoauthverify()](function.sodium-crypto-auth-verify.html)
-   [sodiumcryptoauth()](function.sodium-crypto-auth.html)
-   [sodiumcryptoboxkeypairfromsecretkeyandpublickey()](function.sodium-crypto-box-keypair-from-secretkey-and-publickey.html)
-   [sodiumcryptoboxkeypair()](function.sodium-crypto-box-keypair.html)
-   [sodiumcryptoboxopen()](function.sodium-crypto-box-open.html)
-   [sodiumcryptoboxpublickeyfromsecretkey()](function.sodium-crypto-box-publickey-from-secretkey.html)
-   [sodiumcryptoboxpublickey()](function.sodium-crypto-box-publickey.html)
-   [sodiumcryptoboxsealopen()](function.sodium-crypto-box-seal-open.html)
-   [sodiumcryptoboxseal()](function.sodium-crypto-box-seal.html)
-   [sodiumcryptoboxsecretkey()](function.sodium-crypto-box-secretkey.html)
-   [sodiumcryptoboxseedkeypair()](function.sodium-crypto-box-seed-keypair.html)
-   [sodiumcryptobox()](function.sodium-crypto-box.html)
-   [sodiumcryptogenerichashfinal()](function.sodium-crypto-generichash-final.html)
-   [sodiumcryptogenerichashinit()](function.sodium-crypto-generichash-init.html)
-   [sodiumcryptogenerichashkeygen()](function.sodium-crypto-generichash-keygen.html)
-   [sodiumcryptogenerichashupdate()](function.sodium-crypto-generichash-update.html)
-   [sodiumcryptogenerichash()](function.sodium-crypto-generichash.html)
-   [sodiumcryptokdfderivefromkey()](function.sodium-crypto-kdf-derive-from-key.html)
-   [sodiumcryptokdfkeygen()](function.sodium-crypto-kdf-keygen.html)
-   [sodiumcryptoкксclientsessionkeys()](function.sodium-crypto-kx-client-session-keys.html)
-   [sodiumcryptoкксkeypair()](function.sodium-crypto-kx-keypair.html)
-   [sodiumcryptoкксpublickey()](function.sodium-crypto-kx-publickey.html)
-   [sodiumcryptoкксsecretkey()](function.sodium-crypto-kx-secretkey.html)
-   [sodiumcryptoкксseedkeypair()](function.sodium-crypto-kx-seed-keypair.html)
-   [sodiumcryptoкксserversessionkeys()](function.sodium-crypto-kx-server-session-keys.html)
-   [sodiumcryptopwhashscryptsalsa208sha256strverify()](function.sodium-crypto-pwhash-scryptsalsa208sha256-str-verify.html)
-   [sodiumcryptopwhashscryptsalsa208sha256str()](function.sodium-crypto-pwhash-scryptsalsa208sha256-str.html)
-   [sodiumcryptopwhashscryptsalsa208sha256()](function.sodium-crypto-pwhash-scryptsalsa208sha256.html)
-   [sodiumcryptopwhashstrverify()](function.sodium-crypto-pwhash-str-verify.html)
-   [sodiumcryptopwhashstr()](function.sodium-crypto-pwhash-str.html)
-   [sodiumcryptopwhash()](function.sodium-crypto-pwhash.html)
-   [sodiumcryptoscalarmultbase()](function.sodium-crypto-scalarmult-base.html)
-   [sodiumcryptoscalarmult()](function.sodium-crypto-scalarmult.html)
-   [sodiumcryptosecretboxkeygen()](function.sodium-crypto-secretbox-keygen.html)
-   [sodiumcryptosecretboxopen()](function.sodium-crypto-secretbox-open.html)
-   [sodiumcryptosecretbox()](function.sodium-crypto-secretbox.html)
-   [sodiumcryptoshorthashkeygen()](function.sodium-crypto-shorthash-keygen.html)
-   [sodiumcryptoshorthash()](function.sodium-crypto-shorthash.html)
-   [sodiumcryptosigndetached()](function.sodium-crypto-sign-detached.html)
-   [sodiumcryptosigned25519пктоcurve25519()](function.sodium-crypto-sign-ed25519-pk-to-curve25519.html)
-   [sodiumcryptosigned25519сктоcurve25519()](function.sodium-crypto-sign-ed25519-sk-to-curve25519.html)
-   [sodiumcryptosignkeypairfromsecretkeyandpublickey()](function.sodium-crypto-sign-keypair-from-secretkey-and-publickey.html)
-   [sodiumcryptosignkeypair()](function.sodium-crypto-sign-keypair.html)
-   [sodiumcryptosignopen()](function.sodium-crypto-sign-open.html)
-   [sodiumcryptosignpublickeyfromsecretkey()](function.sodium-crypto-sign-publickey-from-secretkey.html)
-   [sodiumcryptosignpublickey()](function.sodium-crypto-sign-publickey.html)
-   [sodiumcryptosignsecretkey()](function.sodium-crypto-sign-secretkey.html)
-   [sodiumcryptosignseedkeypair()](function.sodium-crypto-sign-seed-keypair.html)
-   [sodiumcryptosignverifydetached()](function.sodium-crypto-sign-verify-detached.html)
-   [sodiumcryptosign()](function.sodium-crypto-sign.html)
-   [sodiumcryptostreamkeygen()](function.sodium-crypto-stream-keygen.html)
-   [sodiumcryptostreamxor()](function.sodium-crypto-stream-xor.html)
-   [sodiumcryptostream()](function.sodium-crypto-stream.html)
-   [sodiumhex2bin()](function.sodium-hex2bin.html)
-   [sodiumincrement()](function.sodium-increment.html)
-   [sodiummemcmp()](function.sodium-memcmp.html)
-   [sodiummemzero()](function.sodium-memzero.html)
-   [sodiumpad()](function.sodium-pad.html)
-   [sodiumunpad()](function.sodium-unpad.html)

### [ZIP](book.zip.html)

-   [ZipArchive::count()](ziparchive.count.html)
-   [ZipArchive::setEncryptionName()](ziparchive.setencryptionname.html)
-   [ZipArchive::SetEncryptionIndex()](ziparchive.setencryptionindex.html)