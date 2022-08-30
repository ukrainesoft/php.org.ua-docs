Експорт виклику, пов'язаного з підписаним ключем та викликом

-   [« opensslsign](function.openssl-sign.html)
    
-   [opensslspkiexport »](function.openssl-spki-export.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Експорт виклику, пов'язаного з підписаним ключем та викликом
    

# opensslspkiexportchallenge

(PHP 5> = 5.6.0, PHP 7, PHP 8)

opensslspkiexportchallenge — Експорт виклику, пов'язаного з підписаним ключем та викликом

### Опис

```methodsynopsis
openssl_spki_export_challenge(string $spki): string|false
```

Експорт дзвінка з підписаного відкритого ключа та дзвінка.

### Список параметрів

`spki`

Коректний підписаний відкритий ключ із викликом

### Значення, що повертаються

Повертає рядок дзвінка або **`false`** у разі виникнення помилки.

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо параметр `spki` передано некоректні дані.

### Приклади

**Приклад #1 Приклад використання **opensslspkiexportchallenge()****

Повертає рядок дзвінка або **`null`** у разі виникнення помилки.

```php
<?php
$pkey = openssl_pkey_new('secret password');
$spkac = openssl_spki_new($pkey, 'challenge string');
$challenge = openssl_spki_export_challenge(preg_replace('/SPKAC=/', '', $spkac));
?>
```

**Приклад #2 Приклад використання **opensslspkiexportchallenge()** з**

Вилучення рядка виклику, отриманого з елемента

```php
<?php
$challenge = openssl_spki_export_challenge(preg_replace('/SPKAC=/', '', $_POST['spkac']));
?>
<keygen name="spkac" challenge="challenge string" keytype="RSA">
```

### Дивіться також

-   [opensslspkinew()](function.openssl-spki-new.html) - Створення нового підписаного відкритого ключа із викликом
-   [opensslspkiverify()](function.openssl-spki-verify.html) - Перевіряє підписаний відкритий ключ та виклик
-   [opensslspkiexport()](function.openssl-spki-export.html) - Експорт відкритого ключа у форматі PEM із підписаного відкритого ключа з викликом
-   [opensslgetмдmethods()](function.openssl-get-md-methods.html) - Отримати список доступних методів хешування
-   [opensslcsrnew()](function.openssl-csr-new.html) - Генерує CSR
-   [opensslcsrsign()](function.openssl-csr-sign.html) - Підписати CSR за допомогою іншого сертифіката (або ним же) та створити сертифікат