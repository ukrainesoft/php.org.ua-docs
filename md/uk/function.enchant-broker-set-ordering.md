---
navigation:
  - function.enchant-broker-set-dict-path.html: « enchantbrokersetdictpath
  - function.enchant-dict-add-to-personal.html: enchantdictaddтоpersonal »
  - index.md: PHP Manual
  - ref.enchant.md: Функции Enchant
title: enchantbrokersetordering
---
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

Провайдер Enchant, який повертається [enchantbrokerinit()](function.enchant-broker-init.html)

`tag`

Мовний тег. В окремих випадках можна використовувати тег "для визначення порядку для всіх мов, для яких цей порядок не задається явно.

`ordering`

Список імен провайдерів, розділених комами

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `broker` чекає на екземпляр [EnchantBroker](class.enchantbroker.md); Раніше очікувався ресурс ([resource](language.types.resource.md) |
