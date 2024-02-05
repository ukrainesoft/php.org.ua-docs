---
navigation:
  - function.opcache-reset.md: « opcache\_reset
  - intro.outcontrol.md: Вступ "
  - index.md: PHP Manual
  - refs.basic.php.md: Зміна поведінки PHP
title: Управління буфером виводу
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Управління буфером виводу

-   [Вступ](intro.outcontrol.md)
-   [Встановлення та налаштування](outcontrol.setup.md)
    -   [Вимоги](outcontrol.requirements.md)
    -   [Установка](outcontrol.installation.md)
    -   [Налаштування під час виконання](outcontrol.configuration.md)
    -   [Типи ресурсів](outcontrol.resources.md)
-   [Обумовлені константи](outcontrol.constants.md)
-   [Буферизація висновку](outcontrol.output-buffering.md)
-   [Скидання (відправлення) системних буферів](outcontrol.flushing-system-buffers.md)
-   [Буфери виводу користувача](outcontrol.user-level-output-buffers.md)
    -   [Який висновок буферизується?](outcontrol.what-output-is-buffered.md)
    -   [Вкладені буфери виводу](outcontrol.nesting-output-buffers.md)
    -   [Розмір буфера](outcontrol.buffer-size.md)
    -   [Операції, дозволені для буферів](outcontrol.operations-on-buffers.md)
    -   [Обробники виводу](outcontrol.output-handlers.md)
    -   [Робота з оброблювачами виводу](outcontrol.working-with-output-handlers.md)
    -   [Прапори, що передаються обробникам виводу](outcontrol.flags-passed-to-output-handlers.md)
    -   [Значення оброблювача виводу, що повертаються](outcontrol.output-handler-return-values.md)
-   [Приклади](outcontrol.examples.md)
    -   [Основи](outcontrol.examples.basic.md)
    -   [Перезапис виводу](outcontrol.examples.rewrite.md)
-   [Функції контролю виведення](ref.outcontrol.md)
    -   [flush](function.flush.md)— скидає системний буфер виводу
    -   [ob\_clean](function.ob-clean.md)— Очищає (прає) вміст активного буфера виводу
    -   [ob\_end\_clean](function.ob-end-clean.md)— Очищає (стирає) вміст активного буфера виводу та відключає його
    -   [ob\_end\_flush](function.ob-end-flush.md)— Скидає (відправляє) значення активного оброблювача виводу, що повертається, і відключає активний буфер виводу
    -   [ob\_flush](function.ob-flush.md)— Скидає (відправляє) повернене активним обробником висновку значення
    -   [ob\_get\_clean](function.ob-get-clean.md)— Отримує вміст активного буфера виводу та вимикає його
    -   [ob\_get\_contents](function.ob-get-contents.md)— Повертає вміст буфера виводу
    -   [ob\_get\_flush](function.ob-get-flush.md)— Скидає (відправляє) повернене активним обробником виводу значення, повертає вміст активного буфера виводу та відключає його
    -   [ob\_get\_length](function.ob-get-length.md)— Повертає розмір буфера виводу
    -   [ob\_get\_level](function.ob-get-level.md)— Повертає рівень вкладеності механізму буферизації виводу
    -   [ob\_get\_status](function.ob-get-status.md)— Отримує статус буфера виводу
    -   [ob\_implicit\_flush](function.ob-implicit-flush.md)— Вмикає/вимикає неявне скидання
    -   [ob\_list\_handlers](function.ob-list-handlers.md)— Повертає список активних обробників виводу
    -   [ob\_start](function.ob-start.md)— Включає буферизацію виводу
    -   [output\_add\_rewrite\_var](function.output-add-rewrite-var.md)— Додає значення до обробника перезапису URL
    -   [output\_reset\_rewrite\_vars](function.output-reset-rewrite-vars.md)— Скинути значення обробника URL
