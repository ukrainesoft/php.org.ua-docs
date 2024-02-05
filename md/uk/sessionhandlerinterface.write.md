---
navigation:
  - sessionhandlerinterface.read.md: '« SessionHandlerInterface::read'
  - class.sessionidinterface.md: SessionIdInterface »
  - index.md: PHP Manual
  - class.sessionhandlerinterface.md: SessionHandlerInterface
title: 'SessionHandlerInterface::write'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SessionHandlerInterface::write

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

SessionHandlerInterface::write — Записати дані сесії

### Опис

```methodsynopsis
public SessionHandlerInterface::write(string $id, string $data): bool
```

Записує дані сесії у сховище сесій. Викликається функцією [session\_write\_close()](function.session-write-close.md), коли невдало завершується функція [session\_register\_shutdown()](function.session-register-shutdown.md) або під час нормального завершення роботи. Увага: [SessionHandlerInterface::close()](sessionhandlerinterface.close.md) викликається відразу після цієї функції.

PHP викликає цей метод, коли сесія готова для збереження та закриття. Кодуються дані сесії із суперглобального масиву [$\_SESSION](reserved.variables.session.md) серіалізований рядок і передаються разом з ідентифікатором сесії даним методом для зберігання. Метод серіалізації, що використовується, вказаний в опції [session.serialize\_handler](session.configuration.md#ini.session.serialize-handler)

Зауважте, що цей метод зазвичай викликається PHP після закриття буферів виводу, якщо явно не викликається [session\_write\_close()](function.session-write-close.md)

### Список параметрів

`id`

Ідентифікатор сесії

`data`

Закодовані дані сесії. Ці дані є результатом внутрішнього кодування PHP суперглобального масиву. [$\_SESSION](reserved.variables.session.md) в серіалізований рядок та передачі її як цей параметр. Зауважте, що сесії використовують альтернативний метод серіалізації.

### Значення, що повертаються

Значення сесійного сховища, що повертається (зазвичай **`true`** у разі успішного виконання, **`false`** у разі виникнення помилки). Це значення повертається назад до PHP для внутрішньої обробки.

### Дивіться також

-   Директива конфігурації[session.serialize\_handler](session.configuration.md#ini.session.serialize-handler)
