---
navigation:
  - function.mdspecialchars-decode.md: « htmlspecialchars\_decode
  - function.implode.md: implode »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: htmlspecialchars
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# htmlspecialchars

(PHP 4, PHP 5, PHP 7, PHP 8)

htmlspecialchars - Перетворює спеціальні символи в HTML-сутності

### Опис

```methodsynopsis
htmlspecialchars(    string $string,    int $flags = ENT_QUOTES | ENT_SUBSTITUTE | ENT_HTML401,    ?string $encoding = null,    bool $double_encode = true): string
```

У HTML деякі символи мають особливий зміст і мають бути представлені у вигляді HTML-сутностей, щоб зберегти їх значення. Ця функція повертає рядок, над яким проведено ці перетворення. Якщо вам потрібно перетворити всі можливі сутності, використовуйте [htmlentities()](function.mdentities.md)

Якщо вхідний рядок, переданий у цю функцію та результуючий документ, використовують однакове кодування символів, то цієї функції достатньо, щоб підготувати дані для вставки в більшість частин HTML-документа. Однак, якщо дані містять символи, не визначені в кодуванні символів результуючого документа і ви очікуєте збереження цих символів (як числові або іменовані сутності), то вам буде недостатньо цієї і [htmlentities()](function.mdentities.md) функцій (які лише перетворюють підрядки з відповідними сутностями). Необхідно використовувати функцію [mb\_encode\_numericentity()](function.mb-encode-numericentity.md)

**Виробляються такі перетворення**

| Символ | Замена |
| --- | --- |
| `&` (амперсанд) | `&amp;` |
| `"` (подвійні лапки) | `&quot;`, якщо не встановлено **`ENT_NOQUOTES`** |
| `'` (одинарні лапки) | `&#039;`(для\*\*`ENT_HTML401`**) или`&apos;`(для**`ENT_XML1`\*\* **`ENT_XHTML`**или**`ENT_HTML5`**), але тільки якщо встановлена **`ENT_QUOTES`** |
| `<` (менше) | `&lt;` |
| `>` (більше) | `&gt;` |

### Список параметрів

`string`

Конвертований рядок (string).

`flags`

Бітова маска з вказаних нижче прапорів, що визначають режим обробки лапок, некоректних кодових послідовностей і тип документа, що використовується. За замовчуванням використовується `ENT_QUOTES | ENT_SUBSTITUTE | ENT_HTML401`

**Доступні значення параметра `flags`**

| Название константы | Опис |
| --- | --- |
| **`ENT_COMPAT`** | Перетворює подвійні лапки, одинарні лапки не змінюються. |
| **`ENT_QUOTES`** | Перетворює як подвійні, і одинарні лапки. |
| **`ENT_NOQUOTES`** | Залишає без зміни як подвійні, так і одинарні лапки. |
| **`ENT_IGNORE`** | Без будь-яких повідомлень відкидає некоректні кодові послідовності замість повернення порожнього рядка. Використання цього прапора не рекомендується, оскільки це може призвести до [» негативних наслідків, пов'язаних з безпекою](http://unicode.org/reports/tr36/#Deletion_of_Noncharacters) |
| **`ENT_SUBSTITUTE`** | Замінює некоректні кодові послідовності символом заміни Юнікоду U+FFFD у разі використання UTF-8 або при використанні іншого кодування, замість повернення порожнього рядка. |
| **`ENT_DISALLOWED`** | Замінює неправильні коди символів для заданого типу документа символом заміни юнікоду U+FFFD (UTF-8) або (при використанні іншого кодування) замість того, щоб залишати все як є. Це може бути корисним, наприклад, для того, щоб переконатися у формальній правильності XML-документів із вбудованим зовнішнім контентом. |
| **`ENT_HTML401`** | Обробка коду відповідно до HTML 4.01. |
| **`ENT_XML1`** | Обробка коду відповідно до XML 1. |
| **`ENT_XHTML`** | Обробка коду відповідно до XHTML. |
| **`ENT_HTML5`** | Обробка коду відповідно до HTML 5. |

`encoding`

Необов'язковий аргумент, що визначає кодування, яке використовується при конвертації символів.

Если не указан, то значение по умолчанию для`encoding` залежить від конфігураційної опції [default\_charset](ini.core.md#ini.default-charset)

Хоча цей аргумент є технічно необов'язковим, рекомендується вказати правильне значення для вашого коду, опція конфігурації [default\_charset](ini.core.md#ini.default-charset) може бути задана неправильно для вхідних даних.

Для цілей цієї функції кодування `ISO-8859-1` `ISO-8859-15` `UTF-8` `cp866` `cp1251` `cp1252`и`KOI8-R` є практично еквівалентними, припускаючи те, що сам рядок `string` містить коректні символи у зазначеному кодуванні, то символи, що змінюються **htmlspecialchars()**, залишаться на тих же місцях у всіх цих кодуваннях.

Підтримуються такі кодування:

**Підтримувані кодування**

| Кодировка | Псевдонимы | Опис |
| --- | --- | --- |
| ISO-8859-1 | ISO8859-1 | Західноєвропейська Latin-1. |
| ISO-8859-5 | ISO8859-5 | Рідко використовуване кириличне кодування (Latin/Cyrillic). |
| ISO-8859-15 | ISO8859-15 | Західноєвропейська Latin-9. Додає символ євро, французькі та фінські літери до кодування Latin-1 (ISO-8859-1). |
| UTF-8 |  | 8-бітна Unicode, сумісна з ASCII. |
| cp866 | ibm866, 866 | Кирилічна кодування, що застосовується в DOS. |
| cp1251 | Windows-1251, win-1251, 1251 | Кирилічна кодування, що використовується у Windows. |
| cp1252 | Windows-1252, 1252 | Західно-європейське кодування, що використовується у Windows. |
| KOI8-R | koi8-ru, koi8r | Російське кодування. |
| BIG5 | 950 | Традиційний китайський, застосовується переважно на Тайвані. |
| GB2312 | 936 | Спрощена китайська, стандартне національне кодування. |
| BIG5-HKSCS |  | Розширена Big5, що застосовується в Гонконгу. |
| Shift\_JIS | SJIS, SJIS-win, cp932, 932 | Японське кодування. |
| EUC-JP | EUCJP, eucJP-win | Японське кодування. |
| MacRoman |  | Кодування, яке використовується в Mac OS. |
| `''` |  | Порожній рядок активує режим визначення кодування із файлу скрипта (Zend multibyte), [default\_charset](ini.core.md#ini.default-charset) та поточної локалі (дивіться [nl\_langinfo()](function.nl-langinfo.md) і [setlocale()](function.setlocale.md)) у зазначеному порядку. Не рекомендується використовувати. |

> **Зауваження**: Інші кодування не підтримуються, замість них буде застосовано кодування за замовчуванням та згенеровано попередження.

`double_encode`

Якщо параметр `double_encode` вимкнений, то PHP не перетворюватиме існуючі html-сутності. За замовчуванням все перетворюється без обмежень.

### Значення, що повертаються

Перетворений рядок (string).

Якщо вхідний рядок `string` містить неправильну послідовність символів у зазначеному кодуванні `encoding`, то повертатиметься порожній рядок у випадку, якщо прапори **`ENT_IGNORE`**или**`ENT_SUBSTITUTE`** не встановлені.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Значення за промовчанням `flags` змінено з **`ENT_COMPAT`**на**`ENT_QUOTES`** |

### Приклади

**Пример #1 Пример использования**htmlspecialchars()\*\*\*\*

```php
<?php
$new = htmlspecialchars("<a href='test'>Test</a>", ENT_QUOTES);
echo $new; // &lt;a href=&#039;test&#039;&gt;Test&lt;/a&gt;
?>
```

### Примітки

> **Зауваження** :
> 
> Зверніть увагу, що функція не робить інших перетворень, крім описаних вище. Для перетворення всіх HTML-сутностей використовуйте [htmlentities()](function.mdentities.md)

> **Зауваження** :
> 
> У разі неоднозначного значення `flags`, застосовуються такі правила:
> 
> -   Якщо одночасно відсутні константи\*\*`ENT_COMPAT`\*\* **`ENT_QUOTES`**и**`ENT_NOQUOTES`**, за умовчанням буде використовуватися\*\*`ENT_NOQUOTES`\*\*
> -   Якщо одночасно присутні дві або більше констант\*\*`ENT_COMPAT`\*\* **`ENT_QUOTES`**и**`ENT_NOQUOTES`** **`ENT_QUOTES`**матиме більший пріоритет. Наступна за пріоритетом буде**`ENT_COMPAT`**
> -   Якщо немає жодної з констант\*\*`ENT_HTML401`\*\* **`ENT_HTML5`** **`ENT_XHTML`**и**`ENT_XML1`**, за умовчанням буде використовуватися\*\*`ENT_HTML401`\*\*
> -   Якщо одночасно присутні дві або більше констант\*\*`ENT_HTML401`\*\* **`ENT_HTML5`** **`ENT_XHTML`** **`ENT_XML1`**, то пріоритет буде таким:**`ENT_HTML5`**, потім\*\*`ENT_XHTML`\*\* **`ENT_XML1`**, а потім\*\*`ENT_HTML401`\*\*
> -   Якщо одночасно присутні дві або більше констант\*\*`ENT_DISALLOWED`\*\* **`ENT_IGNORE`** **`ENT_SUBSTITUTE`**, найвищий пріоритет буде мати\*\*`ENT_IGNORE`**, а наступна за нею**`ENT_SUBSTITUTE`\*\*

### Дивіться також

-   [get\_html\_translation\_table()](function.get-html-translation-table.md) \- Повертає таблицю перетворень, використовувану функціями htmlspecialchars і htmlentities
-   [htmlspecialchars\_decode()](function.mdspecialchars-decode.md) \- Перетворює спеціальні HTML-сутності назад на символи
-   [strip\_tags()](function.strip-tags.md) \- Видаляє теги HTML та PHP з рядка
-   [htmlentities()](function.mdentities.md) \- Перетворює всі можливі символи у відповідні HTML-сутності
-   [nl2br()](function.nl2br.md) \- Вставляє HTML код розриву рядка перед кожним перекладом рядка