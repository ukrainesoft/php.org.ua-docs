Експорт відкритого ключа у форматі PEM із підписаного відкритого ключа з викликом

-   [« opensslspkiexportchallenge](function.openssl-spki-export-challenge.html)
    
-   [opensslspkinew »](function.openssl-spki-new.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Експорт відкритого ключа у форматі PEM із підписаного відкритого ключа з викликом
    

# opensslspkiexport

(PHP 5> = 5.6.0, PHP 7, PHP 8)

opensslspkiexport — Експорт відкритого ключа у форматі PEM із підписаного відкритого ключа з викликом

### Опис

```methodsynopsis
openssl_spki_export(string $spki): string|false
```

Експортує відкритий ключ у форматі PEM із підписаного відкритого ключа з викликом

### Список параметрів

`spki`

Коректний відкритий ключ із викликом

### Значення, що повертаються

Повертає відкритий ключ у форматі PEM або **`false`** у разі виникнення помилки.

### Помилки

Викликає помилку рівня **`E_WARNING`** якщо параметр `spki` передано некоректні дані.

### Приклади

**Приклад #1 Приклад використання **opensslspkiexport()****

Повертає відкритий ключ у форматі PEM або **`null`** у разі виникнення помилки.

```php
<?php
$pkey = openssl_pkey_new('secret password');
$spkac = openssl_spki_new($pkey, 'challenge string');
$pubKey = openssl_spki_export(preg_replace('/SPKAC=/', '', $spkac));

if ($pubKey) {
    echo $pubKey;
}
?>
```

**Приклад #2 Приклад використання **opensslspkiexport()** з**

Повертає відкритий ключ у форматі PEM, отриманий із елемента

```php
<?php
$spkac = openssl_spki_export(preg_replace('/SPKAC=/', '', $_POST['spkac']));
if ($spkac != NULL) {
    echo $spkac;
} else {
    echo "Не удалось извлечь открытый ключ";
}
?>
<keygen name="spkac" challenge="challenge string" keytype="RSA">
```

### Дивіться також

-   [opensslspkinew()](function.openssl-spki-new.html) - Створення нового підписаного відкритого ключа із викликом
-   [opensslspkiverify()](function.openssl-spki-verify.html) - Перевіряє підписаний відкритий ключ та виклик
-   [opensslspkiexportchallenge()](function.openssl-spki-export-challenge.html) - Експорт виклику, пов'язаного з підписаним ключем та викликом
-   [opensslgetмдmethods()](function.openssl-get-md-methods.html) - Отримати список доступних методів хешування
-   [opensslcsrnew()](function.openssl-csr-new.html) - Генерує CSR
-   [opensslcsrsign()](function.openssl-csr-sign.html) - Підписати CSR за допомогою іншого сертифіката (або ним же) та створити сертифікат