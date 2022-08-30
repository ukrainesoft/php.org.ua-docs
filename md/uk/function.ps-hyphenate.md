Переносить слово

-   [«psgetvalue](function.ps-get-value.html)
    
-   [псincludefile »](function.ps-include-file.html)
    
-   [PHP Manual](index.html)
    
-   [Функції PS](ref.ps.html)
    
-   Переносить слово
    

# псhyphenate

(PECL ps >= 1.1.1)

псhyphenate - Переносить слово

### Опис

```methodsynopsis
ps_hyphenate(resource $psdoc, string $text): array|false
```

Переносить це слово. Функція **псhyphenate()** оцінює дефіси значення (встановлюється [псsetvalue()](function.ps-set-value.html)) та дефіси параметра (встановлюється [псsetparameter()](function.ps-set-parameter.html)). Перед викликом цієї функції необхідно встановити дефіс.

Для роботи функції потрібно, щоб категорія мовного стандарту LCCTYPE було встановлено коректно. Це робиться при ініціалізації модуля з використанням змінних оточення. У системах Unix для додаткової інформації прочитайте довідкову сторінку мовних стандартів.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [псnew()](function.ps-new.html)

`text`

`text` не повинен містити жодних символів, відмінних від літер. Можливі позиції для переносів повертаються як масиву цілих чисел. Кожне число - це позиція символу в `text`, після якої може бути виконане перенесення.

### Значення, що повертаються

Масив цілих чисел, що вказує на положення можливих переносів у тексті або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Перенесення тексту**

```php
<?php
$word = "Koordinatensystem";
$psdoc = ps_new();
ps_set_parameter($psdoc, "hyphendict", "hyph_de.dic");
$hyphens = ps_hyphenate($psdoc, $word);
for($i=0; $i<strlen($word); $i++) {
  echo $word[$i];
  if(in_array($i, $hyphens))
    echo "-";
}
ps_delete($psdoc);
?>
```

Результат виконання цього прикладу:

```
Ko-ordi-na-ten-sys-tem
```

### Дивіться також

-   [псshowboxed()](function.ps-show-boxed.html) - Виводить текст у поле
-   locale(1)