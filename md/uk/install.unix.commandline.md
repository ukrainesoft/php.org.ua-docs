---
navigation:
  - install.unix.litespeed.md: Веб-сервер LiteSpeed/OpenLiteSpeed ​​на системах Unix
  - install.unix.openbsd.md: 'OpenBSD, замечания по установке »'
  - index.md: PHP Manual
  - install.unix.md: Встановлення на Unix-системи
title: Установка з інтерфейсами CGI та командного рядка
---
## Установка з інтерфейсами CGI та командного рядка

За замовчуванням, PHP збирається одночасно як CLI та CGI програма, яка може бути використана для обробки CGI-запитів. PHP як модуль сервера виграє у продуктивності, проте PHP CGI дозволяє запускати PHP від ​​користувача, відмінного від того, під яким виконується сервер.

**Увага**

Використовуючи інсталяцію CGI, ваш сервер відкритий перед кількома можливими вразливістю. Будь ласка, ознайомтесь із розділом ["Безпека CGI"](security.cgi-bin.md) щоб дізнатися, як можна захистити себе від таких атак.

### Тестування

Якщо ви зібрали PHP як CGI, ви можете протестувати ваше складання командою **make test**. Тестування вашої збірки – завжди гарна ідея. Таким чином ви зможете раніше виявити проблеми PHP на вашій платформі замість того, щоб боротися з ними пізніше.

### Використання змінних

Деякі [змінні оточення сервера](reserved.variables.server.md) не визначено у поточній [» специфікації CGI/1.1](http://www.faqs.org/rfcs/rfc3875). Визначено лише такі змінні: AUTHTYPE, CONTENTLENGTH, CONTENTTYPE, GATEWAYINTERFACE, PATHINFO, PATHTRANSLATED, QUERYSTRING, REMOTEADDR, REMOTEHOST, REMOTEIDENT, REMOTEUSER, REQUESTMETHOD, SCRIPTNAME, SERVERNAME, SERVERPORT, SERVERPROTOCOL та SERVERSOFTWARE. Решта має оброблятися як додаткові модулі (vendor extensions).
