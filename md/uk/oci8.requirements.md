---
navigation:
  - oci8.setup.md: '" Встановлення та налаштування'
  - oci8.installation.md: Встановлення »
  - index.md: PHP Manual
  - oci8.setup.md: Встановлення та налаштування
title: Вимоги
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Вимоги

Модуль OCI8 3.0 включений до PHP 8. Також він доступний у [» PECL](https://pecl.php.net/)Для PHP 7, используйте OCI8 2.2 from[» PECL](https://pecl.php.net/). Для роботи OCI8 потрібні клієнтські бібліотеки Oracle 10*g* або вище.

Якщо база даних Oracle знаходиться на тій же машині, що і PHP, всі необхідні бібліотеки і заголовкові файли вже встановлені. Якщо PHP встановлений на іншу машину, використовуйте безкоштовні бібліотеки з [» Oracle Instant Client](https://www.oracle.com/database/technologies/instant-client.md)

Для использования Oracle Instant Client, установите`Basic`или`Basic Lite` zip-архів Oracle Instant Client або RPM або DMG пакет. При складанні PHP з вихідного коду також встановіть Instant Client `SDK`

Необхідно використовувати PHP з тими ж або свіжими версіями бібліотек Oracle, ніж ті, з якими було зібрано модуль OCI8.

> **Зауваження** :
> 
> Принципи клієнт-серверної мережевої сумісності Oracle, дозволяють створювати з'єднання між версіями Oracle Client і Oracle Database, що розрізняються. Подробиці див. у документі сумісності ID 207303.1. Коротко, Oracle Client 19, 18 і 12.2 можуть з'єднуватися з Oracle Database 11.2 і вище. Oracle Client 12.1 може з'єднуватися з Oracle Database 10.2 та вище. Oracle Client 11.2 може з'єднуватися з Oracle Database 9.2 та вище.

> **Зауваження** :
> 
> Повний набір можливостей OCI8 можливий лише за допомогою новітніх версій клієнтських бібліотек Oracle та бази даних.
