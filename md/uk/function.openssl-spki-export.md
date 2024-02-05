---
navigation:
  - function.openssl-spki-export-challenge.md: « openssl\_spki\_export\_challenge
  - function.openssl-spki-new.md: openssl\_spki\_new »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_spki\_export
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_spki\_export

(PHP 5 >= 5.6.0, PHP 7, PHP 8)

openssl\_spki\_export — Експорт відкритого ключа у форматі PEM із підписаного відкритого ключа з викликом

### Опис

```methodsynopsis
openssl_spki_export(string $spki): string|false
```

Експортує відкритий ключ у форматі PEM із підписаного відкритого ключа з викликом

### Список параметрів

`spki`

Коректний відкритий ключ із викликом.

### Значення, що повертаються

Повертає відкритий ключ у форматі PEM або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Викликає помилку рівня **`E_WARNING`** якщо параметр `spki` передано некоректні дані.

### Приклади

**Пример #1 Пример использования**openssl\_spki\_export()\*\*\*\*

Повертає відкритий ключ у форматі PEM або \*\*`null`\*\*в случае возникновения ошибки.

```php
<?php
$pkey = openssl_pkey_new('secret password');
$spkac = openssl_spki_new($pkey, 'challenge string');
$pubKey = openssl_spki_export(preg_replace('/SPKAC=/', '', $spkac));

if ($pubKey) {
    echo $pubKey;
}
?>
```

**Пример #2 Пример использования**openssl\_spki\_export()**с**

Повертає відкритий ключ у форматі PEM, отриманий із елемента

```php
<?php
$spkac = openssl_spki_export(preg_replace('/SPKAC=/', '', $_POST['spkac']));
if ($spkac != NULL) {
    echo $spkac;
} else {
    echo "Не удалось извлечь открытый ключ";
}
?>
<keygen name="spkac" challenge="challenge string" keytype="RSA">
```

### Дивіться також

-   [openssl\_spki\_new()](function.openssl-spki-new.md) \- Створення нового підписаного відкритого ключа із викликом
-   [openssl\_spki\_verify()](function.openssl-spki-verify.md) \- Перевіряє підписаний відкритий ключ та виклик
-   [openssl\_spki\_export\_challenge()](function.openssl-spki-export-challenge.md) \- Експорт виклику, пов'язаного з підписаним ключем та викликом
-   [openssl\_get\_md\_methods()](function.openssl-get-md-methods.md) \- Отримати список доступних методів хешування
-   [openssl\_csr\_new()](function.openssl-csr-new.md) \- Генерує CSR
-   [openssl\_csr\_sign()](function.openssl-csr-sign.md) \- Підписати CSR за допомогою іншого сертифіката (або ним же) та створити сертифікат
