---
navigation:
  - outcontrol.buffer-size.md: « Розмір буфера
  - outcontrol.output-handlers.md: Обробники виводу »
  - index.md: PHP Manual
  - outcontrol.user-level-output-buffers.md: Буфери виводу користувача
title: 'Операції, дозволені для буферів'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Операції, дозволені для буферів

Операціями, дозволеними для буферів, керують, передаючи [прапори керування буфером](outcontrol.constants.md#outcontrol.constants.buffer-control-flags)в третий параметр —`flags` - функції [ob\_start()](function.ob-start.md). Якщо параметр не встановлено, за промовчанням будуть дозволені всі операції. Якщо замість цього встановлено значення , буфер не можна буде скинути, очистити або видалити, але його вміст, як і раніше, буде доступний.

Флаг\*\*`PHP_OUTPUT_HANDLER_CLEANABLE`\*\* дозволяє функції [ob\_clean()](function.ob-clean.md) очищати вміст буфера.

**Увага**

Відсутність прапора **`PHP_OUTPUT_HANDLER_CLEANABLE`** не завадить функціям [ob\_end\_clean()](function.ob-end-clean.md) або [ob\_get\_clean()](function.ob-get-clean.md) очистити вміст буфера.

Флаг\*\*`PHP_OUTPUT_HANDLER_FLUSHABLE`\*\* дозволяє функції [ob\_flush()](function.ob-flush.md) скидати вміст буфера.

**Увага**

Відсутність прапора **`PHP_OUTPUT_HANDLER_FLUSHABLE`** не завадить функціям [ob\_end\_flush()](function.ob-end-flush.md) або [ob\_get\_flush()](function.ob-get-flush.md) скинути вміст буфера.

Флаг\*\*`PHP_OUTPUT_HANDLER_REMOVABLE`\*\* дозволяє функціям [ob\_end\_clean()](function.ob-end-clean.md) [ob\_end\_flush()](function.ob-end-flush.md) [ob\_get\_clean()](function.ob-get-clean.md) або [ob\_get\_flush()](function.ob-get-flush.md) відключати буфер.

Флаг\*\*`PHP_OUTPUT_HANDLER_STDFLAGS`\*\* - це комбінація трьох прапорів, які дозволяють кожну з трьох операцій бути виконаною з буфером.
