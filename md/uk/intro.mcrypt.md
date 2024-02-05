---
navigation:
  - book.mcrypt.md: « Mcrypt
  - mcrypt.setup.md: Встановлення та налаштування "
  - index.md: PHP Manual
  - book.mcrypt.md: Mcrypt
title: Вступ
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Вступ

**Увага**

Ця функціональність оголошена *застарілої* в PHP 7.1.0 та *ВИДАЛЕНО* у PHP 7.2.0.

Є такі альтернативи:

-   [Sodium](book.sodium.md)(доступний з PHP 7.2.0)
-   [OpenSSL](book.openssl.md)

> **Зауваження** :
> 
> Цей модуль був переміщений до репозиторію [» PECL](https://pecl.php.net/) і більше не постачається з PHP 7.2.0.

Це інтерфейс до бібліотеки mcrypt, яка підтримує широкий спектр блокових алгоритмів, таких як DES, TripleDES, Blowfish (за замовчуванням), 3-WAY, SAFER-SK64, SAFER-SK128, TWOFISH, TEA, RC2 та GOST з режимами шифрування CBC, OFB , CFB та ECB. Додатково підтримуються RC6 та IDEA, які є "не вільними". CFB/OFB за замовчуванням 8-біт.
