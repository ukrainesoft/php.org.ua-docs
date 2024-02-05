---
navigation:
  - componere.cast_by_ref.md: « Componere\\cast\_by\_ref
  - intro.errorfunc.md: Вступ "
  - index.md: PHP Manual
  - refs.basic.php.md: Зміна поведінки PHP
title: Обробка та логування помилок
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обробка та логування помилок

-   [Вступ](intro.errorfunc.md)
-   [Встановлення та налаштування](errorfunc.setup.md)
    -   [Вимоги](errorfunc.requirements.md)
    -   [Установка](errorfunc.installation.md)
    -   [Налаштування під час виконання](errorfunc.configuration.md)
    -   [Типи ресурсів](errorfunc.resources.md)
-   [Обумовлені константи](errorfunc.constants.md)
-   [Приклади](errorfunc.examples.md)
-   [Функції обробки помилок](ref.errorfunc.md)
    -   [debug\_backtrace](function.debug-backtrace.md) \- Генерує стек викликів функцій
    -   [debug\_print\_backtrace](function.debug-print-backtrace.md)— Виводить стек викликів функцій
    -   [error\_clear\_last](function.error-clear-last.md)— Очистити останню помилку
    -   [error\_get\_last](function.error-get-last.md)— Отримання інформації про останню помилку, що сталася
    -   [error\_log](function.error-log.md)— Надсилає повідомлення про помилку заданому обробнику помилок
    -   [error\_reporting](function.error-reporting.md) \- Встановлює, які помилки PHP потраплять у звіт
    -   [restore\_error\_handler](function.restore-error-handler.md)— Відновлює попередній обробник помилок
    -   [restore\_exception\_handler](function.restore-exception-handler.md)— Відновлює попередній обробник винятків
    -   [set\_error\_handler](function.set-error-handler.md)— Задає користувальницький обробник помилок
    -   [set\_exception\_handler](function.set-exception-handler.md) \- Задає користувальницький обробник винятків
    -   [trigger\_error](function.trigger-error.md)— Викликає помилку користувача/попередження/сповіщення
    -   [user\_error](function.user-error.md) \- Псевдонім trigger\_error
