---
navigation:
  - function.ssh2-fetch-stream.md: « ssh2\_fetch\_stream
  - function.ssh2-forward-accept.md: ssh2\_forward\_accept »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_fingerprint
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_fingerprint

(PECL ssh2 >= 0.9.0)

ssh2\_fingerprint — отримання відбитка віддаленого сервера

### Опис

```methodsynopsis
ssh2_fingerprint(resource $session, int $flags = SSH2_FINGERPRINT_MD5 | SSH2_FINGERPRINT_HEX): string
```

Повертає хеш ключа хоста із активної сесії.

### Список параметрів

`session`

Ідентифікатор з'єднання SSH, отриманий з [ssh2\_connect()](function.ssh2-connect.md)

`flags`

`flags` може бути **`SSH2_FINGERPRINT_MD5`** або **`SSH2_FINGERPRINT_SHA1`**, об'єднані логічним АБО (OR) з **`SSH2_FINGERPRINT_HEX`** або **`SSH2_FINGERPRINT_RAW`**

### Значення, що повертаються

Повертає хеш ключа хоста у вигляді рядка.

### Приклади

**Приклад #1 Перевірка відбитка з відомим значенням**

```php
<?php
$known_host = '6F89C2F0A719B30CC38ABDF90755F2E4';

$connection = ssh2_connect('shell.example.com', 22);

$fingerprint = ssh2_fingerprint($connection,
               SSH2_FINGERPRINT_MD5 | SSH2_FINGERPRINT_HEX);

if ($fingerprint != $known_host) {
  die("Ключ хоста не совпадает!\n" .
      "Возможно, атака посредника?");
}
?>
```
