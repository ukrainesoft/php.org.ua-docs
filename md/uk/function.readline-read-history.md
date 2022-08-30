Прочитати історію команд із файлу

-   [« readlineвінnewline](function.readline-on-new-line.html)
    
-   [readlineredisplay »](function.readline-redisplay.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Readline](ref.readline.md)
    
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