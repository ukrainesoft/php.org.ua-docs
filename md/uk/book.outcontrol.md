Управління буфером виводу

-   [« opcache\_reset](function.opcache-reset.html)
    
-   [Введение »](intro.outcontrol.html)
    
-   [PHP Manual](index.html)
    
-   [Изменение поведения PHP](refs.basic.php.html)
    
-   Управління буфером виводу
    

# Управління буфером виводу

-   [Введение](intro.outcontrol.html)
-   [Установка и настройка](outcontrol.setup.html)
    -   [Требования](outcontrol.requirements.html)
    -   [Установка](outcontrol.installation.html)
    -   [Настройка во время выполнения](outcontrol.configuration.html)
    -   [Типы ресурсов](outcontrol.resources.html)
-   [Предопределённые константы](outcontrol.constants.html)
-   [Примеры](outcontrol.examples.html)
    -   [Базовое использование](outcontrol.examples.basic.html)
    -   [Использование перезаписи вывода](outcontrol.examples.rewrite.html)
-   [Функции контроля вывода](ref.outcontrol.html)
    -   [flush](function.flush.html) - Скидання системного буфера виводу
    -   [ob\_clean](function.ob-clean.html) - Очистити (стерти) буфер виводу
    -   [ob\_end\_clean](function.ob-end-clean.html) — Очистити (стерти) буфер виводу та вимкнути буферизацію виводу
    -   [ob\_end\_flush](function.ob-end-flush.html) — Скинути (відправити) буфер виведення та вимкнути буферизацію виводу
    -   [ob\_flush](function.ob-flush.html) — Скинути (надіслати) буфер виводу
    -   [ob\_get\_clean](function.ob-get-clean.html) — Отримати вміст поточного буфера та видалити його
    -   [ob\_get\_contents](function.ob-get-contents.html) — Повертає вміст буфера виводу
    -   [ob\_get\_flush](function.ob-get-flush.html) — Скинути буфер виводу, повернути його у вигляді рядка та вимкнути буферизацію виводу
    -   [ob\_get\_length](function.ob-get-length.html) — Повертає розмір буфера виводу
    -   [ob\_get\_level](function.ob-get-level.html) — Повертає рівень вкладеності механізму буферизації виводу
    -   [ob\_get\_status](function.ob-get-status.html) — Отримати статус буфера виводу
    -   [ob\_gzhandler](function.ob-gzhandler.html) - callback-функція, що використовується для gzip-стиснення буфера виводу при виклику obstart
    -   [ob\_implicit\_flush](function.ob-implicit-flush.html) — Увімкнення/вимкнення неявного скидання
    -   [ob\_list\_handlers](function.ob-list-handlers.html) - Список всіх використовуваних обробників виводу
    -   [ob\_start](function.ob-start.html) — Увімкнення буферизації виводу
    -   [output\_add\_rewrite\_var](function.output-add-rewrite-var.html) — Додати значення до обробника URL
    -   [output\_reset\_rewrite\_vars](function.output-reset-rewrite-vars.html) — Скинути значення обробника URL