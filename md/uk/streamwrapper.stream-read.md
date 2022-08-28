Читає із потоку

-   [« streamWrapper::stream\_open](streamwrapper.stream-open.html)
    
-   [streamWrapper::stream\_seek »](streamwrapper.stream-seek.html)
    
-   [PHP Manual](index.html)
    
-   [streamWrapper](class.streamwrapper.html)
    
-   Читає із потоку
    

# streamWrapper::streamread

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::streamread — Читає з потоку

### Опис

```methodsynopsis
public streamWrapper::stream_read(int $count): string|false
```

Цей метод викликається у процесі виконання функцій [fread()](function.fread.html) і [fgets()](function.fgets.html)

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
> [streamWrapper::stream\_eof()](streamwrapper.stream-eof.html) викликається відразу після виклику **streamWrapper::streamread()**, щоб перевірити, чи кінець файлу EOF досягнуто. Якщо метод не реалізований, то вважається, що кінець EOF файлу досягнутий.

**Увага**

При читанні файлу повністю (наприклад, функцією [file\_get\_contents()](function.file-get-contents.html)), PHP буде викликати **streamWrapper::streamread()** і разом із ним [streamWrapper::stream\_eof()](streamwrapper.stream-eof.html) у циклі, поки **streamWrapper::streamread()** повертає непустий рядок. Повертається з [streamWrapper::stream\_eof()](streamwrapper.stream-eof.html) значення у своїй ігнорується.

### Дивіться також

-   [fread()](function.fread.html) - Бінарно-безпечне читання файлу
-   [fgets()](function.fgets.html) - Читає рядок із файлу