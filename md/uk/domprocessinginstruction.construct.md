---
navigation:
  - class.domprocessinginstruction.md: « DOMProcessingInstruction
  - class.domtext.md: DOMText »
  - index.md: PHP Manual
  - class.domprocessinginstruction.md: DOMProcessingInstruction
title: 'DOMProcessingInstruction::construct'
---
# DOMProcessingInstruction::construct

(PHP 5, PHP 7, PHP 8)

DOMProcessingInstruction::construct — Створює новий об'єкт класу [DOMProcessingInstruction](class.domprocessinginstruction.md)

### Опис

public **DOMProcessingInstruction::construct**(string `$name`, string `$value` = "")

Створює новий об'єкт класу [DOMProcessingInstruction](class.domprocessinginstruction.md). Цей об'єкт буде доступний лише для читання. Він може бути доданий до документа. Додаткові вузли не можна прикріпити до цього об'єкта, доки він приєднаний до будь-якого документа. Для створення вузла, що модифікується, використовуйте [DOMDocument::createProcessingInstruction](domdocument.createprocessinginstruction.md)

### Список параметрів

`name`

Ім'я інструкції для оброблювача.

`value`

Значення інструкції для оброблювача.

### Приклади

**Приклад #1 Створення класу [DOMProcessingInstruction](class.domprocessinginstruction.md)**

```php
<?php

$dom = new DOMDocument('1.0', 'UTF-8');
$html = $dom->appendChild(new DOMElement('html'));
$body = $html->appendChild(new DOMElement('body'));
$pinode = new DOMProcessingInstruction('php', 'echo "Hello World"; ');
$body->appendChild($pinode);
echo $dom->saveXML();

?>
```

Результат виконання цього прикладу:

```
<?xml version="1.0" encoding="UTF-8"?>
<html><body><?php echo "Hello World"; ?></body></html>
```

### Дивіться також

-   [DOMDocument::createProcessingInstruction()](domdocument.createprocessinginstruction.md) - Створити новий PI-вузол
