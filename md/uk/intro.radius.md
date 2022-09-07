---
navigation:
  - book.radius.md: « Radius
  - radius.setup.md: Встановлення та налаштування »
  - index.md: PHP Manual
  - book.radius.md: Radius
title: Вступ
---
# Вступ

Пакет базується на бібліотеці libradius (Remote Authentication Dial In User Service) з FreeBSD. Він дозволяє проводити облік та автентифікацію клієнтів шляхом запитів до віддалених мережевих сервісів.

Цей модуль PECL додає повну підтримку Radius Authentication ([» RFC 2865](http://www.faqs.org/rfcs/rfc2865)) та Radius Accounting ([» RFC 2866](http://www.faqs.org/rfcs/rfc2866)). Цей пакет доступний для Unix (тестувався у FreeBSD та Linux) та для Windows.

> **Зауваження**
> 
> Детальний опис бібліотеки libradius можна знайти [»тут](http://www.freebsd.org/cgi/man.cgi?query=libradius). Детальна інформація про файл конфігурації лежить [»тут](http://www.freebsd.org/cgi/man.cgi?query=radius.conf)
