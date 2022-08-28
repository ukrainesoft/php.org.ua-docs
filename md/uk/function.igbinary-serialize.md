Створює компактне, двійкове уявлення, що зберігається.

-   [« Функции Igbinary](ref.igbinary.html)
    
-   [igbinary\_unserialize »](function.igbinary-unserialize.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Igbinary](ref.igbinary.html)
    
-   Створює компактне, двійкове уявлення, що зберігається.
    

# igbinaryserialize

(PECL igbinary >= 1.1.1)

igbinaryserialize — Створює компактне, двійкове уявлення, що зберігається.

### Опис

```methodsynopsis
igbinary_serialize(mixed $value): string|false
```

Створює значення, що зберігається.

Корисно для зберігання або передачі значень PHP без втрати їх типу та структури.

Щоб знову перетворити серіалізований рядок на значення PHP, можна використовувати [igbinary\_unserialize()](function.igbinary-unserialize.html)

### Список параметрів

`value`

Значення, яке потрібно серіалізувати . **igbinaryserialize()** обробляє всі типи, крім ресурсів (resource) та деяких об'єктів (object) (див. примітку нижче). Навіть масиви (array), що містять посилання на себе, можуть бути серіалізовані функцією **igbinaryserialize()**. Циклічні посилання всередині масивів (array) або об'єктів (object), що серіалізуються, також будуть збережені. Будь-яке інше посилання буде втрачено.

При серіалізації об'єктів, igbinary намагатиметься викликати функції [\_\_serialize()](language.oop5.magic.html#object.serialize) або [\_\_sleep()](language.oop5.magic.html#object.sleep) перед серіалізацією. Це дозволить об'єкту виконати будь-яку очистку в останню хвилину тощо. перед серіалізацією. Аналогічно, коли об'єкт відновлюється за допомогою [igbinary\_unserialize()](function.igbinary-unserialize.html), викликається функція [\_\_unserialize()](language.oop5.magic.html#object.unserialize) або [\_\_wakeup()](language.oop5.magic.html#object.wakeup)

> **Зауваження**
> 
> Початок імен закритих членів об'єкта (object) доповнюються ім'ям класу, а початок імен захищених членів символом `'*'`. Ці доповнені значення оточуються нульовим байтом з обох боків.

### Значення, що повертаються

Повертає рядок, що містить уявлення потоку байтів `value`, яке може бути збережене будь-де.

Зверніть увагу, що це двійковий рядок, який може включати будь-яке байтове значення і повинен зберігатися і оброблятися як такий. Наприклад, виведення функції **igbinaryserialize()** зазвичай повинен зберігатися у полі бази даних `BLOB`, а не в полі `CHAR` або `TEXT`

### Приклади

**Приклад #1 Приклад використання **igbinaryserialize()****

```php
<?php
$ser = igbinary_serialize(['test', 'test']);
echo urlencode($ser), "\n";
var_export(igbinary_unserialize($ser));
?>
```

Результат виконання цього прикладу:

```
%00%00%00%02%14%02%06%00%11%04test%06%01%0E%00
array (
  0 => 'test',
  1 => 'test',
)
```

### Примітки

> **Зауваження**
> 
> Зверніть увагу, що багато вбудованих об'єктів PHP не можуть бути серіалізовані. Однак ті, хто має таку можливість, реалізують або інтерфейс [Serializable](class.serializable.html), або магічні методи [\_\_serialize()](language.oop5.magic.html#object.serialize)[\_\_unserialize()](language.oop5.magic.html#object.unserialize) або [\_\_sleep()](language.oop5.magic.html#object.sleep)[\_\_wakeup()](language.oop5.magic.html#object.wakeup). Якщо внутрішній клас не відповідає жодній із цих вимог, він не може бути надійно серіалізований за допомогою будь-якого серіалізатора.
> 
> Існує кілька історичних винятків із наведеного вище правила, коли деякі внутрішні об'єкти можуть бути серіалізовані без реалізації інтерфейсу або розкриття методів.

### Дивіться також

-   [serialize()](function.serialize.html) - Генерує придатне для зберігання подання змінної
-   [igbinary\_unserialize()](function.igbinary-unserialize.html) - Створює значення PHP із збереженого уявлення функцією igbinaryserialize
-   [var\_export()](function.var-export.html) - Виводить або повертає інтерпретоване рядкове подання змінної
-   [json\_encode()](function.json-encode.html) - Повертає JSON-подання даних
-   [Сериализация объектов](language.oop5.serialization.html)
-   [\_\_sleep()](language.oop5.magic.html#object.sleep)
-   [\_\_wakeup()](language.oop5.magic.html#object.wakeup)
-   [\_\_serialize()](language.oop5.magic.html#object.serialize)
-   [\_\_unserialize()](language.oop5.magic.html#object.unserialize)