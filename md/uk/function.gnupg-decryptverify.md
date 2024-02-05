---
navigation:
  - function.gnupg-decrypt.md: « gnupg\_decrypt
  - function.gnupg-deletekey.md: gnupg\_deletekey »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupg\_decryptverify
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gnupg\_decryptverify

(PECL gnupg >= 0.2)

gnupg\_decrypt verify — Розшифровує та перевіряє підпис переданого тексту

### Опис

```methodsynopsis
gnupg_decryptverify(resource $identifier, string $text, string &$plaintext): array|false
```

Розшифровує та перевіряє підпис переданого тексту та повертає інформацію про підпис.

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.md)или**gnupg**

`text`

Текст для розшифрування.

`plaintext`

Параметру`plaintext` передається розшифрований текст.

### Значення, що повертаються

У разі успішного виконання функція повертає інформацію про підпис та передає до параметра `plaintext` розшифрований текст. У разі помилки функція повертає **`false`**

### Приклади

**Пример #1 Пример использования**gnupg\_decryptverify()\*\* у процедурному стилі\*\*

```php
<?php
$plaintext = "";
$res = gnupg_init();
gnupg_adddecryptkey($res, "8660281B6051D071D94B5B230549F9DC851566DC", "test");
$info = gnupg_decryptverify($res, $text, $plaintext);
print_r($info);
?>
```

**Пример #2 Пример использования**gnupg\_decryptverify()\*\* в об'єктно-орієнтованому стилі\*\*

```php
<?php
$plaintext = "";
$gpg = new gnupg();
$gpg->adddecryptkey("8660281B6051D071D94B5B230549F9DC851566DC","test");
$info = $gpg->decryptverify($text,$plaintext);
print_r($info);
?>
```
