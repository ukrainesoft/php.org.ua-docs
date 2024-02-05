---
navigation:
  - function.oci-cancel.md: « oci\_cancel
  - function.oci-close.md: oci\_close »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_client\_version
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_client\_version

(PHP 5 >= 5.3.7, PHP 7, PHP 8, PECL OCI8 >= 1.4.6)

oci\_client\_version — Повертає версію клієнтської бібліотеки

### Опис

```methodsynopsis
oci_client_version(): string
```

Повертає номер версії у вигляді рядка клієнтської C-бібліотеки Oracle, з якою пов'язаний PHP.

### Список параметрів

Немає.

### Значення, що повертаються

Повертає номер версії у вигляді рядка (string).

### Приклади

**Приклад #1 Приклад використання** oci\_client\_version()\*\*\*\*

```php
<?php
    echo "Версия клиента: " . oci_client_version(); // Версия клиента: 19.9.0.0.0
?>
```

### Примітки

> **Зауваження** :
> 
> Бібліотеки Oracle версій до 10*g*R2 немає необхідного функціоналу, щоб видати номер версії. У цьому випадку функція поверне рядок " Unknown " .

### Дивіться також

-   [oci\_server\_version()](function.oci-server-version.md) \- Повертає версію сервера Oracle
