---
navigation:
  - exec.constants.md: « Обумовлені константи
  - function.escapeshellarg.md: escapeshellarg »
  - index.md: PHP Manual
  - book.exec.md: Запуск програми
title: Функції запуску програм
---
# Функції запуску програм

## Примітки

**Увага**

Відкриті файли з блокуванням (особливо відкриті сесії) мають бути закриті до виконання програми на тлі.

## Дивіться також

Ці функції також тісно пов'язані з оператором [зворотні лапки (](language.operators.execution.md)

## Зміст

-   [escapeshellarg](function.escapeshellarg.md) — Екранувати рядок для того, щоб він міг бути використаний як аргумент командного рядка
-   [escapeshellcmd](function.escapeshellcmd.md) — Екранувати метасимволи командного рядка
-   [exec](function.exec.md) — Виконати зовнішню програму
-   [passthru](function.passthru.md) — Виконати зовнішню програму та відобразити необроблений висновок
-   [procclose](function.proc-close.md) — Завершити процес, відкритий procopen та повернути код повернення цього процесу
-   [procgetstatus](function.proc-get-status.md) — Отримати інформацію про процес, відкритий procopen
-   [procnice](function.proc-nice.md) — Змінити пріоритет поточного процесу
-   [procopen](function.proc-open.md) — Виконати команду та відкрити покажчик на файл для введення/виводу
-   [procterminate](function.proc-terminate.md) — Знищити процес, відкритий за допомогою функції procopen
-   [shellexec](function.shell-exec.md) — Виконати команду через оболонку та повернути висновок у вигляді рядка
-   [system](function.system.md) — Виконати зовнішню програму та відобразити висновок
