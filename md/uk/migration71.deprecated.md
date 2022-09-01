---
navigation:
  - migration71.incompatible.html: '« Зміни, що ламають зворотну сумісність'
  - migration71.changed-functions.html: Змінені функції »
  - index.html: PHP Manual
  - migration71.html: Миграция с PHP 7.0.x на PHP 7.1.x
title: 'Функціонал, оголошений застарілим у PHP 7.1.x'
---
## Функціонал, оголошений застарілим у PHP 7.1.x

### ext/mcrypt

Модуль mcrypt не розвивався вже майже десять років, а також був украй складним у використанні. Він був оголошений застарілим на користь OpenSSL. Він буде видалений з ядра PHP і переміщений до PECL PHP 7.2.

### Модифікатор "e" для функцій [мбeregreplace()](function.mb-ereg-replace.html) і [мбeregireplace()](function.mb-eregi-replace.html)

Модифікатор шаблону `e` був оголошений застарілим для функцій [мбeregreplace()](function.mb-ereg-replace.html) і [мбeregireplace()](function.mb-eregi-replace.html)
