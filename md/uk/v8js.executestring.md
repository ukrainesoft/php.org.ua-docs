---
navigation:
  - v8js.construct.md: '« V8Js::\_\_construct'
  - v8js.getextensions.md: 'V8Js::getExtensions »'
  - index.md: PHP Manual
  - class.v8js.md: V8Js
title: 'V8Js::executeString'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Прапори запуску. Значення має бути однією з констант `V8Js::FLAG_*`, по умолчанию\*\*`V8Js::FLAG_NONE`\*\*

-   **`V8Js::FLAG_NONE`**: без прапорів
    
-   **`V8Js::FLAG_FORCE_ARRAY`**: змушує об'єкти JS бути асоціативними масивами PHP
    

### Значення, що повертаються

Повертає останню змінну, створену в коді Javascript, попередньо сконвертувавши її у відповідний тип PHP.
