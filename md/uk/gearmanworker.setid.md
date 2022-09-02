---
navigation:
  - gearmanworker.returncode.md: '« GearmanWorker::returnCode'
  - gearmanworker.setoptions.md: 'GearmanWorker::setOptions »'
  - index.md: PHP Manual
  - class.gearmanworker.md: GearmanWorker
title: 'GearmanWorker::setId'
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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **GearmanWorker::setId()****

Завдання ідентифікатора для простого оброблювача.

```php
<?php
$worker= new GearmanWorker();
$worker->setId('test');
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Run the following command:
gearadmin --workers

Output:
30 ::3a3a:3361:3361:3a33%976303667 - : test
```
