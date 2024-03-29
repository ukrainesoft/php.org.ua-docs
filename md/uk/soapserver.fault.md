---
navigation:
  - soapserver.construct.md: '« SoapServer::\_\_construct'
  - soapserver.getfunctions.md: 'SoapServer::getFunctions »'
  - index.md: PHP Manual
  - class.soapserver.md: SoapServer
title: 'SoapServer::fault'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SoapServer::fault

(PHP 5, PHP 7, PHP 8)

SoapServer::fault — Вимушує SoapServer повернути помилку

### Опис

```methodsynopsis
public SoapServer::fault(    string $code,    string $string,    string $actor = "",    mixed $details = null,    string $name = ""): void
```

Надсилає клієнту відповідь на поточний запит із повідомленням про помилку.

> **Зауваження** :
> 
> Може бути викликана лише під час обробки запиту.

### Список параметрів

`code`

Код помилки, що повертається

`string`

Короткий опис помилки

`actor`

Рядок, що ідентифікує відправника, що спричинив помилку

`details`

Детальна інформація про помилку

`name`

Ім'я помилки. Може використовуватись для вибору імені із WSDL-файлу.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [SoapFault::\_\_construct()](soapfault.construct.md) \- Конструктор SoapFault
