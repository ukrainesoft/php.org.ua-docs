---
navigation:
  - spoofchecker.construct.md: '« Spoofchecker::\_\_construct'
  - spoofchecker.setallowedlocales.md: 'Spoofchecker::setAllowedLocales »'
  - index.md: PHP Manual
  - class.spoofchecker.md: Spoofchecker
title: 'Spoofchecker::isSuspicious'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Spoofchecker::isSuspicious

(PHP 5 >= 5.4.0, PHP 7, PHP 8, PECL intl >= 2.0.0)

Spoofchecker::isSuspicious — Перевіряє, чи текст містить підозрілі символи

### Опис

```methodsynopsis
public Spoofchecker::isSuspicious(string $string, int &$errorCode = null): bool
```

Перевіряє, чи текст містить підозрілі символи, які візуально ідентичні, але є символами Unicode з іншого мовного набору.

### Список параметрів

`string`

Рядок для перевірки.

`errorCode`

Цей параметр передається за посиланням та заповнюється цілим числом (int), що містить помилку, якщо така є.

### Значення, що повертаються

Повертає **`true`**, якщо містить підозрілі символи та **`false`**, якщо ні.

### Приклади

**Пример #1 Пример использования**Spoofchecker::isSuspicious()\*\*\*\*

```php
<?php
$checker = new Spoofchecker();

$checker->isSuspicious('google.com'); // false: только символы ASCII

$checker->isSuspicious('Рaypal.com'); // true
// Первая буква из кириллического набора, а не обычная латинская "P"
```
