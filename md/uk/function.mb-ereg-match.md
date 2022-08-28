Збіг з регулярним виразом для багатобайтового рядка

-   [« mb\_encoding\_aliases](function.mb-encoding-aliases.html)
    
-   [mb\_ereg\_replace\_callback »](function.mb-ereg-replace-callback.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с многобайтовыми строками](ref.mbstring.html)
    
-   Збіг з регулярним виразом для багатобайтового рядка
    

# мбeregmatch

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

мбeregmatch — Збіг з регулярним виразом для багатобайтового рядка

### Опис

```methodsynopsis
mb_ereg_match(string $pattern, string $string, ?string $options = null): bool
```

Збіг з регулярним виразом для багатобайтового рядка.

> **Зауваження** `pattern` зіставляється лише на початку `string`

### Список параметрів

`pattern`

Шаблон регулярного виразу.

`string`

Оцінений рядок (string).

`options`

Опція пошуку. Детальніше дивіться [mb\_regex\_set\_options()](function.mb-regex-set-options.html)

### Значення, що повертаються

Повертає **`true`**, якщо `string` збігається з регулярним виразом `pattern` **`false`** - в іншому випадку.

### список змін

| Версия | Описание                                |
|--------|-----------------------------------------|
|        | `options` тепер допускає значення null. |

### Примітки

> **Зауваження**
> 
> Для цієї функції буде використано внутрішнє кодування або кодування, встановлене функцією [mb\_regex\_encoding()](function.mb-regex-encoding.html)

### Дивіться також

-   [mb\_regex\_encoding()](function.mb-regex-encoding.html) - Встановлює/отримує поточне кодування для багатобайтового регулярного виразу
-   [mb\_ereg()](function.mb-ereg.html) - Збіг з регулярним виразом з підтримкою багатобайтових кодувань