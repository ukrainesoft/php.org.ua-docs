Створити інвертований транслітератор

-   [« Transliterator::createFromRules](transliterator.createfromrules.html)
    
-   [Transliterator::getErrorCode »](transliterator.geterrorcode.html)
    
-   [PHP Manual](index.html)
    
-   [Transliterator](class.transliterator.html)
    
-   Створити інвертований транслітератор
    

# Transliterator::createInverse

# transliteratorcreateinverse

(PHP 5 >= 5.4.0, PHP 7, PHP 8, PECL intl >= 2.0.0)

Transliterator::createInverse -- transliteratorcreateinverse — Створити інвертований транслітератор

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public Transliterator::createInverse(): ?Transliterator
```

Процедурний стиль

```methodsynopsis
transliterator_create_inverse(Transliterator $transliterator): ?Transliterator
```

Відкриває інвертований транслітератор.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт [Transliterator](class.transliterator.html) або **`null`** у разі виникнення помилки.

### Дивіться також

-   [Transliterator::getErrorMessage()](transliterator.geterrormessage.html) - Отримати останнє повідомлення про помилку
-   [Transliterator::create()](transliterator.create.html) - Створити транслітератор