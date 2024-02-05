---
navigation:
  - mongodb-driver-serverapi.bsonserialize.md: '« MongoDB\\Driver\\ServerApi::bsonSerialize'
  - mongodb-driver-serverapi.serialize.md: 'MongoDB\\Driver\\ServerApi::serialize »'
  - index.md: PHP Manual
  - class.mongodb-driver-serverapi.md: MongoDB\\Driver\\ServerApi
title: 'MongoDB\\Driver\\ServerApi::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ServerApi::\_\_construct

(mongodb >=1.10.0)

MongoDB\\Driver\\ServerApi::\_\_construct — Створює новий екземпляр ServerApi

### Опис

```methodsynopsis
final public MongoDB\Driver\ServerApi::__construct(string $version, ?bool $strict = null, ?bool $deprecationErrors = null)
```

Створює новий екземпляр [MongoDB\\Driver\\ServerApi](class.mongodb-driver-serverapi.md) екземпляр, який використовується для оголошення версії API під час створення [MongoDB\\Driver\\Manager](class.mongodb-driver-manager.md)

### Список параметрів

`version`

Версія сервера API.

Підтримувані версії API представлені у вигляді констант [MongoDB\\Driver\\ServerApi](class.mongodb-driver-serverapi.md). Єдиною підтримуваною версією API є **`MongoDB\Driver\ServerApi::V1`**

`strict`

Если у параметра`strict`установлено значение\*\*`true`**, сервер буде видавати помилку для будь-якої команди, яка не є частиною вказаної версії API. Якщо значення не вказано, використовується значення за замовчуванням (**`false`\*\*

`deprecationErrors`

Если у параметра`deprecationErrors`установлено значение\*\*`true`**, сервер буде видавати помилку під час використання команди, яка застаріла у вказаній версії API. Якщо значення не встановлено, використовується значення за замовчуванням (**`false`\*\*
