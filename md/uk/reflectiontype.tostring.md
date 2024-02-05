---
navigation:
  - reflectiontype.allowsnull.md: '« ReflectionType::allowsNull'
  - class.reflectionuniontype.md: ReflectionUnionType »
  - index.md: PHP Manual
  - class.reflectiontype.md: ReflectionType
title: 'ReflectionType::\_\_function toString() { \[native code\] }'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionType::\_\_function toString() { \[native code\] }

(PHP 7, PHP 8)

ReflectionType::\_\_toString — Перетворення на рядок

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.1.0. Використовувати цю функцію вкрай не рекомендується.

### Опис

```methodsynopsis
public ReflectionType::__toString(): string
```

Отримує назву типу параметра.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає тип параметра.

### список змін

| Версия | Опис |
| --- | --- |
| 7.1.0 | **ReflectionType::\_\_toString()** оголошено застарілим. |

### Приклади

**Приклад #1 Приклад використання** ReflectionType::\_\_toString()\*\*\*\*

```php
<?php
function someFunction(string $param) {}

$reflectionFunc = new ReflectionFunction('someFunction');
$reflectionParam = $reflectionFunc->getParameters()[0];

echo $reflectionParam->getType();
```

Висновок наведеного прикладу буде схожим на:

```
string
```

### Дивіться також

-   [ReflectionNamedType::getName()](reflectionnamedtype.getname.md) \- Отримує ім'я типу у вигляді рядка
-   [ReflectionNamedType::isBuiltin()](reflectionnamedtype.isbuiltin.md) \- Перевіряє, чи є тип вбудованим
-   [ReflectionType::allowsNull()](reflectiontype.allowsnull.md) \- Перевіряє, чи допустимо NULL
-   [ReflectionUnionType::getTypes()](reflectionuniontype.gettypes.md) \- Повертає типи, включені до типу union
-   [ReflectionParameter::getType()](reflectionparameter.gettype.md) \- Отримати тип параметра
