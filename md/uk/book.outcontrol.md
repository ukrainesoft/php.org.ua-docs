Управління буфером виводу

-   [« opcachereset](function.opcache-reset.html)
    
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
-   [Функції контролю виведення](ref.outcontrol.html)
    -   [flush](function.flush.html) - Скидання системного буфера виводу
    -   [проclean](function.ob-clean.html) - Очистити (стерти) буфер виводу
    -   [проendclean](function.ob-end-clean.html) — Очистити (стерти) буфер виводу та вимкнути буферизацію виводу
    -   [проendflush](function.ob-end-flush.html) — Скинути (відправити) буфер виведення та вимкнути буферизацію виводу
    -   [проflush](function.ob-flush.html) — Скинути (надіслати) буфер виводу
    -   [проgetclean](function.ob-get-clean.html) — Отримати вміст поточного буфера та видалити його
    -   [проgetcontents](function.ob-get-contents.html) — Повертає вміст буфера виводу
    -   [проgetflush](function.ob-get-flush.html) — Скинути буфер виводу, повернути його у вигляді рядка та вимкнути буферизацію виводу
    -   [проgetlength](function.ob-get-length.html) — Повертає розмір буфера виводу
    -   [проgetlevel](function.ob-get-level.html) — Повертає рівень вкладеності механізму буферизації виводу
    -   [проgetstatus](function.ob-get-status.html) — Отримати статус буфера виводу
    -   [проgzhandler](function.ob-gzhandler.html) - callback-функція, що використовується для gzip-стиснення буфера виводу при виклику obstart
    -   [проimplicitflush](function.ob-implicit-flush.html) — Увімкнення/вимкнення неявного скидання
    -   [проlisthandlers](function.ob-list-handlers.html) - Список всіх використовуваних обробників виводу
    -   [проstart](function.ob-start.html) — Увімкнення буферизації виводу
    -   [outputaddrewritevar](function.output-add-rewrite-var.html) — Додати значення до обробника URL
    -   [outputresetrewritevars](function.output-reset-rewrite-vars.html) — Скинути значення обробника URL