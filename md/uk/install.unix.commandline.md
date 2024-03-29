---
navigation:
  - install.unix.litespeed.md: Веб-сервер LiteSpeed/OpenLiteSpeed ​​на системах Unix
  - install.unix.openbsd.md: 'OpenBSD, зауваження щодо встановлення »'
  - index.md: PHP Manual
  - install.unix.md: Встановлення на Unix-системи
title: Установка з інтерфейсами CGI та командного рядка
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Установка з інтерфейсами CGI та командного рядка

За замовчуванням, PHP збирається одночасно як CLI та CGI програма, яка може бути використана для обробки CGI-запитів. PHP як модуль сервера виграє у продуктивності, проте PHP CGI дозволяє запускати PHP від ​​користувача, відмінного від того, під яким виконується сервер.

**Увага**

Використовуючи інсталяцію CGI, сервер відкритий перед кількома можливими вразливістю. Будь ласка, ознайомтесь із розділом «[Безпека CGI](security.cgi-bin.md)» щоб дізнатися, як можна захистити себе від таких атак.

### Тестування

Якщо ви зібрали PHP як CGI, ви можете протестувати ваше складання командою **make test**. Тестування вашої збірки – завжди гарна ідея. Таким чином ви зможете раніше виявити проблеми PHP на вашій платформі замість того, щоб боротися з ними пізніше.

### Використання змінних

Деякі [змінні оточення сервера](reserved.variables.server.md) не визначено у поточній [» специфікації CGI/1.1](http://www.faqs.org/rfcs/rfc3875). Визначено лише такі змінні: AUTH\_TYPE, CONTENT\_LENGTH, CONTENT\_TYPE, GATEWAY\_INTERFACE, PATH\_INFO, PATH\_TRANSLATED, QUERY\_STRING, REMOTE\_ADDR, REMOTE\_HOST, REMOTE\_IDENT, REMOTE\_USER, REQUEST\_METHOD, SCRIPT\_NAME, SERVER\_NAME, SERVER\_PORT, SERVER\_PROTOCOL та SERVER\_SOFTWARE. Решта має оброблятися як додаткові модулі (vendor extensions).
