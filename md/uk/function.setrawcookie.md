Надсилає cookie без URL-кодування значення

-   [« setcookie](function.setcookie.md)
    
-   [socketgetstatus »](function.socket-get-status.html)
    
-   [PHP Manual](index.md)
    
-   [Мережеві функції](ref.network.md)
    
-   Надсилає cookie без URL-кодування значення
    

# setrawcookie

(PHP 5, PHP 7, PHP 8)

setrawcookie — Надсилає cookie без URL-кодування значення

### Опис

```methodsynopsis
setrawcookie(    string $name,    string $value = ?,    int $expires_or_options = 0,    string $path = ?,    string $domain = ?,    bool $secure = false,    bool $httponly = false): bool
```

Альтернативна сигнатура доступна з PHP 7.3.0 (іменовані параметри не підтримуються):

```methodsynopsis
setrawcookie(string $name, string $value = ?, array $options = []): bool
```

Функція **setrawcookie()** є повним аналогом функції [setcookie()](function.setcookie.md), за винятком того, що значення cookie не буде автоматично закодовано під час надсилання браузеру.

### Список параметрів

Для отримання інформації про параметр, дивіться документацію по функції [setcookie()](function.setcookie.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                            |
|--------|-------------------------------------------------------------------------------------------------------------------------------------|
|        | Додано альтернативний підпис, що підтримує масив опцій `options`. Цей підпис також підтримує налаштування cookie-атрибута SameSite. |

### Дивіться також

-   [setcookie()](function.setcookie.md) - Надсилає cookie