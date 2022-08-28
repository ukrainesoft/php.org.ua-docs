Перевіряє підписаний відкритий ключ та виклик

-   [« openssl\_spki\_new](function.openssl-spki-new.html)
    
-   [openssl\_verify »](function.openssl-verify.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Перевіряє підписаний відкритий ключ та виклик
    

# opensslspkiverify

(PHP 5> = 5.6.0, PHP 7, PHP 8)

opensslspkiverify — Перевіряє підписаний відкритий ключ та виклик

### Опис

```methodsynopsis
openssl_spki_verify(string $spki): bool
```

Перевіряє підписаний відкритий ключ та виклик

### Список параметрів

`spki`

Коректний підписаний відкритий ключ та виклик

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо параметр `spki` передано некоректні дані.

### Приклади

**Приклад #1 Приклад використання **opensslspkiverify()****

Перевірка наявного підписаного відкритого ключа з викликом

```php
<?php
$pkey = openssl_pkey_new('secret password');
$spkac = openssl_spki_new($pkey, 'challenge string');

if (openssl_spki_verify(preg_replace('/SPKAC=/', '', $spkac))) {
    echo $spkac;
} else {
    echo "Проверка SPKAC не удалась";
}
?>
```

**Приклад #2 Приклад використання **opensslspkiverify()** з** 

Перевірка наявного підписаного відкритого ключа та виклику, отриманого з елемента 

```php
<?php
if (openssl_spki_verify(preg_replace('/SPKAC=/', '', $_POST['spkac']))) {
    echo $spkac;
} else {
    echo "Проверка SPKAC не удалась";
}
?>
<keygen name="spkac" challenge="challenge string" keytype="RSA">
```

### Дивіться також

-   [openssl\_spki\_new()](function.openssl-spki-new.html) - Створення нового підписаного відкритого ключа із викликом
-   [openssl\_spki\_export\_challenge()](function.openssl-spki-export-challenge.html) - Експорт виклику, пов'язаного з підписаним ключем та викликом
-   [openssl\_spki\_export()](function.openssl-spki-export.html) - Експорт відкритого ключа у форматі PEM із підписаного відкритого ключа з викликом
-   [openssl\_get\_md\_methods()](function.openssl-get-md-methods.html) - Отримати список доступних методів хешування
-   [openssl\_csr\_new()](function.openssl-csr-new.html) - Генерує CSR
-   [openssl\_csr\_sign()](function.openssl-csr-sign.html) - Підписати CSR за допомогою іншого сертифіката (або ним же) та створити сертифікат