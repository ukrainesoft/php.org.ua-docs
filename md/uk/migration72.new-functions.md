Нові функції

-   [« Новые возможности](migration72.new-features.html)
    
-   [Новые глобальные константы »](migration72.constants.html)
    
-   [PHP Manual](index.html)
    
-   [Миграция с PHP 7.1.x на PHP 7.2.x](migration72.html)
    
-   Нові функції
    

## Нові функції

### Ядро PHP

-   [stream\_isatty()](function.stream-isatty.html)
-   [sapi\_windows\_vt100\_support()](function.sapi-windows-vt100-support.html)

### [SPL](book.spl.html)

-   [spl\_object\_id()](function.spl-object-id.html)

### [DOM](book.dom.html)

-   [DomNodeList::count()](domnodelist.count.html)
-   [DOMNamedNodeMap::count()](domnamednodemap.count.html)

### [FTP](book.ftp.html)

-   [ftp\_append()](function.ftp-append.html)

### [GD](book.image.html)

-   [imagesetclip()](function.imagesetclip.html)
-   [imagegetclip()](function.imagegetclip.html)
-   [imageopenpolygon()](function.imageopenpolygon.html)
-   [imageresolution()](function.imageresolution.html)
-   [imagecreatefrombmp()](function.imagecreatefrombmp.html)
-   [imagebmp()](function.imagebmp.html)

### [Hash](book.hash.html)

-   [hash\_hmac\_algos()](function.hash-hmac-algos.html)

### [LDAP](book.ldap.html)

-   [ldap\_parse\_exop()](function.ldap-parse-exop.html)
-   [ldap\_exop()](function.ldap-exop.html)
-   [ldap\_exop\_passwd()](function.ldap-exop-passwd.html)
-   [ldap\_exop\_whoami()](function.ldap-exop-whoami.html)

### [Многобайтные строки](book.mbstring.html)

-   [mb\_chr()](function.mb-chr.html)
-   [mb\_ord()](function.mb-ord.html)
-   [mb\_scrub()](function.mb-scrub.html)

### [Oracle OCI8](book.oci8.html)

-   [oci\_register\_taf\_callback()](function.oci-register-taf-callback.html)
-   [oci\_unregister\_taf\_callback()](function.oci-unregister-taf-callback.html)

### [Сокеты](book.sockets.html)

-   [socket\_addrinfo\_lookup()](function.socket-addrinfo-lookup.html)
-   [socket\_addrinfo\_connect()](function.socket-addrinfo-connect.html)
-   [socket\_addrinfo\_bind()](function.socket-addrinfo-bind.html)
-   [socket\_addrinfo\_explain()](function.socket-addrinfo-explain.html)

### [Sodium](book.sodium.html)

-   [sodium\_add()](function.sodium-add.html)
-   [sodium\_bin2hex()](function.sodium-bin2hex.html)
-   [sodium\_compare()](function.sodium-compare.html)
-   [sodium\_crypto\_aead\_aes256gcm\_decrypt()](function.sodium-crypto-aead-aes256gcm-decrypt.html)
-   [sodium\_crypto\_aead\_aes256gcm\_encrypt()](function.sodium-crypto-aead-aes256gcm-encrypt.html)
-   [sodium\_crypto\_aead\_aes256gcm\_is\_available()](function.sodium-crypto-aead-aes256gcm-is-available.html)
-   [sodium\_crypto\_aead\_aes256gcm\_keygen()](function.sodium-crypto-aead-aes256gcm-keygen.html)
-   [sodium\_crypto\_aead\_chacha20poly1305\_decrypt()](function.sodium-crypto-aead-chacha20poly1305-decrypt.html)
-   [sodium\_crypto\_aead\_chacha20poly1305\_encrypt()](function.sodium-crypto-aead-chacha20poly1305-encrypt.html)
-   [sodium\_crypto\_aead\_chacha20poly1305\_ietf\_decrypt()](function.sodium-crypto-aead-chacha20poly1305-ietf-decrypt.html)
-   [sodium\_crypto\_aead\_chacha20poly1305\_ietf\_encrypt()](function.sodium-crypto-aead-chacha20poly1305-ietf-encrypt.html)
-   [sodium\_crypto\_aead\_chacha20poly1305\_ietf\_keygen()](function.sodium-crypto-aead-chacha20poly1305-ietf-keygen.html)
-   [sodium\_crypto\_aead\_chacha20poly1305\_keygen()](function.sodium-crypto-aead-chacha20poly1305-keygen.html)
-   [sodium\_crypto\_auth\_keygen()](function.sodium-crypto-auth-keygen.html)
-   [sodium\_crypto\_auth\_verify()](function.sodium-crypto-auth-verify.html)
-   [sodium\_crypto\_auth()](function.sodium-crypto-auth.html)
-   [sodium\_crypto\_box\_keypair\_from\_secretkey\_and\_publickey()](function.sodium-crypto-box-keypair-from-secretkey-and-publickey.html)
-   [sodium\_crypto\_box\_keypair()](function.sodium-crypto-box-keypair.html)
-   [sodium\_crypto\_box\_open()](function.sodium-crypto-box-open.html)
-   [sodium\_crypto\_box\_publickey\_from\_secretkey()](function.sodium-crypto-box-publickey-from-secretkey.html)
-   [sodium\_crypto\_box\_publickey()](function.sodium-crypto-box-publickey.html)
-   [sodium\_crypto\_box\_seal\_open()](function.sodium-crypto-box-seal-open.html)
-   [sodium\_crypto\_box\_seal()](function.sodium-crypto-box-seal.html)
-   [sodium\_crypto\_box\_secretkey()](function.sodium-crypto-box-secretkey.html)
-   [sodium\_crypto\_box\_seed\_keypair()](function.sodium-crypto-box-seed-keypair.html)
-   [sodium\_crypto\_box()](function.sodium-crypto-box.html)
-   [sodium\_crypto\_generichash\_final()](function.sodium-crypto-generichash-final.html)
-   [sodium\_crypto\_generichash\_init()](function.sodium-crypto-generichash-init.html)
-   [sodium\_crypto\_generichash\_keygen()](function.sodium-crypto-generichash-keygen.html)
-   [sodium\_crypto\_generichash\_update()](function.sodium-crypto-generichash-update.html)
-   [sodium\_crypto\_generichash()](function.sodium-crypto-generichash.html)
-   [sodium\_crypto\_kdf\_derive\_from\_key()](function.sodium-crypto-kdf-derive-from-key.html)
-   [sodium\_crypto\_kdf\_keygen()](function.sodium-crypto-kdf-keygen.html)
-   [sodium\_crypto\_kx\_client\_session\_keys()](function.sodium-crypto-kx-client-session-keys.html)
-   [sodium\_crypto\_kx\_keypair()](function.sodium-crypto-kx-keypair.html)
-   [sodium\_crypto\_kx\_publickey()](function.sodium-crypto-kx-publickey.html)
-   [sodium\_crypto\_kx\_secretkey()](function.sodium-crypto-kx-secretkey.html)
-   [sodium\_crypto\_kx\_seed\_keypair()](function.sodium-crypto-kx-seed-keypair.html)
-   [sodium\_crypto\_kx\_server\_session\_keys()](function.sodium-crypto-kx-server-session-keys.html)
-   [sodium\_crypto\_pwhash\_scryptsalsa208sha256\_str\_verify()](function.sodium-crypto-pwhash-scryptsalsa208sha256-str-verify.html)
-   [sodium\_crypto\_pwhash\_scryptsalsa208sha256\_str()](function.sodium-crypto-pwhash-scryptsalsa208sha256-str.html)
-   [sodium\_crypto\_pwhash\_scryptsalsa208sha256()](function.sodium-crypto-pwhash-scryptsalsa208sha256.html)
-   [sodium\_crypto\_pwhash\_str\_verify()](function.sodium-crypto-pwhash-str-verify.html)
-   [sodium\_crypto\_pwhash\_str()](function.sodium-crypto-pwhash-str.html)
-   [sodium\_crypto\_pwhash()](function.sodium-crypto-pwhash.html)
-   [sodium\_crypto\_scalarmult\_base()](function.sodium-crypto-scalarmult-base.html)
-   [sodium\_crypto\_scalarmult()](function.sodium-crypto-scalarmult.html)
-   [sodium\_crypto\_secretbox\_keygen()](function.sodium-crypto-secretbox-keygen.html)
-   [sodium\_crypto\_secretbox\_open()](function.sodium-crypto-secretbox-open.html)
-   [sodium\_crypto\_secretbox()](function.sodium-crypto-secretbox.html)
-   [sodium\_crypto\_shorthash\_keygen()](function.sodium-crypto-shorthash-keygen.html)
-   [sodium\_crypto\_shorthash()](function.sodium-crypto-shorthash.html)
-   [sodium\_crypto\_sign\_detached()](function.sodium-crypto-sign-detached.html)
-   [sodium\_crypto\_sign\_ed25519\_pk\_to\_curve25519()](function.sodium-crypto-sign-ed25519-pk-to-curve25519.html)
-   [sodium\_crypto\_sign\_ed25519\_sk\_to\_curve25519()](function.sodium-crypto-sign-ed25519-sk-to-curve25519.html)
-   [sodium\_crypto\_sign\_keypair\_from\_secretkey\_and\_publickey()](function.sodium-crypto-sign-keypair-from-secretkey-and-publickey.html)
-   [sodium\_crypto\_sign\_keypair()](function.sodium-crypto-sign-keypair.html)
-   [sodium\_crypto\_sign\_open()](function.sodium-crypto-sign-open.html)
-   [sodium\_crypto\_sign\_publickey\_from\_secretkey()](function.sodium-crypto-sign-publickey-from-secretkey.html)
-   [sodium\_crypto\_sign\_publickey()](function.sodium-crypto-sign-publickey.html)
-   [sodium\_crypto\_sign\_secretkey()](function.sodium-crypto-sign-secretkey.html)
-   [sodium\_crypto\_sign\_seed\_keypair()](function.sodium-crypto-sign-seed-keypair.html)
-   [sodium\_crypto\_sign\_verify\_detached()](function.sodium-crypto-sign-verify-detached.html)
-   [sodium\_crypto\_sign()](function.sodium-crypto-sign.html)
-   [sodium\_crypto\_stream\_keygen()](function.sodium-crypto-stream-keygen.html)
-   [sodium\_crypto\_stream\_xor()](function.sodium-crypto-stream-xor.html)
-   [sodium\_crypto\_stream()](function.sodium-crypto-stream.html)
-   [sodium\_hex2bin()](function.sodium-hex2bin.html)
-   [sodium\_increment()](function.sodium-increment.html)
-   [sodium\_memcmp()](function.sodium-memcmp.html)
-   [sodium\_memzero()](function.sodium-memzero.html)
-   [sodium\_pad()](function.sodium-pad.html)
-   [sodium\_unpad()](function.sodium-unpad.html)

### [ZIP](book.zip.html)

-   [ZipArchive::count()](ziparchive.count.html)
-   [ZipArchive::setEncryptionName()](ziparchive.setencryptionname.html)
-   [ZipArchive::SetEncryptionIndex()](ziparchive.setencryptionindex.html)