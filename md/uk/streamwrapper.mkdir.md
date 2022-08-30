Створення директорії

-   [« streamWrapper::dirrewinddir](streamwrapper.dir-rewinddir.html)
    
-   [streamWrapper::rename »](streamwrapper.rename.html)
    
-   [PHP Manual](index.html)
    
-   [streamWrapper](class.streamwrapper.html)
    
-   Створення директорії
    

# streamWrapper::mkdir

(PHP 5, PHP 7, PHP 8)

streamWrapper::mkdir — Створення директорії

### Опис

```methodsynopsis
public streamWrapper::mkdir(string $path, int $mode, int $options): bool
```

Цей метод викликається у процесі виконання [mkdir()](function.mkdir.html)

> **Зауваження**
> 
> Щоб повідомлення про помилки відповідали реальним помилкам, цей метод *не потрібно* визначати у випадках, коли обгортка не підтримує створення директорій.

### Список параметрів

`path`

Створювана директорія.

`mode`

Значення, передане в [mkdir()](function.mkdir.html)

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

-   [mkdir()](function.mkdir.html) - створює директорію
-   [streamwrapper::rmdir()](streamwrapper.rmdir.html) - видаляє директорію