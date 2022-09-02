---
navigation:
  - componere.cast_by_ref.md: « Componerecastбref
  - intro.errorfunc.md: Введение »
  - index.md: PHP Manual
  - refs.basic.php.md: Изменение поведения PHP
title: Обробка та логування помилок
---
# Обробка та логування помилок

-   [Введение](intro.errorfunc.md)
-   [Встановлення та налаштування](errorfunc.setup.md)
    -   [Вимоги](errorfunc.requirements.md)
    -   [Установка](errorfunc.installation.md)
    -   [Налаштування під час виконання](errorfunc.configuration.md)
    -   [Типи ресурсів](errorfunc.resources.md)
-   [Обумовлені константи](errorfunc.constants.md)
-   [Приклади](errorfunc.examples.md)
-   [Функции обработки ошибок](ref.errorfunc.md)
    -   [debugbacktrace](function.debug-backtrace.md) — Виводить стек викликів функцій у масив
    -   [debugprintbacktrace](function.debug-print-backtrace.md) — Виводить стек викликів функцій
    -   [errorclearlast](function.error-clear-last.md) — Очистити останню помилку
    -   [errorgetlast](function.error-get-last.md) — Отримання інформації про останню помилку, що сталася
    -   [errorlog](function.error-log.md) — Надсилає повідомлення про помилку заданому обробнику помилок
    -   [errorreporting](function.error-reporting.md) - Задає, які помилки PHP потраплять у звіт
    -   [restoreerrorhandler](function.restore-error-handler.md) — Відновлює попередній обробник помилок
    -   [restoreexceptionhandler](function.restore-exception-handler.md) — Відновлює попередній обробник винятків
    -   [seterrorhandler](function.set-error-handler.md) — Задає користувальницький обробник помилок
    -   [setexceptionhandler](function.set-exception-handler.md) - Задає користувальницький обробник винятків
    -   [triggererror](function.trigger-error.md) — Викликає помилку користувача/попередження/сповіщення
    -   [usererror](function.user-error.md) - Псевдонім triggererror
