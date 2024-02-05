---
navigation:
  - soapclient.gettypes.md: '« SoapClient::\_\_getTypes'
  - soapclient.setlocation.md: 'SoapClient::\_\_setLocation »'
  - index.md: PHP Manual
  - class.soapclient.md: SoapClient
title: 'SoapClient::\_\_setCookie'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SoapClient::\_\_setCookie

(PHP 5 >= 5.0.4, PHP 7, PHP 8)

SoapClient::\_\_setCookie — Встановлює cookie для запитів SOAP

### Опис

```methodsynopsis
public SoapClient::__setCookie(string $name, ?string $value = null): void
```

Визначає cookie, які будуть надіслані із SOAP-запитами.

> **Зауваження** :
> 
> Виклик цього методу вплине на всі наступні виклики методів [SoapClient](class.soapclient.md)

### Список параметрів

`name`

Ім'я cookie.

`value`

Значення cookie. Якщо не вказано, cookie буде видалено.

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `value` тепер допускає значення null. |
