---
navigation:
  - migration83.constants.md: « Нові глобальні константи
  - migration83.deprecated.md: Застаріла функціональність »
  - index.md: PHP Manual
  - migration83.md: Міграція з PHP 8.2.x на PHP 8.3.x
title: 'Зміни, що ламають зворотну сумісність'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Зміни, що ламають зворотну сумісність

### Ядро PHP

#### Програми, які були дуже близькими до переповнення стека викликів

Програми, які були дуже близькими до переповнення стека викликів, тепер можуть викидати виняток [Error](class.error.md), коли зайнятий у байтах розмір стека більший, ніж визначено в налаштуванні zend.max\_allowed\_stack\_size-zend.reserved\_stack\_size (fiber.stack\_size-zend.reserved\_stack\_size для файберів).

#### Виконання функції proc\_get\_status() кілька разів

Виконання функції proc\_get\_status() кілька разів тепер завжди повертає правильне значення у POSIX-системах. Раніше лише перший виклик функції повертав правильне значення. Виконання функції [proc\_close()](function.proc-close.md) після функції [proc\_get\_status()](function.proc-get-status.md) тепер повертає правильний код виходу. Раніше це повернуло б значення `-1`. Внутрішньо це працює через кешування результатів на POSIX-системах. Якщо потрібна колишня поведінка, можна перевірити ключ `«cached»` у масиві, який повертає функція [proc\_get\_status()](function.proc-get-status.md), щоб перевірити, чи кешували результат.

#### Таймери Zend Max Execution

Таймери Zend Max Execution тепер за замовчуванням включені для збирання ZTS в системах Linux.

#### Увімкнення трейтів зі статичними властивостями

Включення трейтів зі статичними властивостями тепер повторно визначатиме статичні властивості, успадковані з батьківського класу. Це створить різні сховища статичних якостей для поточного класу. Це аналогічно додаванню статичної якості у класі, без трейтів.

#### Надання негативного індексу порожньому масиву

При додаванні до масиву з зайнятим негативним індексом, який, припустимо, зберігається в змінній $n, нового значення, наступний індекс отримає значення `$n + 1`, а не

#### Перевірка невідповідності видимості констант класів

Невідповідність видимості констант класів тепер буде коректно перевірено під час реалізації інтерфейсів.

#### Записи WeakMap, ключ яких відповідає самим собі

Записи об'єкту [WeakMap](class.weakmap.md), ключ яких зіставлений із собою, (можливо, транзитивно) тепер можна видалити під час збору циклу якщо ключ недоступний, крім шляхом перебору значень WeakMap (доступність під час перебору вважається слабкої). Раніше такі записи не видалялися б автоматично.

### Модуль Date

Замість попереджень та загальних винятків у модуль DateTime були додані властиві тільки йому винятки та помилки в ієрархії класів [DateError](class.dateerror.md) і [DateException](class.dateexception.md). Це покращує обробку помилок та винятків, коли потрібно перевірити їх існування.

### Модуль DOM

Виклик методів [DOMChildNode::after()](domchildnode.after.md) [DOMChildNode::before()](domchildnode.before.md) і [DOMChildNode::replaceWith()](domchildnode.replacewith.md) на вузлі, у якого немає батьківського вузла, тепер непрацездатно, а не винятком ієрархії, щоб поведінка була сумісною зі специфікацією DOM.

Виклик методів класів [DOMParentNode](class.domparentnode.md) і [DOMChildNode](class.domchildnode.md) без документа тепер працює, а не викидає винятки \*\*`DOM_HIERARCHY_REQUEST_ERR`\*\*класса[DOMException](class.domexception.md). Це відповідає поведінці специфікації DOM.

Виклик методу [DOMDocument::createAttributeNS()](domdocument.createattributens.md) без префікса неправильно створив простір імен за умовчанням, поміщаючи елемент всередину простору імен замість атрибута. Цю помилку тепер виправлено.

Метод[DOMDocument::createAttributeNS()](domdocument.createattributens.md)раньше неправильно бросал исключение\*\*`DOM_NAMESPACE_ERRNAMESPACE_ERR`\*\*класса[DOMException](class.domexception.md)коли префікс вже був зайнятий іншим URI. Тепер він правильно обирає інший префікс у разі конфлікту префіксів.

Нові методи та властивості були додані до ряду класів DOM. Якщо клас класу успадковується від цих класів і оголошує метод або властивість з таким же ім'ям, воно має бути сумісним. В інших випадках буде викинуто типову помилку компіляції про несумісність. Ознайомитись зі списком нових методів та властивостей можна у розділах [список нової функціональності](migration83.new-features.md#migration83.new-features.dom) і [нові функції](migration83.new-functions.md#migration83.new-functions.dom)

### Клас FFI

Функції мови Сі, для яких заданий тип void, що повертається, тепер повертають значення **`null`** замість замість об'єкта `object(FFI\CData:void) { }`

### Модуль Opcache

Налаштування INI-директиви [opcache.consistency\_checks](opcache.configuration.md#ini.opcache.consistency-checks) було видалено. Ця функція не працювала при трасуванні JIT, а також з кешем успадкування і була відключена в PHP 8.1.18 та PHP 8.2.5; тепер її неможливо увімкнути. І трасуючий JIT, і кеш успадкування можуть змінити пам'ять (shm), що розділяється, після збереження скрипту шляхом анулювання його контрольної суми. Були спроби виправити пропуски через покажчики, що модифікуються, але була відхилена через складність. Через це вирішили видалити цю функцію.

### Модуль Phar

Тип констант класса[Phar](class.phar.md) тепер оголошено.

### Стандартні функції

У функцію [range()](function.range.md) було внесено низку змін:

-   Тепер викидається виняток[TypeError](class.typeerror.md), коли об'єкти (object), ресурси (resource) чи масиви (array) передаються як граничних значень.
-   Тепер під час передачі у параметр`$step`значення викидається докладніше описаний виняток[ValueError](class.valueerror.md)
-   Тепер викидається виняток[ValueError](class.valueerror.md), когда в параметр`$step`передаються негативні значення збільшення діапазонів.
-   Якщо параметр `$step`передається число з плаваючою точкою, яке може бути інтерпретовано як ціле число, воно так і оцінюється.
-   Тепер викидається виняток[ValueError](class.valueerror.md)якщо будь-який аргумент представляє нескінченне число або нечисло (NAN).
-   Тепер викликається помилка рівня\*\*`E_WARNING`\*\*, якщо параметр `$start`или`$end`приймає значення порожнього рядка. Значення продовжує наводитися до значення
-   Тепер викликається помилка рівня\*\*`E_WARNING`\*\*, якщо параметр `$start`или`$end`приймає нечисловий рядок розміром більше одного байта.
-   Тепер викликається помилка рівня\*\*`E_WARNING`\*\*, якщо значення, передане до параметра`$start`или`$end`, наводиться до цілого числа через те, що інше значення - число (наприклад,`range(5, 'z');`
-   Тепер при спробі згенерувати діапазон символів викликається помилка рівня\*\*`E_WARNING`\*\*, если значение параметра`$step`— це число з плаваючою точкою, крім випадків, коли обидва вхідні значення — числові рядки (наприклад,`range('5', '9', 0.5);`не викличе попередження).
-   Тепер замість приведення одного зі значень до цілого числа функція[range()](function.range.md)створює список символів, якщо один із них — це числовий рядок (наприклад,`range('9', 'A');`

```php
<?php

range('9', 'A');  // ["9", ":", ";", "<", "=", ">", "?", "@", "A"], начиная с PHP 8.3.0
range('9', 'A');  // [9, 8, 7, 6, 5, 4, 3, 2, 1, 0], до PHP 8.3.0
```

Прапори перевірки помилок у функції [file()](function.file.md) тепер перехоплює усі неприпустимі прапори. Константа \*\*`FILE_APPEND`\*\*ранее молча принималась.

### SNMP

Тип констант класса[SNMP](class.snmp.md) тепер оголошено.
