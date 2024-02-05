---
navigation:
  - function.enchant-broker-set-dict-path.md: « enchant\_broker\_set\_dict\_path
  - function.enchant-dict-add-to-personal.md: enchant\_dict\_add\_to\_personal »
  - index.md: PHP Manual
  - ref.enchant.md: Функції Enchant
title: enchant\_broker\_set\_ordering
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# enchant\_broker\_set\_ordering

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL enchant >= 0.1.0 )

enchant\_broker\_set\_ordering — Виберіть словники для мови.

### Опис

```methodsynopsis
enchant_broker_set_ordering(EnchantBroker $broker, string $tag, string $ordering): bool
```

Задає переваги вибору словників для мови, описаний за допомогою тега 'tag'. Порядок задається за допомогою списку імен провайдерів, розділених комами. В окремих випадках можна використовувати тег "\*для визначення порядку для всіх мов, для яких цей порядок не задається явно.

### Список параметрів

`broker`

Провайдер Enchant, який повертається [enchant\_broker\_init()](function.enchant-broker-init.md)

`tag`

Мовний тег. В окремих випадках можна використовувати тег "\*для визначення порядку для всіх мов, для яких цей порядок не задається явно.

`ordering`

Список імен провайдерів, розділених комами

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |
