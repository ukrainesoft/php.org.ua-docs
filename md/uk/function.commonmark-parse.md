Розбір

-   [« Функции CommonMark](ref.cmark.md)
    
-   [CommonMarkRender »](function.commonmark-render.html)
    
-   [PHP Manual](index.md)
    
-   [Функции CommonMark](ref.cmark.md)
    
-   Розбір
    

# CommonMarkParse

(cmark >= 1.0.0)

CommonMarkParse - Розбір

### Опис

```methodsynopsis
CommonMark\Parse(string $content, int $options = ?): CommonMark\Node
```

Розбирає `content`

### Список параметрів

`content`

Рядок markdown

`options`

Маска з:

**`CommonMark\Parser\Normal`** (int)

**`CommonMark\Parser\Normalize`** (int)

**`CommonMark\Parser\ValidateUTF8`** (int)

**`CommonMark\Parser\Smart`** (int)

### Значення, що повертаються

Поверне кореневий (root) вузол CommonMarkNode