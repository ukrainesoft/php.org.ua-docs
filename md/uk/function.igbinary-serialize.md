---
navigation:
  - ref.igbinary.md: « Функції Igbinary
  - function.igbinary-unserialize.md: igbinary\_unserialize »
  - index.md: PHP Manual
  - ref.igbinary.md: Функції Igbinary
title: igbinary\_serialize
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# igbinary\_serialize

(PECL igbinary >= 1.1.1)

igbinary\_serialize — Створює компактне, двійкове уявлення значення, що зберігається.

### Опис

```methodsynopsis
igbinary_serialize(mixed $value): string|false
```

Створює значення, що зберігається.

Корисно для зберігання або передачі значень PHP без втрати їх типу та структури.

Щоб знову перетворити серіалізований рядок на значення PHP, можна використовувати [igbinary\_unserialize()](function.igbinary-unserialize.md)

### Список параметрів

`value`

Значення, яке необхідно серіалізувати . **igbinary\_serialize()** обробляє всі типи, крім ресурсів (resource) та деяких об'єктів (object) (див. примітку нижче). Навіть масиви (array), що містять посилання на себе, можуть бути серіалізовані функцією **igbinary\_serialize()**. Циклічні посилання всередині масивів (array) або об'єктів (object), що серіалізуються, також будуть збережені. Будь-яке інше посилання буде втрачено.

При серіалізації об'єктів, igbinary намагатиметься викликати функції [\_\_serialize()](language.oop5.magic.md#object.serialize) або [\_\_sleep()](language.oop5.magic.md#object.sleep) перед серіалізацією. Це дозволить об'єкту виконати будь-яку очистку в останню хвилину тощо. перед серіалізацією. Аналогічно, коли об'єкт відновлюється за допомогою [igbinary\_unserialize()](function.igbinary-unserialize.md), викликається функція [\_\_unserialize()](language.oop5.magic.md#object.unserialize) або [\_\_wakeup()](language.oop5.magic.md#object.wakeup)

> **Зауваження** :
> 
> Початок імен закритих членів об'єкта (object) доповнюються ім'ям класу, а початок імен захищених членів символом `'*'`. Ці доповнені значення оточуються нульовим байтом з обох боків.

### Значення, що повертаються

Возвращает строку, содержащую представление потока байтов`value`, яке може бути збережене будь-де.

Зверніть увагу, що це двійковий рядок, який може включати будь-яке байтове значення і повинен зберігатися і оброблятися як такий. Наприклад, виведення функції **igbinary\_serialize()** зазвичай повинен зберігатися у полі бази даних `BLOB`, а не в поле`CHAR`или`TEXT`

### Приклади

**Пример #1 Пример использования**igbinary\_serialize()\*\*\*\*

```php
<?php
$ser = igbinary_serialize(['test', 'test']);
echo urlencode($ser), "\n";
var_export(igbinary_unserialize($ser));
?>
```

Результат виконання наведеного прикладу:

```
%00%00%00%02%14%02%06%00%11%04test%06%01%0E%00
array (
  0 => 'test',
  1 => 'test',
)
```

### Примітки

> **Зауваження** :
> 
> Зверніть увагу, що багато вбудованих об'єктів PHP не можуть бути серіалізовані. Однак ті, хто має таку можливість, реалізують або інтерфейс [Serializable](class.serializable.md), або магічні методи [\_\_serialize()](language.oop5.magic.md#object.serialize) [\_\_unserialize()](language.oop5.magic.md#object.unserialize) або [\_\_sleep()](language.oop5.magic.md#object.sleep) [\_\_wakeup()](language.oop5.magic.md#object.wakeup). Якщо внутрішній клас не відповідає жодній із цих вимог, він не може бути надійно серіалізований за допомогою будь-якого серіалізатора.
> 
> Існує кілька історичних винятків із наведеного вище правила, коли деякі внутрішні об'єкти можуть бути серіалізовані без реалізації інтерфейсу або розкриття методів.

### Дивіться також

-   [serialize()](function.serialize.md) \- Генерує придатне для зберігання уявлення змінної
-   [igbinary\_unserialize()](function.igbinary-unserialize.md) \- Створює значення PHP із збереженого уявлення функцією igbinary\_serialize
-   [var\_export()](function.var-export.md) \- Виводить або повертає інтерпретоване рядкове подання змінної
-   [json\_encode()](function.json-encode.md) \- Повертає JSON-подання даних
-   [Серіалізація об'єктів](language.oop5.serialization.md)
-   [\_\_sleep()](language.oop5.magic.md#object.sleep)
-   [\_\_wakeup()](language.oop5.magic.md#object.wakeup)
-   [\_\_serialize()](language.oop5.magic.md#object.serialize)
-   [\_\_unserialize()](language.oop5.magic.md#object.unserialize)
