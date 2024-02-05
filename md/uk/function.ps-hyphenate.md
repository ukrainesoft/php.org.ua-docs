---
navigation:
  - function.ps-get-value.md: « ps\_get\_value
  - function.ps-include-file.md: ps\_include\_file »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_hyphenate
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_hyphenate

(PECL ps >= 1.1.1)

ps\_hyphenate - Переносить слово

### Опис

```methodsynopsis
ps_hyphenate(resource $psdoc, string $text): array|false
```

Переносить це слово. Функція **ps\_hyphenate()** оцінює дефіси значення (встановлюється [ps\_set\_value()](function.ps-set-value.md)) та дефіси параметра (встановлюється [ps\_set\_parameter()](function.ps-set-parameter.md)). Перед викликом цієї функції необхідно встановити дефіс.

Для роботи функції потрібно, щоб категорія мовного стандарту LC\_CTYPE було встановлено коректно. Це робиться при ініціалізації модуля з використанням змінних оточення. У системах Unix для отримання додаткової інформації прочитайте довідкову сторінку мовних стандартів.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.md)

`text`

`text` не повинен містити жодних символів, відмінних від літер. Можливі позиції для переносів повертаються як масиву цілих чисел. Кожне число - це позиція символу в `text`, після якої може бути виконане перенесення.

### Значення, що повертаються

Масив цілих чисел, що вказує на положення можливих переносів у тексті або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Перенесення тексту**

```php
<?php
$word = "Koordinatensystem";
$psdoc = ps_new();
ps_set_parameter($psdoc, "hyphendict", "hyph_de.dic");
$hyphens = ps_hyphenate($psdoc, $word);
for($i=0; $i<strlen($word); $i++) {
  echo $word[$i];
  if(in_array($i, $hyphens))
    echo "-";
}
ps_delete($psdoc);
?>
```

Результат виконання наведеного прикладу:

```
Ko-ordi-na-ten-sys-tem
```

### Дивіться також

-   [ps\_show\_boxed()](function.ps-show-boxed.md) \- Виводить текст у поле
-   locale(1)
