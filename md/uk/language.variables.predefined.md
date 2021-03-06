- [« Основи](language.variables.basics.md)
- [Область видимості змінної »](language.variables.scope.md)

- [PHP Manual](index.md)
- [Змінні](language.variables.md)
- Зумовлені змінні

## Зумовлені змінні

Будь-якому запуску скрипту PHP надає велику кількість
визначених змінних. Однак багато з цих змінних не можуть
бути повністю задокументовані, оскільки вони залежать від того, хто запускає
скрипт сервера, його версії та налаштувань, а також інших факторів.
Деякі з цих змінних недоступні, коли PHP запущено з [командної строчки](features.commandline.md). Дивіться [список зарезервованих визначених змінних](reserved.variables.md) для отримання
додаткову інформацію.

PHP надає додатковий набір певних масивів,
що містять змінні сервери (якщо вони доступні), оточення та
введення користувача. Ці масиви є особливими, оскільки вони
стають глобальними автоматично - тобто, автоматично доступні в
будь-якої області видимості. З цієї причини вони також відомі як
'автоглобальні' або 'суперглобальні' змінні. (У PHP немає механізму
що визначаються користувачем суперглобальних змінних.) Дивіться [список суперглобальних змінних](language.variables.superglobals.md) для
отримання додаткової інформації.

> **Примітка**: **Змінні змінних**
>
> Суперглобальні змінні неможливо знайти [змінними > змінних](language.variables.variable.md) всередині функцій або
> методів класу.

Якщо деякі зі змінних у
[variables_order](ini.core.md#ini.variables-order) не встановлено,
відповідні їм визначені масиви також залишаться порожніми.
