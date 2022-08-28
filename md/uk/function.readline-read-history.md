Прочитати історію команд із файлу

-   [« readline\_on\_new\_line](function.readline-on-new-line.html)
    
-   [readline\_redisplay »](function.readline-redisplay.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Readline](ref.readline.html)
    
-   Прочитати історію команд із файлу
    

# readlinereadhistory

(PHP 4, PHP 5, PHP 7, PHP 8)

readlinereadhistory — Прочитати історію команд із файлу

### Опис

```methodsynopsis
readline_read_history(?string $filename = null): bool
```

Функція читає історію команд із файлу.

### Список параметрів

`filename`

Шлях до файлу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `filename` тепер допускає значення null. |