Клонує об'єкт

-   [« ReflectionExtension](class.reflectionextension.html)
    
-   [ReflectionExtension::\_\_construct »](reflectionextension.construct.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionExtension](class.reflectionextension.html)
    
-   Клонує об'єкт
    

# ReflectionExtension::clone

(PHP 5, PHP 7, PHP 8)

ReflectionExtension::clone — Клонує об'єкт

### Опис

```methodsynopsis
private ReflectionExtension::__clone(): void
```

Метод clone запобігає клонуванню об'єкта. Об'єкти reflection не можуть бути клоновані.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Метод нічого не повертає, у разі виклику виникає рокова помилка.

### список змін

| Версия | Описание                       |
|--------|--------------------------------|
|        | Метод не є остаточним (final). |

### Дивіться також

-   [ReflectionExtension::\_\_construct()](reflectionextension.construct.html) - Створює об'єкт класу ReflectionExtension
-   [Клонирование объектов](language.oop5.cloning.html)