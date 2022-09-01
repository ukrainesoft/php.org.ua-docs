---
navigation:
  - sessionhandlerinterface.read.md: '« SessionHandlerInterface::read'
  - class.sessionidinterface.md: SessionIdInterface »
  - index.md: PHP Manual
  - class.sessionhandlerinterface.md: SessionHandlerInterface
title: 'SessionHandlerInterface::write'
---
# SessionHandlerInterface::write

(PHP 5> = 5.4.0, PHP 7, PHP 8)

SessionHandlerInterface::write — Записати дані сесії

### Опис

```methodsynopsis
public SessionHandlerInterface::write(string $id, string $data): bool
```

Записує дані сесії у сховище сесій. Викликається функцією [sessionwriteclose()](function.session-write-close.html), коли невдало завершується функція [sessionregistershutdown()](function.session-register-shutdown.html) або під час нормального завершення роботи. Увага: [SessionHandlerInterface::close()](sessionhandlerinterface.close.md) викликається відразу після цієї функції.

PHP викликає цей метод, коли сесія готова для збереження та закриття. Кодуються дані сесії із суперглобального масиву [SESSION](reserved.variables.session.md) серіалізований рядок і передаються разом з ідентифікатором сесії даним методом для зберігання. Метод серіалізації, що використовується, вказаний в опції [session.serializehandler](session.configuration.html#ini.session.serialize-handler)

Зауважте, що цей метод зазвичай викликається PHP після закриття буферів виводу, якщо явно не викликається [sessionwriteclose()](function.session-write-close.html)

### Список параметрів

`id`

Ідентифікатор сесії

`data`

Закодовані дані сесії. Ці дані є результатом внутрішнього кодування PHP суперглобального масиву. [SESSION](reserved.variables.session.md) в серіалізований рядок та передачі її як цей параметр. Зауважте, що сесії використовують альтернативний метод серіалізації.

### Значення, що повертаються

Значення сесійного сховища, що повертається (зазвичай **`true`** у разі успішного виконання, **`false`** у разі виникнення помилки). Це значення повертається назад до PHP для внутрішньої обробки.

### Дивіться також

-   Директива конфігурації [session.serializehandler](session.configuration.html#ini.session.serialize-handler)
