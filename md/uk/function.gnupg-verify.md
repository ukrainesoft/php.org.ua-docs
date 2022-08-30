Перевіряє підпис тексту

-   [« gnupgsign](function.gnupg-sign.html)
    
-   [wkhtmltox »](book.wkhtmltox.html)
    
-   [PHP Manual](index.html)
    
-   [GnuPG Функції](ref.gnupg.html)
    
-   Перевіряє підпис тексту
    

# gnupgverify

(PECL gnupg >= 0.1)

gnupgverify — Перевірка підпису тексту

### Опис

```methodsynopsis
gnupg_verify(    resource $identifier,    string $signed_text,    string $signature,    string &$plaintext = ?): array
```

Перевіряє підпис переданого у параметрі `signed_text` тексту та повертає інформацію про підпис.

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupginit()](function.gnupg-init.html) або **gnupg**

`signed_text`

Підписаний текст.

`signature`

Підпис. Щоб перевірити прозорий підпис, параметр повинен дорівнювати **`false`**

`plaintext`

Звичайний текст. Якщо цей необов'язковий параметр необхідно передати, він заповнюється звичайним текстом.

### Значення, що повертаються

У разі успішного виконання, функція повертає інформацію про підпис. У разі помилки функція повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **gnupgverify()** у процедурному стилі**

```php
<?php
$plaintext = "";
$res = gnupg_init();
// прозрачная подпись
$info = gnupg_verify($res, $signed_text, false, $plaintext);
print_r($info);
// раздельная подпись
$info = gnupg_verify($res, $signed_text, $signature);
print_r($info);
?>
```

**Приклад #2 Приклад використання **gnupgverify()** в об'єктно-орієнтованому стилі**

```php
<?php
$plaintext = "";
$gpg = new gnupg();
// прозрачная подпись
$info = $gpg->verify($signed_text, false, $plaintext);
print_r($info);
// раздельная подпись
$info = $gpg->verify($signed_text, $signature);
print_r($info);
?>
```