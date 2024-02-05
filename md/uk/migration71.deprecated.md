---
navigation:
  - migration71.incompatible.md: '« Зміни, що ламають зворотну сумісність'
  - migration71.changed-functions.md: Змінені функції »
  - index.md: PHP Manual
  - migration71.md: Міграція з PHP 7.0.x на PHP 7.1.x
title: 'Функціонал, оголошений застарілим у PHP 7.1.x'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Функціонал, оголошений застарілим у PHP 7.1.x

### ext/mcrypt

Модуль mcrypt не розвивався вже майже десять років, а також був дуже складним у використанні. Він був оголошений застарілим на користь OpenSSL. Він буде видалений з ядра PHP і переміщений до PECL PHP 7.2.

### Модифікатор "e" для функцій [mb\_ereg\_replace()](function.mb-ereg-replace.md) і [mb\_eregi\_replace()](function.mb-eregi-replace.md)

Модификатор шаблона`e` був оголошений застарілим для функцій [mb\_ereg\_replace()](function.mb-ereg-replace.md) і [mb\_eregi\_replace()](function.mb-eregi-replace.md)
