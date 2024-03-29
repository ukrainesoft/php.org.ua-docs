---
navigation:
  - outcontrol.user-level-output-buffers.md: « Користувальницькі буфери виводу
  - outcontrol.nesting-output-buffers.md: Вкладені буфери виводу »
  - index.md: PHP Manual
  - outcontrol.user-level-output-buffers.md: Буфери виводу користувача
title: Який висновок буферизується?
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Який висновок буферизується?

Користувальницькі буфери виведення PHP після запуску повністю буферизують виведення до тих пір, поки вони не будуть вимкнені або скрипт не завершить роботу. Висновок у контексті буфера виведення PHP — це все, що PHP відобразив або відправив назад в браузер. З практичної точки зору, висновок – це дані ненульової довжини, які:

-   написані за межами тегів`<?php ?>`
-   виводять мовні конструкції і функції, явна мета яких - виведення змін або рядків, як наприклад:[echo](function.echo.md) [print](function.print.md) [printf()](function.printf.md) [var\_dump()](function.var-dump.md) [var\_export()](function.var-export.md) [vprintf()](function.vprintf.md)
-   виводять функції, мета яких - збирання та виведення даних або інформації про запущений скрипт або PHP, як наприклад:[debug\_print\_backtrace()](function.debug-print-backtrace.md) [phpcredits()](function.phpcredits.md) [phpinfo()](function.phpinfo.md) [ReflectionExtension::info()](reflectionextension.info.md)
-   виводить PHP за неперехопленого виключення або необробленої помилки (за умови, що включені директиви[display\_errors](errorfunc.configuration.md#ini.display-errors) і [error\_reporting](errorfunc.configuration.md#ini.error-reporting)) .
-   записують у потік`php://output`

> **Зауваження**: Дані, які записуються відразу в потік виводу (`stdout`) або передаються у функцію SAPI з схожою функціональністю, не будуть захоплені користувальницькими буферами виводу. У це включено запис даних стандартний потік виведення (`stdout`) функцією [fwrite()](function.fwrite.md) або надсилання заголовків функціями [header()](function.header.md) або [setcookie()](function.setcookie.md)
