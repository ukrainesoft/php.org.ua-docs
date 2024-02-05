---
navigation:
  - closure.construct.md: '« Closure::\_\_construct'
  - closure.bindto.md: 'Closure::bindTo »'
  - index.md: PHP Manual
  - class.closure.md: Closure
title: 'Closure::bind'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Closure::bind

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

Closure::bind — Дублює замикання із зазначенням конкретного зв'язаного об'єкта та області видимості класу

### Опис

```methodsynopsis
public static Closure::bind(Closure $closure, ?object $newThis, object|string|null $newScope = "static"): ?Closure
```

Цей метод є статичним варіантом [Closure::bindTo()](closure.bindto.md)Смотрите документацию к указанному методу для подробной информации.

### Список параметрів

`closure`

Анонімна функція для прив'язування об'єкту.

`newThis`

Об'єкт, до якого буде прив'язана передана анонімна функція, або **`null`** для від'єднання функції від поточного об'єкта.

`newScope`

Область видимості класу, з якою має бути пов'язане замикання, або 'static' збереження поточної області видимості. Якщо передано об'єкт, то буде використано його клас. Цей параметр визначає видимість protected (захищених) та private (закритих) методів прив'язаного об'єкта. Заборонено як цей параметр передавати (об'єктом) внутрішній клас.

### Значення, що повертаються

Повертає новий об'єкт [Closure](class.closure.md)или\*\*`null`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад**Closure::bind()\*\*\*\*

```php
<?php
class A {
    private static $sfoo = 1;
    private $ifoo = 2;
}
$cl1 = static function() {
    return A::$sfoo;
};
$cl2 = function() {
    return $this->ifoo;
};

$bcl1 = Closure::bind($cl1, null, 'A');
$bcl2 = Closure::bind($cl2, new A(), 'A');
echo $bcl1(), "\n";
echo $bcl2(), "\n";
?>
```

Висновок наведеного прикладу буде схожим на:

```
1
2
```

### Дивіться також

-   [Анонімні функції](functions.anonymous.md)
-   [Closure::bindTo()](closure.bindto.md) \- Дублює замикання із зазначенням пов'язаного об'єкта та області видимості класу
