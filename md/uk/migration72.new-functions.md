---
navigation:
  - migration72.new-features.md: '" Нові можливості'
  - migration72.constants.md: Нові глобальні константи »
  - index.md: PHP Manual
  - migration72.md: Міграція з PHP 7.1.x на PHP 7.2.x
title: Нові функції
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Нові функції

### Ядро PHP

-   [stream\_isatty()](function.stream-isatty.md)
-   [sapi\_windows\_vt100\_support()](function.sapi-windows-vt100-support.md)

### [SPL](book.spl.md)

-   [spl\_object\_id()](function.spl-object-id.md)

### [DOM](book.dom.md)

-   [DomNodeList::count()](domnodelist.count.md)
-   [DOMNamedNodeMap::count()](domnamednodemap.count.md)

### [FTP](book.ftp.md)

-   [ftp\_append()](function.ftp-append.md)

### [GD](book.image.md)

-   [imagesetclip()](function.imagesetclip.md)
-   [imagegetclip()](function.imagegetclip.md)
-   [imageopenpolygon()](function.imageopenpolygon.md)
-   [imageresolution()](function.imageresolution.md)
-   [imagecreatefrombmp()](function.imagecreatefrombmp.md)
-   [imagebmp()](function.imagebmp.md)

### [Hash](book.hash.md)

-   [hash\_hmac\_algos()](function.hash-hmac-algos.md)

### [LDAP](book.ldap.md)

-   [ldap\_parse\_exop()](function.ldap-parse-exop.md)
-   [ldap\_exop()](function.ldap-exop.md)
-   [ldap\_exop\_passwd()](function.ldap-exop-passwd.md)
-   [ldap\_exop\_whoami()](function.ldap-exop-whoami.md)

### [Багатобайтні рядки](book.mbstring.md)

-   [mb\_chr()](function.mb-chr.md)
-   [mb\_ord()](function.mb-ord.md)
-   [mb\_scrub()](function.mb-scrub.md)

### [Oracle OCI8](book.oci8.md)

-   [oci\_register\_taf\_callback()](function.oci-register-taf-callback.md)
-   [oci\_unregister\_taf\_callback()](function.oci-unregister-taf-callback.md)

### [Сокети](book.sockets.md)

-   [socket\_addrinfo\_lookup()](function.socket-addrinfo-lookup.md)
-   [socket\_addrinfo\_connect()](function.socket-addrinfo-connect.md)
-   [socket\_addrinfo\_bind()](function.socket-addrinfo-bind.md)
-   [socket\_addrinfo\_explain()](function.socket-addrinfo-explain.md)

### [Sodium](book.sodium.md)

-   [sodium\_add()](function.sodium-add.md)
-   [sodium\_bin2hex()](function.sodium-bin2hex.md)
-   [sodium\_compare()](function.sodium-compare.md)
-   [sodium\_crypto\_aead\_aes256gcm\_decrypt()](function.sodium-crypto-aead-aes256gcm-decrypt.md)
-   [sodium\_crypto\_aead\_aes256gcm\_encrypt()](function.sodium-crypto-aead-aes256gcm-encrypt.md)
-   [sodium\_crypto\_aead\_aes256gcm\_is\_available()](function.sodium-crypto-aead-aes256gcm-is-available.md)
-   [sodium\_crypto\_aead\_aes256gcm\_keygen()](function.sodium-crypto-aead-aes256gcm-keygen.md)
-   [sodium\_crypto\_aead\_chacha20poly1305\_decrypt()](function.sodium-crypto-aead-chacha20poly1305-decrypt.md)
-   [sodium\_crypto\_aead\_chacha20poly1305\_encrypt()](function.sodium-crypto-aead-chacha20poly1305-encrypt.md)
-   [sodium\_crypto\_aead\_chacha20poly1305\_ietf\_decrypt()](function.sodium-crypto-aead-chacha20poly1305-ietf-decrypt.md)
-   [sodium\_crypto\_aead\_chacha20poly1305\_ietf\_encrypt()](function.sodium-crypto-aead-chacha20poly1305-ietf-encrypt.md)
-   [sodium\_crypto\_aead\_chacha20poly1305\_ietf\_keygen()](function.sodium-crypto-aead-chacha20poly1305-ietf-keygen.md)
-   [sodium\_crypto\_aead\_chacha20poly1305\_keygen()](function.sodium-crypto-aead-chacha20poly1305-keygen.md)
-   [sodium\_crypto\_auth\_keygen()](function.sodium-crypto-auth-keygen.md)
-   [sodium\_crypto\_auth\_verify()](function.sodium-crypto-auth-verify.md)
-   [sodium\_crypto\_auth()](function.sodium-crypto-auth.md)
-   [sodium\_crypto\_box\_keypair\_from\_secretkey\_and\_publickey()](function.sodium-crypto-box-keypair-from-secretkey-and-publickey.md)
-   [sodium\_crypto\_box\_keypair()](function.sodium-crypto-box-keypair.md)
-   [sodium\_crypto\_box\_open()](function.sodium-crypto-box-open.md)
-   [sodium\_crypto\_box\_publickey\_from\_secretkey()](function.sodium-crypto-box-publickey-from-secretkey.md)
-   [sodium\_crypto\_box\_publickey()](function.sodium-crypto-box-publickey.md)
-   [sodium\_crypto\_box\_seal\_open()](function.sodium-crypto-box-seal-open.md)
-   [sodium\_crypto\_box\_seal()](function.sodium-crypto-box-seal.md)
-   [sodium\_crypto\_box\_secretkey()](function.sodium-crypto-box-secretkey.md)
-   [sodium\_crypto\_box\_seed\_keypair()](function.sodium-crypto-box-seed-keypair.md)
-   [sodium\_crypto\_box()](function.sodium-crypto-box.md)
-   [sodium\_crypto\_generichash\_final()](function.sodium-crypto-generichash-final.md)
-   [sodium\_crypto\_generichash\_init()](function.sodium-crypto-generichash-init.md)
-   [sodium\_crypto\_generichash\_keygen()](function.sodium-crypto-generichash-keygen.md)
-   [sodium\_crypto\_generichash\_update()](function.sodium-crypto-generichash-update.md)
-   [sodium\_crypto\_generichash()](function.sodium-crypto-generichash.md)
-   [sodium\_crypto\_kdf\_derive\_from\_key()](function.sodium-crypto-kdf-derive-from-key.md)
-   [sodium\_crypto\_kdf\_keygen()](function.sodium-crypto-kdf-keygen.md)
-   [sodium\_crypto\_kx\_client\_session\_keys()](function.sodium-crypto-kx-client-session-keys.md)
-   [sodium\_crypto\_kx\_keypair()](function.sodium-crypto-kx-keypair.md)
-   [sodium\_crypto\_kx\_publickey()](function.sodium-crypto-kx-publickey.md)
-   [sodium\_crypto\_kx\_secretkey()](function.sodium-crypto-kx-secretkey.md)
-   [sodium\_crypto\_kx\_seed\_keypair()](function.sodium-crypto-kx-seed-keypair.md)
-   [sodium\_crypto\_kx\_server\_session\_keys()](function.sodium-crypto-kx-server-session-keys.md)
-   [sodium\_crypto\_pwhash\_scryptsalsa208sha256\_str\_verify()](function.sodium-crypto-pwhash-scryptsalsa208sha256-str-verify.md)
-   [sodium\_crypto\_pwhash\_scryptsalsa208sha256\_str()](function.sodium-crypto-pwhash-scryptsalsa208sha256-str.md)
-   [sodium\_crypto\_pwhash\_scryptsalsa208sha256()](function.sodium-crypto-pwhash-scryptsalsa208sha256.md)
-   [sodium\_crypto\_pwhash\_str\_verify()](function.sodium-crypto-pwhash-str-verify.md)
-   [sodium\_crypto\_pwhash\_str()](function.sodium-crypto-pwhash-str.md)
-   [sodium\_crypto\_pwhash()](function.sodium-crypto-pwhash.md)
-   [sodium\_crypto\_scalarmult\_base()](function.sodium-crypto-scalarmult-base.md)
-   [sodium\_crypto\_scalarmult()](function.sodium-crypto-scalarmult.md)
-   [sodium\_crypto\_secretbox\_keygen()](function.sodium-crypto-secretbox-keygen.md)
-   [sodium\_crypto\_secretbox\_open()](function.sodium-crypto-secretbox-open.md)
-   [sodium\_crypto\_secretbox()](function.sodium-crypto-secretbox.md)
-   [sodium\_crypto\_shorthash\_keygen()](function.sodium-crypto-shorthash-keygen.md)
-   [sodium\_crypto\_shorthash()](function.sodium-crypto-shorthash.md)
-   [sodium\_crypto\_sign\_detached()](function.sodium-crypto-sign-detached.md)
-   [sodium\_crypto\_sign\_ed25519\_pk\_to\_curve25519()](function.sodium-crypto-sign-ed25519-pk-to-curve25519.md)
-   [sodium\_crypto\_sign\_ed25519\_sk\_to\_curve25519()](function.sodium-crypto-sign-ed25519-sk-to-curve25519.md)
-   [sodium\_crypto\_sign\_keypair\_from\_secretkey\_and\_publickey()](function.sodium-crypto-sign-keypair-from-secretkey-and-publickey.md)
-   [sodium\_crypto\_sign\_keypair()](function.sodium-crypto-sign-keypair.md)
-   [sodium\_crypto\_sign\_open()](function.sodium-crypto-sign-open.md)
-   [sodium\_crypto\_sign\_publickey\_from\_secretkey()](function.sodium-crypto-sign-publickey-from-secretkey.md)
-   [sodium\_crypto\_sign\_publickey()](function.sodium-crypto-sign-publickey.md)
-   [sodium\_crypto\_sign\_secretkey()](function.sodium-crypto-sign-secretkey.md)
-   [sodium\_crypto\_sign\_seed\_keypair()](function.sodium-crypto-sign-seed-keypair.md)
-   [sodium\_crypto\_sign\_verify\_detached()](function.sodium-crypto-sign-verify-detached.md)
-   [sodium\_crypto\_sign()](function.sodium-crypto-sign.md)
-   [sodium\_crypto\_stream\_keygen()](function.sodium-crypto-stream-keygen.md)
-   [sodium\_crypto\_stream\_xor()](function.sodium-crypto-stream-xor.md)
-   [sodium\_crypto\_stream()](function.sodium-crypto-stream.md)
-   [sodium\_hex2bin()](function.sodium-hex2bin.md)
-   [sodium\_increment()](function.sodium-increment.md)
-   [sodium\_memcmp()](function.sodium-memcmp.md)
-   [sodium\_memzero()](function.sodium-memzero.md)
-   [sodium\_pad()](function.sodium-pad.md)
-   [sodium\_unpad()](function.sodium-unpad.md)

### [ZIP](book.zip.md)

-   [ZipArchive::count()](ziparchive.count.md)
-   [ZipArchive::setEncryptionName()](ziparchive.setencryptionname.md)
-   [ZipArchive::SetEncryptionIndex()](ziparchive.setencryptionindex.md)
