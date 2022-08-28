Видаляє директорію

-   [« streamWrapper::rename](streamwrapper.rename.html)
    
-   [streamWrapper::stream\_cast »](streamwrapper.stream-cast.html)
    
-   [PHP Manual](index.html)
    
-   [streamWrapper](class.streamwrapper.html)
    
-   Видаляє директорію
    

# streamWrapper::rmdir

(PHP 5, PHP 7, PHP 8)

streamWrapper::rmdir — Видаляє директорію

### Опис

```methodsynopsis
public streamWrapper::rmdir(string $path, int $options): bool
```

Цей метод викликається у процесі виконання [rmdir()](function.rmdir.html)

> **Зауваження**
> 
> Щоб повідомлення про помилки відповідали реальним помилкам, цей метод *не потрібно* визначати у випадках, коли обгортка не підтримує видалення директорій.

### Список параметрів

`path`

URL директорії, що видаляється.

`options`

Бітова маска, складена з констант, начебто **`STREAM_MKDIR_RECURSIVE`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо виклик до цього методу не вдалося (наприклад, не реалізовано).

### Примітки

> **Зауваження**
> 
> Властивість streamWrapper::$context буде оновлено, якщо коректний контекст був переданий у функцію, що викликається.

### Дивіться також

-   [rmdir()](function.rmdir.html) - видаляє директорію
-   [streamwrapper::mkdir()](streamwrapper.mkdir.html) - створення директорії
-   [streamwrapper::unlink()](streamwrapper.unlink.html) - Видалення файлу