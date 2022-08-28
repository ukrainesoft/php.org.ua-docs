Отримання поточного значення конфігурації конфігурації magicquotesruntime

-   [« get\_magic\_quotes\_gpc](function.get-magic-quotes-gpc.html)
    
-   [get\_required\_files »](function.get-required-files.html)
    
-   [PHP Manual](index.html)
    
-   [Опции PHP/информационные функции](ref.info.html)
    
-   Отримання поточного значення конфігурації конфігурації magicquotesruntime
    

# getmagicquotesruntime

(PHP 4, PHP 5, PHP 7)

getmagicquotesruntime — Отримання поточного значення конфігурації конфігурації magicquotesruntime

**Увага**

Ця функція *ЗАСТАРІЛА*, починаючи з PHP 7.4.0 і була *ВИДАЛЕНО*починаючи з PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
get_magic_quotes_runtime(): bool
```

Повертає поточне значення налаштування [magic\_quotes\_runtime](info.configuration.html#ini.magic-quotes-runtime)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає 0, якщо опція magicquotesruntime вимкнена, 1 або. З версії PHP 5.4.0 завжди повертає **`false`**

### список змін

| Версия | Описание                      |
|--------|-------------------------------|
|        | Функцію оголошено застарілою. |

### Приклади

**Приклад #1 Приклад використання **getmagicquotesruntime()****

```php
<?php
// Проверка, работает ли magic_quotes_runtime
if (get_magic_quotes_runtime())
{
    // отключение
    set_magic_quotes_runtime(false);
}
?>
```

### Дивіться також

-   [get\_magic\_quotes\_gpc()](function.get-magic-quotes-gpc.html) - Отримання поточного значення конфігурації конфігурації magicquotesgpc