Отримати тип варіанта

-   [« variantfix](function.variant-fix.html)
    
-   [variantidiv »](function.variant-idiv.html)
    
-   [PHP Manual](index.md)
    
-   [Функции COM](ref.com.md)
    
-   Отримати тип варіанта
    

# variantgettype

(PHP 5, PHP 7, PHP 8)

variantgettype — Отримати тип варіанта

### Опис

```methodsynopsis
variant_get_type(variant $variant): int
```

Повертає тип об'єкта варіанта.

### Список параметрів

`variant`

Різновид.

### Значення, що повертаються

Функція повертає ціле значення, що означає тип `variant`, який може бути екземпляром класів [com](class.com.md) [dotnet](class.dotnet.md) або [variant](class.variant.md). Повертається значення одно з констант **`VT_XXX`**

Значення, що повертається для об'єктів COM і DOTNET зазвичай дорівнює **`VT_DISPATCH`**; єдина причина, чому ця функція працює для цих класів полягає в тому, що COM та DOTNET є нащадками VARIANT.

### Дивіться також

-   [variantsettype()](function.variant-set-type.html) - Приведення варіанта до іншого типу "за місцем"