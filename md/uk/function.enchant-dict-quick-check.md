---
navigation:
  - function.enchant-dict-is-in-session.html: « enchantdictісінsession
  - function.enchant-dict-store-replacement.html: enchantdictstorereplacement »
  - index.md: PHP Manual
  - ref.enchant.md: Функции Enchant
title: enchantdictquickcheck
---
# enchantdictquickcheck

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL enchant:0.2.0-1.0.1)

enchantdictquickcheck — Перевірити, чи правильно написано слово та запропонувати варіанти заміни

### Опис

```methodsynopsis
enchant_dict_quick_check(EnchantDictionary $dictionary, string $word, array &$suggestions = null): bool
```

Якщо слово коректне, то поверне **`true`**, в іншому випадку поверне **`false`**. Якщо заданий параметр suggestions, він буде заповнений варіантами заміни.

### Список параметрів

`dictionary`

Словник Enchant, що повертається [enchantbrokerrequestdict()](function.enchant-broker-request-dict.html) або [enchantbrokerrequestpwldict()](function.enchant-broker-request-pwl-dict.md)

`word`

Слово для перевірки

`suggestions`

Якщо перевірка провалилася, то ця змінна міститиме масив із варіантами заміни.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо слово написано правильно або **`false`**, якщо ні

### список змін

| Версия | Описание |
| --- | --- |
|  | `dictionary` чекає на екземпляр [EnchantDictionary](class.enchantdictionary.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **enchantdictquickcheck()****

```php
<?php
$tag = 'en_US';
$r = enchant_broker_init();

if (enchant_broker_dict_exists($r,$tag)) {
    $d = enchant_broker_request_dict($r, $tag);
    enchant_dict_quick_check($d, 'soong', $suggs);
    print_r($suggs);
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] => song
    [1] => snog
    [2] => soon
    [3] => Sang
    [4] => Sung
    [5] => sang
    [6] => sung
    [7] => sponge
    [8] => spongy
    [9] => snag
    [10] => snug
    [11] => sonic
    [12] => sing
    [13] => songs
    [14] => Son
    [15] => Sonja
    [16] => Synge
    [17] => son
    [18] => Sejong
    [19] => sarong
    [20] => sooner
    [21] => Sony
    [22] => sown
    [23] => scone
    [24] => song's
)
```

### Дивіться також

-   [enchantdictcheck()](function.enchant-dict-check.md) - Перевіряє, чи правильно задано слово
-   [enchantdictsuggest()](function.enchant-dict-suggest.md) - Поверне список можливих варіантів для слова з помилкою
