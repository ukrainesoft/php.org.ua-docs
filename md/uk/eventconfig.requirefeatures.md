---
navigation:
  - eventconfig.construct.md: '« EventConfig::\_\_construct'
  - eventconfig.setflags.md: 'EventConfig::setFlags »'
  - index.md: PHP Manual
  - class.eventconfig.md: EventConfig
title: 'EventConfig::requireFeatures'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Бітова маска потрібних властивостей. Дивіться [константи `EventConfig::FEATURE_*`](class.eventconfig.md#eventconfig.constants)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** EventConfig::requireFeatures()\*\*\*\*

```php
<?php
$cfg = new EventConfig();

// Создаём event_base, связанный с конфигом $cfg
$base = new EventBase($cfg);

// Запрашиваем свойство FDS
if ($cfg->requireFeatures(EventConfig::FEATURE_FDS)) {
    echo "Свойство FDS запрошено\n";

    $base = new EventBase($cfg);
    ($base->getFeatures() & EventConfig::FEATURE_FDS)
        and print "FDS — произвольные типы дескрипторов файлов, а не только сокеты\n";
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Свойство FDS запрошено
FDS - произвольные типы дескрипторов файлов, а не только сокеты
```

### Дивіться також

-   [EventBase::getFeatures()](eventbase.getfeatures.md) \- Повертає бітову маску підтримуваних функцій
