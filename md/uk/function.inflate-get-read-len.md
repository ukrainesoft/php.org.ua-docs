Отримує кількість прочитаних байт

-   [« inflateadd](function.inflate-add.html)
    
-   [inflategetstatus »](function.inflate-get-status.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Zlib](ref.zlib.md)
    
-   Отримує кількість прочитаних байт
    

# inflategetreadlen

(PHP 7> = 7.2.0, PHP 8)

inflategetreadlen — Отримує кількість прочитаних байт

### Опис

```methodsynopsis
inflate_get_read_len(InflateContext $context): int
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`context`

### Значення, що повертаються

Повертає кількість прочитаних байт або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `context` чекає на екземпляр [InflateContext](class.inflatecontext.md); раніше, очікувався ресурс (resource). |