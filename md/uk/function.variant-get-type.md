---
navigation:
  - function.variant-fix.md: « variant\_fix
  - function.variant-idiv.md: variant\_idiv »
  - index.md: PHP Manual
  - ref.com.md: Функції COM
title: variant\_get\_type
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# variant\_get\_type

(PHP 5, PHP 7, PHP 8)

variant\_get\_type — Отримати тип варіанта

### Опис

```methodsynopsis
variant_get_type(variant $variant): int
```

Повертає тип об'єкта варіанта.

### Список параметрів

`variant`

Варіант.

### Значення, що повертаються

Функция возвращает целочисленное значение, обозначающее тип`variant`, який може бути екземпляром класів [com](class.com.md) [dotnet](class.dotnet.md) або [variant](class.variant.md). Повертається значення одно з констант **`VT_XXX`**

Значення, що повертається для об'єктів COM і DOTNET зазвичай дорівнює **`VT_DISPATCH`**; єдина причина, чому ця функція працює для цих класів полягає в тому, що COM та DOTNET є нащадками VARIANT.

### Дивіться також

-   [variant\_set\_type()](function.variant-set-type.md) \- Наводить варіант до іншого типу «за місцем»
