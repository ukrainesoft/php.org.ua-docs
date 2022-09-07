---
navigation:
  - v8js.resources.md: « Типи ресурсів
  - class.v8js.md: V8Js »
  - index.md: PHP Manual
  - book.v8js.md: V8js
title: Приклади
---
# Приклади

Основи використання

**Приклад #1 Запуск Javascript**

```php
<?php

$v8 = new V8Js();

/* basic.js */
$JS = <<< EOT
len = print('Hello' + ' ' + 'World!' + "\\n");
len;
EOT;

try {
  var_dump($v8->executeString($JS, 'basic.js'));
} catch (V8JsException $e) {
  var_dump($e);
}

?>
```

Результат виконання цього прикладу:

```
Hello World!
int(13)
```
