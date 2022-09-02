---
navigation:
  - eventconfig.construct.md: '« EventConfig::construct'
  - eventconfig.setflags.md: 'EventConfig::setFlags »'
  - index.md: PHP Manual
  - class.eventconfig.md: EventConfig
title: 'EventConfig::requireFeatures'
---
# EventConfig::requireFeatures

(PECL event >= 1.2.6-beta)

EventConfig::requireFeatures — Ввести необхідні додатки властивості методу події

### Опис

```methodsynopsis
public
   EventConfig::requireFeatures(
    int
     $feature
   ): bool
```

Вводить необхідну програму функціональність методу події

### Список параметрів

`feature`

Бітова маска потрібних властивостей. Дивіться [константи`EventConfig::FEATURE_*`](class.eventconfig.md#eventconfig.constants)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **EventConfig::requireFeatures()****

```php
<?php
$cfg = new EventConfig();

// Создаём event_base, связанный с конфигом $cfg
$base = new EventBase($cfg);

// Запрашиваем свойство FDS
if ($cfg->requireFeatures(EventConfig::FEATURE_FDS)) {
    echo "Свойство FDS запрошено\n";

    $base = new EventBase($cfg);
    ($base->getFeatures() & EventConfig::FEATURE_FDS)
        and print("FDS - произвольные типы дескрипторов файлов, а не только сокеты\n");
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Свойство FDS запрошено
FDS - произвольные типы дескрипторов файлов, а не только сокеты
```

### Дивіться також

-   [EventBase::getFeatures()](eventbase.getfeatures.md) - Повертає бітову маску підтримуваних функцій
