---
navigation:
  - function.openssl-spki-new.html: « opensslspkinew
  - function.openssl-verify.html: opensslverify »
  - index.md: PHP Manual
  - ref.openssl.md: Функции OpenSSL
title: opensslspkiverify
---
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

-   [opensslspkinew()](function.openssl-spki-new.md) - Створення нового підписаного відкритого ключа із викликом
-   [opensslspkiexportchallenge()](function.openssl-spki-export-challenge.md) - Експорт виклику, пов'язаного з підписаним ключем та викликом
-   [opensslspkiexport()](function.openssl-spki-export.md) - Експорт відкритого ключа у форматі PEM із підписаного відкритого ключа з викликом
-   [opensslgetмдmethods()](function.openssl-get-md-methods.md) - Отримати список доступних методів хешування
-   [opensslcsrnew()](function.openssl-csr-new.md) - Генерує CSR
-   [opensslcsrsign()](function.openssl-csr-sign.md) - Підписати CSR за допомогою іншого сертифіката (або ним же) та створити сертифікат
