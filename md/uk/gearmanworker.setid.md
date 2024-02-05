---
navigation:
  - gearmanworker.returncode.md: '« GearmanWorker::returnCode'
  - gearmanworker.setoptions.md: 'GearmanWorker::setOptions »'
  - index.md: PHP Manual
  - class.gearmanworker.md: GearmanWorker
title: 'GearmanWorker::setId'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanWorker::setId

(No version information available, might only be in Git)

GearmanWorker::setId — Призначає обробнику ідентифікатор, щоб надалі мати можливість опитати всі доступні обробники

### Опис

```methodsynopsis
public GearmanWorker::setId(string $id): bool
```

Призначає обробнику ідентифікатор.

### Список параметрів

`id`

Строковий ідентифікатор.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**GearmanWorker::setId()\*\*\*\*

Завдання ідентифікатора для простого оброблювача.

```php
<?php
$worker= new GearmanWorker();
$worker->setId('test');
?>
```

Висновок наведеного прикладу буде схожим на:

```
Run the following command:
gearadmin --workers

Output:
30 ::3a3a:3361:3361:3a33%976303667 - : test
```
