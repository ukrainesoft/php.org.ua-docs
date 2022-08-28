Надати перевагу вибору словників для мови

-   [« enchant\_broker\_set\_dict\_path](function.enchant-broker-set-dict-path.html)
    
-   [enchant\_dict\_add\_to\_personal »](function.enchant-dict-add-to-personal.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Enchant](ref.enchant.html)
    
-   Надати перевагу вибору словників для мови
    

# enchantbrokersetordering

(PHP 5> = 5.3.0, PHP 7, PHP 8, PECL enchant> = 0.1.0)

enchantbrokersetordering — Виберіть словники для мови.

### Опис

```methodsynopsis
enchant_broker_set_ordering(EnchantBroker $broker, string $tag, string $ordering): bool
```

Задає переваги вибору словників для мови, описаний за допомогою тега 'tag'. Порядок задається за допомогою списку імен провайдерів, розділених комами. В окремих випадках можна використовувати тег "для визначення порядку для всіх мов, для яких цей порядок не задається явно.

### Список параметрів

`broker`

Провайдер Enchant, який повертається [enchant\_broker\_init()](function.enchant-broker-init.html)

`tag`

Мовний тег. В окремих випадках можна використовувати тег "для визначення порядку для всіх мов, для яких цей порядок не задається явно.

`ordering`

Список імен провайдерів, розділених комами

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                  |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------|
|        | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.html); Раніше очікувався ресурс ([resource](language.types.resource.html) |