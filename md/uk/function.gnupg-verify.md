---
navigation:
  - function.gnupg-sign.md: « gnupg\_sign
  - book.wkhtmltox.md: wkhtmltox »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupg\_verify
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gnupg\_verify

(PECL gnupg >= 0.1)

gnupg\_verify — Перевірка підпису тексту

### Опис

```methodsynopsis
gnupg_verify(    resource $identifier,    string $signed_text,    string $signature,    string &$plaintext = ?): array|false
```

Перевіряє підпис переданого у параметрі `signed_text` тексту та повертає інформацію про підпис.

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.md)или**gnupg**

`signed_text`

Підписаний текст.

`signature`

Підпис. Щоб перевірити прозорий підпис, параметр повинен дорівнювати **`false`**

`plaintext`

Звичайний текст. Якщо цей необов'язковий параметр необхідно передати, він заповнюється звичайним текстом.

### Значення, що повертаються

У разі успішного виконання, функція повертає інформацію про підпис. У разі помилки функція повертає **`false`**

### Приклади

**Пример #1 Пример использования**gnupg\_verify()\*\* у процедурному стилі\*\*

```php
<?php
$plaintext = "";
$res = gnupg_init();
// прозрачная подпись
$info = gnupg_verify($res, $signed_text, false, $plaintext);
print_r($info);
// раздельная подпись
$info = gnupg_verify($res, $signed_text, $signature);
print_r($info);
?>
```

**Пример #2 Пример использования**gnupg\_verify()\*\* в об'єктно-орієнтованому стилі\*\*

```php
<?php
$plaintext = "";
$gpg = new gnupg();
// прозрачная подпись
$info = $gpg->verify($signed_text, false, $plaintext);
print_r($info);
// раздельная подпись
$info = $gpg->verify($signed_text, $signature);
print_r($info);
?>
```
