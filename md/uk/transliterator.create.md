Створити транслітератор

-   [« Transliterator::\_\_construct](transliterator.construct.html)
    
-   [Transliterator::createFromRules »](transliterator.createfromrules.html)
    
-   [PHP Manual](index.html)
    
-   [Transliterator](class.transliterator.html)
    
-   Створити транслітератор
    

# Transliterator::create

# transliteratorcreate

(PHP 5 >= 5.4.0, PHP 7, PHP 8, PECL intl >= 2.0.0)

Transliterator::create -- transliteratorcreate — Створити транслітератор

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static Transliterator::create(string $id, int $direction = Transliterator::FORWARD): ?Transliterator
```

Процедурний стиль

```methodsynopsis
transliterator_create(string $id, int $direction = Transliterator::FORWARD): ?Transliterator
```

Відкриває об'єкт Transliterator за ідентифікатором.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`id`

Ідентифікатор. Список усіх зареєстрованих ідентифікаторів транслітератора можна отримати за допомогою [Transliterator::listIDs()](transliterator.listids.html)

`direction`

Напрямок транслітерації. За замовчуванням [\>Transliterator::FORWARD](class.transliterator.html#transliterator.constants.forward). Можно використовувати [Transliterator::REVERSE](class.transliterator.html#transliterator.constants.reverse)

### Значення, що повертаються

Повертає об'єкт [Transliterator](class.transliterator.html) або **`null`** у разі виникнення помилки.

### Дивіться також

-   [Transliterator::getErrorMessage()](transliterator.geterrormessage.html) - Отримати останнє повідомлення про помилку
-   [Transliterator::\_\_construct()](transliterator.construct.html) - Приватний конструктор