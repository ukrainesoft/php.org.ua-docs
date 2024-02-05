---
navigation:
  - function.interface-exists.md: « interface\_exists
  - function.is-subclass-of.md: is\_subclass\_of »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: is\_a
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# is\_a

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

is\_a — Перевіряє, чи об'єкт належить до типу або підтипу.

### Опис

```methodsynopsis
is_a(mixed $object_or_class, string $class, bool $allow_string = false): bool
```

Визначає, чи належить об'єкт чи клас `object_or_class` безпосередньо до типу об'єкта `class`, або тип об'єкта `class` - Супертип об'єкта або класу, що перевіряється.

### Список параметрів

`object_or_class`

Назва класу або екземпляр об'єкта.

`class`

Ім'я класу чи інтерфейсу.

`allow_string`

Если для параметра установлено значение\*\*`false`\*\*, то функція визначить приналежність типу об'єкта, що перевіряється до типу або підтипу класу, тільки якщо в параметр `object_or_class` буде передано екземпляр об'єкта, а не ім'я класу. Це також запобігає виклику автозавантажувача, якщо клас не знайдено.

### Значення, що повертаються

Повертає **`true`**, якщо об'єкт `object_or_class` належить до типу об'єкта `class` або тип об'єкта `class` - Супертип об'єкта, що перевіряється, інакше **`false`**

### Приклади

**Приклад #1 Приклад использования функции**is\_a()\*\*\*\*

```php
<?php

// Объявить класс
class WidgetFactory
{
  var $oink = 'moo';
}

// Создать новый объект
$WF = new WidgetFactory();

if (is_a($WF, 'WidgetFactory')) {
  echo "Да, \$WF всё ещё WidgetFactory\n";
}

?>
```

**Приклад #2 Использование оператора*instanceof***

```php
<?php

if ($WF instanceof WidgetFactory) {
    echo 'Да, $WF — WidgetFactory';
}

?>
```

### Дивіться також

-   [get\_class()](function.get-class.md) \- Повертає ім'я класу, до якого належить об'єкт
-   [get\_parent\_class()](function.get-parent-class.md) \- Повертає ім'я батьківського класу для об'єкта чи класу
-   [is\_subclass\_of()](function.is-subclass-of.md) \- Перевіряє, чи містить об'єкт у своєму дереві предків зазначений клас чи прямо реалізує його
