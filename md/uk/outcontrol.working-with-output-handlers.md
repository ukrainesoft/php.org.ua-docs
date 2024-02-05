---
navigation:
  - outcontrol.output-handlers.md: « Обробники висновку
  - outcontrol.flags-passed-to-output-handlers.md: 'Прапори, що передаються обробникам виводу »'
  - index.md: PHP Manual
  - outcontrol.user-level-output-buffers.md: Буфери виводу користувача
title: Робота з оброблювачами виводу
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Робота з оброблювачами виводу

При викликі обробникам виведення передається вміст буфера та бітова маска, що вказує на стан буферизації виводу.

```methodsynopsis

     handler
    (
     string
      $buffer
    , 
     int
      $phase
     = ?): string
```

`buffer`

Вміст буфера виводу.

`phase`

Бітова маска [\*\*`PHP_OUTPUT_HANDLER_*`\*\*-констант](outcontrol.constants.md#constant.php-output-handler-start)

**Увага**

Виклик наступних функцій з обробника висновку призведе до фатальної помилки: [ob\_clean()](function.ob-clean.md) [ob\_end\_clean()](function.ob-end-clean.md) [ob\_end\_flush()](function.ob-end-flush.md) [ob\_flush()](function.ob-flush.md) [ob\_get\_clean()](function.ob-get-clean.md) [ob\_get\_flush()](function.ob-get-flush.md) [ob\_start()](function.ob-start.md)

> **Зауваження**: Если установлен флаг статуса\*\*`PHP_OUTPUT_HANDLER_DISABLED`\*\* оброблювача, оброблювач не буде запущений викликом функцій [ob\_end\_clean()](function.ob-end-clean.md) [ob\_end\_flush()](function.ob-end-flush.md) [ob\_get\_clean()](function.ob-get-clean.md) [ob\_get\_flush()](function.ob-get-flush.md) або протягом завершення роботи PHP. Цей прапор не дає ефекту під час виклику функцій [ob\_clean()](function.ob-clean.md) або [ob\_flush()](function.ob-flush.md)

> **Зауваження**: Функція завершення роботи на ряді веб-серверів вміє змінювати робочу директорію скрипта, наприклад, на сервері Apache або вбудованому веб-сервері.
