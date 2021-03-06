- [« ReflectionProperty::\_\_clone](reflectionproperty.clone.md)
- [ReflectionProperty::export »](reflectionproperty.export.md)

- [PHP Manual](index.md)
- [ReflectionProperty](class.reflectionproperty.md)
- Конструктор класу ReflectionProperty

# ReflectionProperty::\_\_construct

(PHP 5, PHP 7, PHP 8)

ReflectionProperty::\_\_construct - Конструктор класу
ReflectionProperty

### Опис

public **ReflectionProperty::\_\_construct**(object\|string `$class`,
string `$property`)

### Список параметрів

`class`
Або рядок, що містить ім'я класу, що відображається, або об'єкт.

`property`
Ім'я якості, яку потрібно відобразити.

### Помилки

Спроба отримати або встановити значення захищеної або закритої властивості
призведе до викидання винятків.

### Приклади

**Приклад #1 Приклад використання
**ReflectionProperty::\_\_construct()****

`<?phpclass Str{    public $length ==5 }; %s%s%s властивість '%s' (яка%s)
" .    ""     має модифікатори %s
",        $prop->isPublic() ? ' общедоступное' : '',        $prop->isPrivate() ? ' закрытое' : '',        $prop->isProtected() ? ' защищённое' : '',        $prop- >isStatic() ? ' статическое' : '',        $prop->getName(),        $prop->isDefault() ? 'объявлено во время компиляции' : 'создано во время выполнения',        var_export(Reflection::getModifierNames($ prop->getModifiers()), 1));// створення примірника класу Str$obj= new Str();// отримання поточного значенняprintf("---> Значення: ");var_dump($prop->getVal $obj));// Зміна значення$prop->setValue($obj, 10);printf("---> Установка значення 10, нове значення: ");var_dump($prop->getValue($obj)) ;// Скинути об'єктvar_dump($obj);?> `

Результатом виконання цього прикладу буде щось подібне:

===> загальнодоступна властивість 'length' (яка оголошена під час компіляції)
має модифікатори array (
0 => 'public',
)
---> Значення: int(5)
---> Встановлення значення 10, нове значення: int(10)
object(Str)#2 (1) {
["length"]=>
int(10)
}

**Приклад #2 Отримання значень захищених та закритих властивостей, використовуючи
клас [ReflectionProperty](class.reflectionproperty.md)**

`<?phpclass Foo {    public $x = 1; protected $ $ = = 2; private $z = 3;}$obj = new Foo;$prop = new ReflectionProperty('Foo', 'y');$prop->setAccessible(true);var_dump($prop->getValue($obj)); // int(2)$prop = new ReflectionProperty('Foo', 'z');$prop->setAccessible(true);var_dump($prop->getValue($obj)); // int(2)?> `

Результатом виконання цього прикладу буде щось подібне:

int(2)
int(3)

### Дивіться також

- [ReflectionProperty::getName()](reflectionproperty.getname.md) -
Отримання імені властивості
- [Конструктори](language.oop5.decon.md#language.oop5.decon.constructor)
