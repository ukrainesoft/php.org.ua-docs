---
navigation:
  - exec.constants.md: « Зумовлені константи
  - function.escapeshellarg.md: escapeshellarg »
  - index.md: PHP Manual
  - book.exec.md: Запуск програми
title: Функції запуску програм
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Функції запуску програм

## Примітки

**Увага**

Відкриті файли з блокуванням (особливо відкриті сесії) мають бути закриті до виконання програми на тлі.

## Дивіться також

Ці функції також тісно пов'язані з оператором [зворотні лапки (\`\`) .](language.operators.execution.md)

## Зміст

-   [escapeshellarg](function.escapeshellarg.md)— Екранувати рядок для того, щоб він міг бути використаний як аргумент командного рядка
-   [escapeshellcmd](function.escapeshellcmd.md)— Екранувати метасимволи командного рядка
-   [exec](function.exec.md)— Виконати зовнішню програму
-   [passthru](function.passthru.md)— Виконати зовнішню програму та відобразити необроблений висновок
-   [proc\_close](function.proc-close.md)— Завершити процес, відкритий proc\_open та повернути код повернення цього процесу
-   [proc\_get\_status](function.proc-get-status.md)— Отримати інформацію про процес, відкритий proc\_open
-   [proc\_nice](function.proc-nice.md)— Змінити пріоритет поточного процесу
-   [proc\_open](function.proc-open.md)— Виконати команду та відкрити покажчик на файл для введення/виводу
-   [proc\_terminate](function.proc-terminate.md)— Знищити процес, відкритий за допомогою функції proc\_open
-   [shell\_exec](function.shell-exec.md)— Виконати команду через оболонку та повернути висновок у вигляді рядка
-   [system](function.system.md)— Виконати зовнішню програму та відобразити висновок
