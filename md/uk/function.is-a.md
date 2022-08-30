Перевіряє, чи належить об'єкт до цього класу чи чи є цей клас одним із його батьків

-   [« interfaceexists](function.interface-exists.html)
    
-   [ісsubclassof »](function.is-subclass-of.html)
    
-   [PHP Manual](index.html)
    
-   [Функції роботи з класами та об'єктами](ref.classobj.html)
    
-   Перевіряє, чи належить об'єкт до цього класу чи чи є цей клас одним із його батьків
    

# іса

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

ісa — Перевіряє, чи належить об'єкт до цього класу чи чи є цей клас одним із його батьків

### Опис

```methodsynopsis
is_a(mixed $object_or_class, string $class, bool $allow_string = false): bool
```

Перевіряє, чи об'єкт належить `object_or_class` до цього класу чи є цей клас одним із його батьків.

### Список параметрів

`object_or_class`

Ім'я класу чи об'єкт

`class`

Ім'я класу

`allow_string`

Якщо параметр встановлений у **`false`**, то не допускається ім'я класу у вигляді рядка як параметр `object_or_class`. Це також запобігає виклику автозавантажувача, якщо клас не існує.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо об'єкт належить даному класу або чи є цей клас одним з його батьків, інакше повертається **`false`**

### Приклади

**Приклад #1 Приклад використання **ісa()****

```php
<?php
// объявление класса
class WidgetFactory
{
  var $oink = 'moo';
}

// создание нового объекта
$WF = new WidgetFactory();

if (is_a($WF, 'WidgetFactory')) {
  echo "да, \$WF всё ещё WidgetFactory\n";
}
?>
```

**Приклад #2 Використання оператора *instanceof***

```php
<?php
if ($WF instanceof WidgetFactory) {
    echo 'Да, $WF - WidgetFactory';
}
?>
```

### Дивіться також

-   [getclass()](function.get-class.html) - Повертає ім'я класу, до якого належить об'єкт
-   [getparentclass()](function.get-parent-class.html) - Повертає ім'я батьківського класу для об'єкта чи класу
-   [ісsubclassof()](function.is-subclass-of.html) - Перевіряє, чи містить об'єкт у своєму дереві предків зазначений клас чи прямо реалізує його