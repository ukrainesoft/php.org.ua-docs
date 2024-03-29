---
navigation:
  - function.com-get-active-object.md: « com\_get\_active\_object
  - function.com-message-pump.md: com\_message\_pump »
  - index.md: PHP Manual
  - ref.com.md: Функції COM
title: com\_load\_typelib
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# com\_load\_typelib

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

com\_load\_typelib — Завантаження Typelib

### Опис

```methodsynopsis
com_load_typelib(string $typelib, bool $case_insensitive = true): bool
```

Завантажує бібліотеку типів та реєструє її константи таким чином, якби вони були визначені через [define()](function.define.md)

Зверніть увагу, що набагато ефективніше використовувати опцію конфігурації php.ini [com.typelib-file](com.configuration.md#ini.com.typelib-file) для передзавантаження та реєстрації констант. З іншого боку, такий метод менш гнучкий.

Якщо [com.autoregister-typelib](com.configuration.md#ini.com.autoregister-typelib) включено, то PHP постарається автоматично зареєструвати константи, асоційовані з об'єктом COM, коли ви створюватимете його екземпляр. Але така поведінка залежить від інтерфейсу об'єкта COM і може бути недоступною.

### Список параметрів

`typelib`

`typelib`принимает следующие значения:

-   Имя`.tlb`\-файлу або модуль, що містить бібліотеку типів.
    
-   GUID бібліотеки типів, після якого вказано номер версії, наприклад,`{00000200-0000-0010-8000-00AA006D2EA4},2,0`
    
-   Ім'я бібліотеки типів, наприклад,`Microsoft OLE DB ActiveX Data Objects 1.0 Library`
    

PHP намагатиметься визначити бібліотеку в такому порядку. Кожен наступний пункт є дуже витратним за ресурсами ніж попередній. Тобто. краще вказувати .tbl-файл, якщо неможливо, то GUID і якщо зовсім погано - тоді ім'я бібліотеки. Пошук бібліотеки на ім'я, наприклад, призведе до перебору всіх записів регістру.

`case_insensitive`

`case_insensitive` веде себе протилежно до параметра `$case_insensitive` у функції [define()](function.define.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
