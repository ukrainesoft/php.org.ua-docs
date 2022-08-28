Оголошення класів атрибутів

-   [« Чтение атрибутов с помощью Reflection API](language.attributes.reflection.html)
    
-   [Объяснение ссылок »](language.references.html)
    
-   [PHP Manual](index.html)
    
-   [Атрибуты](language.attributes.html)
    
-   Оголошення класів атрибутів
    

## Оголошення класів атрибутів

Створювати класи для атрибутів необов'язково, але рекомендується. У найпростішому випадку потрібно просто порожній клас з атрибутом `#[Attribute]`, який можна імпортувати з глобального простору назв за допомогою оператора use.

**Приклад #1 Простий клас з атрибутом**

```php
<?php

namespace Example;

use Attribute;

#[Attribute]
class MyAttribute
{
}
```

Для обмеження того, з яким типом декларацій можна використовувати конкретний атрибут, можна передати бітову маску першим параметром `#[Attribute]`

**Приклад #2 Обмеження допустимих сутностей використання атрибута**

```php
<?php

namespace Example;

use Attribute;

#[Attribute(Attribute::TARGET_METHOD | Attribute::TARGET_FUNCTION)]
class MyAttribute
{
}
```

Після цього анотування атрибутом **MyAttribute** чогось, що відрізняється від методу або функції, призведе до викидання винятку під час виклику [ReflectionAttribute::newInstance()](reflectionattribute.newinstance.html)

Можна вказати такі сутності:

-   **`Attribute::TARGET_CLASS`**
-   **`Attribute::TARGET_FUNCTION`**
-   **`Attribute::TARGET_METHOD`**
-   **`Attribute::TARGET_PROPERTY`**
-   **`Attribute::TARGET_CLASS_CONSTANT`**
-   **`Attribute::TARGET_PARAMETER`**
-   **`Attribute::TARGET_ALL`**

За умовчанням, атрибут можна використовувати лише один раз для кожної сутності. Якщо потрібно вказувати кілька однакових атрибутів для однієї сутності - можна виставити відповідний прапор у бітовій масці для декларації `#[Attribute]`

**Приклад #3 Використання ISREPEATABLE для дозволу використовувати атрибут в оголошенні кілька разів**

```php
<?php

namespace Example;

use Attribute;

#[Attribute(Attribute::TARGET_METHOD | Attribute::TARGET_FUNCTION | Attribute::IS_REPEATABLE)]
class MyAttribute
{
}
```