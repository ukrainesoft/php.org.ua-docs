---
navigation:
  - outcontrol.operations-on-buffers.md: '« Операції, дозволені для буферів'
  - outcontrol.working-with-output-handlers.md: Робота з оброблювачами виводу »
  - index.md: PHP Manual
  - outcontrol.user-level-output-buffers.md: Буфери виводу користувача
title: Обробники виводу
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Обробники виводу

Обробники висновку - це [callable](language.types.callable.md)\-об'єкти, пов'язані з буферами виводу, які запускаються викликом функцій [ob\_clean()](function.ob-clean.md) [ob\_flush()](function.ob-flush.md) [ob\_end\_flush()](function.ob-end-flush.md) [ob\_get\_flush()](function.ob-get-flush.md) [ob\_end\_clean()](function.ob-end-clean.md) [ob\_get\_clean()](function.ob-get-clean.md) або протягом завершення роботи PHP.

> **Зауваження**: Процес завершення роботи скине значення обробника, що повертається.

Якщо при запуску буфера виводу обробник не заданий або значення дорівнює **`null`**, буде активовано внутрішній обробник виводу `«default output handler»`, який під час виклику повертає незмінений вміст буфера. Обробниками виводу користуються для повернення зміненої версії вмісту буфера та (або) або отримання побічних ефектів (наприклад, надсилання заголовків).

PHP поставляється з двома внутрішніми обробниками виводу: `«default output handler»`и`«URL-Rewriter»` (В який вбудований свій буфер виведення і до двох екземплярів якого дозволено запускати).

Модулі, що входять до комплекту, включають чотири додаткові обробники висновку: [mb\_output\_handler()](function.mb-output-handler.md) [ob\_gzhandler()](function.ob-gzhandler.md) [ob\_iconv\_handler()](function.ob-iconv-handler.md) [ob\_tidyhandler()](function.ob-tidyhandler.md)
