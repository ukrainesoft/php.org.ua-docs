---
navigation:
  - function.opcache-reset.html: « opcachereset
  - intro.outcontrol.html: Введение »
  - index.html: PHP Manual
  - refs.basic.php.html: Изменение поведения PHP
title: Управління буфером виводу
---
# Управління буфером виводу

-   [Введение](intro.outcontrol.md)
-   [Встановлення та налаштування](outcontrol.setup.md)
    -   [Вимоги](outcontrol.requirements.md)
    -   [Установка](outcontrol.installation.md)
    -   [Налаштування під час виконання](outcontrol.configuration.md)
    -   [Типи ресурсів](outcontrol.resources.md)
-   [Обумовлені константи](outcontrol.constants.md)
-   [Приклади](outcontrol.examples.md)
    -   [Базовое использование](outcontrol.examples.basic.md)
    -   [Використання перезапису виводу](outcontrol.examples.rewrite.md)
-   [Функції контролю виведення](ref.outcontrol.md)
    -   [flush](function.flush.md) - Скидання системного буфера виводу
    -   [проclean](function.ob-clean.md) - Очистити (стерти) буфер виводу
    -   [проendclean](function.ob-end-clean.md) — Очистити (стерти) буфер виводу та вимкнути буферизацію виводу
    -   [проendflush](function.ob-end-flush.md) — Скинути (відправити) буфер виведення та вимкнути буферизацію виводу
    -   [проflush](function.ob-flush.md) — Скинути (надіслати) буфер виводу
    -   [проgetclean](function.ob-get-clean.md) — Отримати вміст поточного буфера та видалити його
    -   [проgetcontents](function.ob-get-contents.md) — Повертає вміст буфера виводу
    -   [проgetflush](function.ob-get-flush.md) — Скинути буфер виводу, повернути його у вигляді рядка та вимкнути буферизацію виводу
    -   [проgetlength](function.ob-get-length.md) — Повертає розмір буфера виводу
    -   [проgetlevel](function.ob-get-level.md) — Повертає рівень вкладеності механізму буферизації виводу
    -   [проgetstatus](function.ob-get-status.md) — Отримати статус буфера виводу
    -   [проgzhandler](function.ob-gzhandler.md) - callback-функція, що використовується для gzip-стиснення буфера виводу при виклику obstart
    -   [про implicit flush](function.ob-implicit-flush.md) — Увімкнення/вимкнення неявного скидання
    -   [проlisthandlers](function.ob-list-handlers.md) - Список всіх використовуваних обробників виводу
    -   [проstart](function.ob-start.md) — Увімкнення буферизації виводу
    -   [outputaddrewritevar](function.output-add-rewrite-var.md) — Додати значення до обробника URL
    -   [outputresetrewritevars](function.output-reset-rewrite-vars.md) — Скинути значення обробника URL
