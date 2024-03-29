---
navigation:
  - transliterator.listids.md: '« Transliterator::listIDs'
  - class.intlbreakiterator.md: IntlBreakIterator »
  - index.md: PHP Manual
  - class.transliterator.md: Transliterator
title: 'Transliterator::transliterate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Transliterator::transliterate

# transliterator\_transliterate

(PHP 5 >= 5.4.0, PHP 7, PHP 8, PECL intl >= 2.0.0)

Transliterator::transliterate -- transliterator\_transliterate — Транслітерувати рядок

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public Transliterator::transliterate(string $string, int $start = 0, int $end = -1): string|false
```

Процедурний стиль

```methodsynopsis
transliterator_transliterate(    Transliterator|string $transliterator,    string $string,    int $start = 0,    int $end = -1): string|false
```

Перетворює рядок або його частину за допомогою транслітератора ICU.

### Список параметрів

`transliterator`

У процедурному варіанті, [Transliterator](class.transliterator.md) або рядок, з якого може бути зібраний об'єкт [Transliterator](class.transliterator.md)

`string`

Рядок для транслітерації.

`start`

Початковий індекс, включно (у кодових одиницях UTF-16), з якого починається частина рядка, призначена для транслітерації. Індексація починається з 0. Текст до цієї позиції залишиться як є.

`end`

Початковий індекс, не включаючи (у кодових одиницях UTF-16), яким закінчується частина рядка, призначена для транслітерації. Індексація починається з 0. Текст із цієї позиції залишиться як є.

### Значення, що повертаються

Повертає перетворений рядок у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Конвертація екранованого UTF-16 рядка**

```php
<?php
$s = "\u304A\u65E9\u3046\u3054\u3056\u3044\u307E\u3059";
echo transliterator_transliterate("Hex-Any/Java", $s), "\n";

//теперь обратная операция с дополнительным символом
$supplChar = html_entity_decode('&#x1D11E;');
echo mb_strlen($supplChar, "UTF-8"), "\n";
$encSupplChar = transliterator_transliterate("Any-Hex/Java", $supplChar);
//вывод двух кодированных UTF-16 символов
echo $encSupplChar, "\n";
//и назад
echo transliterator_transliterate("Hex-Any/Java", $encSupplChar), "\n";
?>
```

Висновок наведеного прикладу буде схожим на:

```
お早うございます
1
\uD834\uDD1E
𝄞
```

### Дивіться також

-   [Transliterator::getErrorMessage()](transliterator.geterrormessage.md) \- Отримати останнє повідомлення про помилку
-   [Transliterator::\_\_construct()](transliterator.construct.md) \- Приватний конструктор
