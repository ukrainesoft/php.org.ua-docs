Додати слово у поточну сесію перевірки

-   [« enchant\_dict\_add\_to\_personal](function.enchant-dict-add-to-personal.html)
    
-   [enchant\_dict\_add »](function.enchant-dict-add.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Enchant](ref.enchant.html)
    
-   Додати слово у поточну сесію перевірки
    

# enchantdictaddтоsession

(PHP 5> = 5.3.0, PHP 7, PHP 8, PECL enchant> = 0.1.0)

enchantdictaddтоsession — Додати слово до поточної сесії перевірки

### Опис

```methodsynopsis
enchant_dict_add_to_session(EnchantDictionary $dictionary, string $word): void
```

Додає слово до заданого словника. Слово буде присутнє тільки в поточній сесії перевірки.

### Список параметрів

`dictionary`

Словник Enchant, що повертається [enchant\_broker\_request\_dict()](function.enchant-broker-request-dict.html) або [enchant\_broker\_request\_pwl\_dict()](function.enchant-broker-request-pwl-dict.html)

`word`

Слово для додавання

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Описание |
| --- | --- |
|  | `dictionary` чекає на екземпляр [EnchantDictionary](class.enchantdictionary.html); Раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [enchant\_broker\_request\_dict()](function.enchant-broker-request-dict.html) - Створити новий словник, використовуючи тег