---
navigation:
  - streamwrapper.stream-open.md: '« streamWrapper::stream\_open'
  - streamwrapper.stream-seek.md: 'streamWrapper::stream\_seek »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::stream\_read'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# streamWrapper::stream\_read

(PHP 4 >= 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::stream\_read — Читає з потоку

### Опис

```methodsynopsis
public streamWrapper::stream_read(int $count): string|false
```

Цей метод викликається у процесі виконання функцій [fread()](function.fread.md) і [fgets()](function.fgets.md)

> **Зауваження** :
> 
> Не забувайте оновлювати позицію читання/запису у потоці (на кількість успішно прочитаних байт).

### Список параметрів

`count`

Скільки байт даних від поточної позиції має бути повернуто.

### Значення, що повертаються

Якщо в потоці кількість доступних байт менша, ніж `count`, має бути повернуто стільки даних, скільки доступно. Якщо доступних даних немає, функція повертає **`false`**

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо виклик до цього методу не вдалося (наприклад, не реалізовано).

> **Зауваження** :
> 
> Якщо значення, що повертається, буде більше, ніж `count`, то буде викликана помилка **`E_WARNING`**, та дані більш зазначеної кількості будуть втрачені.

### Примітки

> **Зауваження** :
> 
> [streamWrapper::stream\_eof()](streamwrapper.stream-eof.md) викликається відразу після виклику **streamWrapper::stream\_read()**, щоб перевірити, чи кінець файлу EOF досягнуто. Якщо метод не реалізований, то вважається, що кінець EOF файлу досягнутий.

**Увага**

При читанні файлу повністю (наприклад, функцією [file\_get\_contents()](function.file-get-contents.md)), PHP буде викликати **streamWrapper::stream\_read()**и вместе с ним[streamWrapper::stream\_eof()](streamwrapper.stream-eof.md)в цикле, пока**streamWrapper::stream\_read()** повертає непустий рядок. Повертається з [streamWrapper::stream\_eof()](streamwrapper.stream-eof.md) значення у своїй ігнорується.

### Дивіться також

-   [fread()](function.fread.md) \- Бінарно-безпечне читання файлу
-   [fgets()](function.fgets.md) \- Читає рядок із файлу
