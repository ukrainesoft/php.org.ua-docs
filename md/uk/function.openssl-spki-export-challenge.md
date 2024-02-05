---
navigation:
  - function.openssl-sign.md: « openssl\_sign
  - function.openssl-spki-export.md: openssl\_spki\_export »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_spki\_export\_challenge
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_spki\_export\_challenge

(PHP 5 >= 5.6.0, PHP 7, PHP 8)

openssl\_spki\_export\_challenge — Експорт виклику, пов'язаного з підписаним ключем та викликом

### Опис

```methodsynopsis
openssl_spki_export_challenge(string $spki): string|false
```

Експорт дзвінка з підписаного відкритого ключа та дзвінка.

### Список параметрів

`spki`

Коректний підписаний відкритий ключ із викликом

### Значення, що повертаються

Повертає рядок дзвінка або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо параметр `spki` передано некоректні дані.

### Приклади

**Приклад #1 Приклад використання** openssl\_spki\_export\_challenge()\*\*\*\*

Повертає рядок дзвінка або \*\*`null`\*\*в случае возникновения ошибки.

```php
<?php
$pkey = openssl_pkey_new('secret password');
$spkac = openssl_spki_new($pkey, 'challenge string');
$challenge = openssl_spki_export_challenge(preg_replace('/SPKAC=/', '', $spkac));
?>
```

**Приклад #2 Приклад использование**openssl\_spki\_export\_challenge()**с**

Вилучення рядка виклику, отриманого з елемента

```php
<?php
$challenge = openssl_spki_export_challenge(preg_replace('/SPKAC=/', '', $_POST['spkac']));
?>
<keygen name="spkac" challenge="challenge string" keytype="RSA">
```

### Дивіться також

-   [openssl\_spki\_new()](function.openssl-spki-new.md) \- Створення нового підписаного відкритого ключа із викликом
-   [openssl\_spki\_verify()](function.openssl-spki-verify.md) \- Перевіряє підписаний відкритий ключ та виклик
-   [openssl\_spki\_export()](function.openssl-spki-export.md) \- Експорт відкритого ключа у форматі PEM із підписаного відкритого ключа з викликом
-   [openssl\_get\_md\_methods()](function.openssl-get-md-methods.md) \- Отримати список доступних методів хешування
-   [openssl\_csr\_new()](function.openssl-csr-new.md) \- Генерує CSR
-   [openssl\_csr\_sign()](function.openssl-csr-sign.md) \- Підписати CSR за допомогою іншого сертифіката (або ним же) та створити сертифікат
