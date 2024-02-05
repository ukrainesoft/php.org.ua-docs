---
navigation:
  - transliterator.geterrormessage.md: '« Transliterator::getErrorMessage'
  - transliterator.transliterate.md: 'Transliterator::transliterate »'
  - index.md: PHP Manual
  - class.transliterator.md: Transliterator
title: 'Transliterator::listIDs'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Transliterator::listIDs

# transliterator\_list\_ids

(PHP 5 >= 5.4.0, PHP 7, PHP 8, PECL intl >= 2.0.0)

Transliterator::listIDs -- transliterator\_list\_ids — Отримати ідентифікатори транслітератора

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Transliterator::listIDs(): array|false
```

Процедурний стиль

```methodsynopsis
transliterator_list_ids(): array|false
```

Повертає масив зареєстрованих ідентифікаторів транслітератора.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив (array) зареєстрованих ідентифікаторів транслітератора або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Отримання зареєстрованих ідентифікаторів транслітератора**

```php
<?php
print_r(Transliterator::listIDs());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => ASCII-Latin
    [1] => Accents-Any
    [2] => Amharic-Latin/BGN
    [3] => Any-Accents
    [4] => Any-Publishing
...
    [650] => Any-ps_Latn/BGN
    [651] => Any-tk/BGN
    [652] => Any-ch_FONIPA
    [653] => Any-cs_FONIPA
    [654] => Any-cy_FONIPA
)
```

### Дивіться також

-   [Transliterator::getErrorMessage()](transliterator.geterrormessage.md) \- Отримати останнє повідомлення про помилку
-   [Transliterator::transliterate()](transliterator.transliterate.md) \- Транслітерувати рядок
