Перейменовує файл або директорію

-   [« streamWrapper::mkdir](streamwrapper.mkdir.md)
    
-   [streamWrapper::rmdir »](streamwrapper.rmdir.md)
    
-   [PHP Manual](index.md)
    
-   [streamWrapper](class.streamwrapper.md)
    
-   Перейменовує файл або директорію
    

# streamWrapper::rename

(PHP 5, PHP 7, PHP 8)

streamWrapper::rename — Перейменовує файл або директорію

### Опис

```methodsynopsis
public streamWrapper::rename(string $path_from, string $path_to): bool
```

Цей метод викликається у процесі виконання [rename()](function.rename.md)

Мушу спробувати перейменувати `path_from` в `path_to`

> **Зауваження**
> 
> Щоб повідомлення про помилки відповідали реальним помилкам, цей метод *не потрібно* визначати у випадках, коли обгортка не підтримує перейменування файлів.

### Список параметрів

`path_from`

URL поточного файлу.

`path_to`

URL, до якого `path_from` має перейменований.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо виклик до цього методу не вдалося (наприклад, не реалізовано).

### Примітки

> **Зауваження**
> 
> Властивість streamWrapper::$context буде оновлено, якщо коректний контекст був переданий у функцію, що викликається.

### Дивіться також

-   [rename()](function.rename.md) - Перейменовує файл або директорію