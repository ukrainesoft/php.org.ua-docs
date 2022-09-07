---
navigation:
  - streamwrapper.stream-open.md: '« streamWrapper::streamopen'
  - streamwrapper.stream-seek.md: 'streamWrapper::streamseek »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::streamread'
---
# streamWrapper::streamread

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::streamread — Читає з потоку

### Опис

```methodsynopsis
public streamWrapper::stream_read(int $count): string|false
```

Цей метод викликається у процесі виконання функцій [fread()](function.fread.md) і [fgets()](function.fgets.md)

> **Зауваження**
> 
> Не забувайте оновлювати позицію читання/запису у потоці (на кількість успішно прочитаних байт).

### Список параметрів

`count`

Скільки байт даних від поточної позиції має бути повернено.

### Значення, що повертаються

Якщо в потоці кількість доступних байт менша, ніж `count`, має бути повернуто стільки даних, скільки доступно. Якщо доступних даних немає, функція повертає **`false`**

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо виклик до цього методу не вдалося (наприклад, не реалізовано).

> **Зауваження**
> 
> Якщо значення, що повертається, буде більше, ніж `count`, то буде викликана помилка **`E_WARNING`**, та дані більш зазначеної кількості будуть втрачені.

### Примітки

> **Зауваження**
> 
> [streamWrapper::streameof()](streamwrapper.stream-eof.md) викликається відразу після виклику **streamWrapper::streamread()**, щоб перевірити, чи кінець файлу EOF досягнуто. Якщо метод не реалізований, то вважається, що кінець EOF файлу досягнутий.

**Увага**

При читанні файлу повністю (наприклад, функцією [filegetcontents()](function.file-get-contents.md)), PHP буде викликати **streamWrapper::streamread()** і разом із ним [streamWrapper::streameof()](streamwrapper.stream-eof.md) у циклі, поки **streamWrapper::streamread()** повертає непустий рядок. Повертається з [streamWrapper::streameof()](streamwrapper.stream-eof.md) значення у своїй ігнорується.

### Дивіться також

-   [fread()](function.fread.md) - Бінарно-безпечне читання файлу
-   [fgets()](function.fgets.md) - Читає рядок із файлу
