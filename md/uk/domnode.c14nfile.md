Канонізувати вузли у файл

-   [« DOMNode::C14N](domnode.c14n.html)
    
-   [DOMNode::cloneNode »](domnode.clonenode.html)
    
-   [PHP Manual](index.html)
    
-   [DOMNode](class.domnode.html)
    
-   Канонізувати вузли у файл
    

# DOMNode::C14NFile

(PHP 5> = 5.2.0, PHP 7, PHP 8)

DOMNode::C14NFile — Канонізувати вузли у файл

### Опис

```methodsynopsis
public DOMNode::C14NFile(    string $uri,    bool $exclusive = false,    bool $withComments = false,    ?array $xpath = null,    ?array $nsPrefixes = null): int|false
```

Канонізувати вузли у файл.

### Список параметрів

`uri`

Шлях для запису виводу.

`exclusive`

Включити ексклюзивний розбір лише тих вузлів, які збігаються з наданими xpath або nsprefixes.

`withComments`

Зберігати коментарі у висновку.

`xpath`

Масив `xpath` для фільтрації вузлів.

`nsPrefixes`

Масив префіксів просторів імен фільтрації вузлів.

### Значення, що повертаються

Кількість записаних байт або **`false`** у разі виникнення помилки

### Дивіться також

-   [DOMNode::C14N()](domnode.c14n.html) - Канонізувати вузли в рядок