Виконати рядок як код Javascript

-   [« V8Js::construct](v8js.construct.md)
    
-   [V8Js::getExtensions »](v8js.getextensions.md)
    
-   [PHP Manual](index.md)
    
-   [V8Js](class.v8js.md)
    
-   Виконати рядок як код Javascript
    

# V8Js::executeString

(PECL v8js >= 0.1.0)

V8Js::executeString — Виконати рядок як код Javascript

### Опис

```methodsynopsis
public V8Js::executeString(string $script, string $identifier = "V8Js::executeString()", int $flags = V8Js::FLAG_NONE): mixed
```

Компілює та виконує рядок, переданий у параметр `script`як код Javascript.

### Список параметрів

`script`

Рядок, що містить код для виконання.

`identifier`

Рядок ідентифікатор для запущеного коду. Використовується для налагодження.

`flags`

Прапори запуску. Значення має бути однією з констант `V8Js::FLAG_*`, за замовчуванням **`V8Js::FLAG_NONE`**

-   **`V8Js::FLAG_NONE`**: без прапорів
    
-   **`V8Js::FLAG_FORCE_ARRAY`**: змушує об'єкти JS бути асоціативними масивами PHP
    

### Значення, що повертаються

Повертає останню змінну, створену в коді Javascript, попередньо сконвертувавши її у відповідний тип PHP.