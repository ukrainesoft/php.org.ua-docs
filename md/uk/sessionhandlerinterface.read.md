---
navigation:
  - sessionhandlerinterface.open.md: '« SessionHandlerInterface::open'
  - sessionhandlerinterface.write.md: 'SessionHandlerInterface::write »'
  - index.md: PHP Manual
  - class.sessionhandlerinterface.md: SessionHandlerInterface
title: 'SessionHandlerInterface::read'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SessionHandlerInterface::read

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

SessionHandlerInterface::read — Читає дані сесії

### Опис

```methodsynopsis
public SessionHandlerInterface::read(string $id): string|false
```

Читає дані сесії зі сховища сесій та повертає результат. Викликається відразу після старту сесії або коли викликана [session\_start()](function.session-start.md). Зверніть увагу, що перед викликом цього методу буде викликано функцію [SessionHandlerInterface::open()](sessionhandlerinterface.open.md)

Цей метод викликається PHP, коли стартує сесія. Цей метод має отримати дані сесії зі сховища за вказаним її ідентифікатором. Рядок, що повертається цим методом, повинен мати той же серіалізований формат, що й вихідний, який передавався функції [SessionHandlerInterface::write()](sessionhandlerinterface.write.md). Якщо запис не знайдено, повертається **`false`**

Дані, що повертаються цим методом, будуть розшифровані всередині PHP, використовуючи метод десеріалізації, зазначений у [session.serialize\_handler](session.configuration.md#ini.session.serialize-handler). Отримані дані будуть використані для заповнення суперглобального масиву [$\_SESSION](reserved.variables.session.md)

Зверніть увагу, що схема серіалізації даних не така, як у функції [unserialize()](function.unserialize.md), і отримати доступ до даних можна за допомогою функції [session\_decode()](function.session-decode.md)

### Список параметрів

`id`

Ідентифікатор сесії

### Значення, що повертаються

Повертає закодований рядок прочитаних даних. Якщо нічого не прочитано, повертається **`false`**. Зауважте, що це значення передається для обробки всередині PHP.

### Дивіться також

-   INI-директива[session.serialize\_handler](session.configuration.md#ini.session.serialize-handler)
