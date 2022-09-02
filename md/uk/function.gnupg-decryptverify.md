---
navigation:
  - function.gnupg-decrypt.md: « gnupgdecrypt
  - function.gnupg-deletekey.md: gnupgdeletekey »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupgdecryptverify
---
# gnupgdecryptverify

(PECL gnupg >= 0.2)

gnupgdecrypt verify — Розшифровує та перевіряє підпис переданого тексту

### Опис

```methodsynopsis
gnupg_decryptverify(resource $identifier, string $text, string &$plaintext): array
```

Розшифровує та перевіряє підпис переданого тексту та повертає інформацію про підпис.

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupginit()](function.gnupg-init.md) або **gnupg**

`text`

Текст для розшифрування.

`plaintext`

Параметру `plaintext` передається розшифрований текст.

### Значення, що повертаються

У разі успішного виконання функція повертає інформацію про підпис та передає до параметра `plaintext` розшифрований текст. У разі помилки функція повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **gnupgdecryptverify()** у процедурному стилі**

```php
<?php
$plaintext = "";
$res = gnupg_init();
gnupg_adddecryptkey($res, "8660281B6051D071D94B5B230549F9DC851566DC", "test");
$info = gnupg_decryptverify($res, $text, $plaintext);
print_r($info);
?>
```

**Приклад #2 Приклад використання **gnupgdecryptverify()** в об'єктно-орієнтованому стилі**

```php
<?php
$plaintext = "";
$gpg = new gnupg();
$gpg->adddecryptkey("8660281B6051D071D94B5B230549F9DC851566DC","test");
$info = $gpg->decryptverify($text,$plaintext);
print_r($info);
?>
```
