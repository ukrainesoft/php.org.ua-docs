---
navigation:
  - quickhash.examples.md: « Приклади
  - quickhashintset.add.md: 'QuickHashIntSet::add »'
  - index.md: PHP Manual
  - book.quickhash.md: Quickhash
title: Клас QuickHashIntSet
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас QuickHashIntSet

(PECL quickhash >= Unknown)

## Вступ

Клас обгортка над набором цілих чисел.

Клас реалізує інтерфейс [Iterator](class.iterator.md)що дає можливість перебору за допомогою конструкції [`foreach`](control-structures.foreach.md). Порядок проходження елементів не гарантується.

## Огляд класів

```classsynopsis


    
    
     
      class QuickHashIntSet
     
     {
    
    /* Константы */
    
     const
     int
      CHECK_FOR_DUPES = 1;

    const
     int
      DO_NOT_USE_ZEND_ALLOC = 2;

    const
     int
      HASHER_NO_HASH = 256;

    const
     int
      HASHER_JENKINS1 = 512;

    const
     int
      HASHER_JENKINS2 = 1024;


    /* Методы */
    
   public add(int $key): bool
public __construct(int $size, int $options = ?)
public delete(int $key): bool
public exists(int $key): bool
publicgetSize(): int
public static loadFromFile(string $filename, int $size = ?, int $options = ?): QuickHashIntSet
public static loadFromString(string $contents, int $size = ?, int $options = ?): QuickHashIntSet
public saveToFile(string $filename): void
public saveToString(): string

   }
```

## Обумовлені константи

**`QuickHashIntSet::CHECK_FOR_DUPES`**

Якщо увімкнено, то додавання повторюваних елементів до набору (за допомогою методів [QuickHashIntSet::add()](quickhashintset.add.md) або [QuickHashIntSet::loadFromFile()](quickhashintset.loadfromfile.md)) призведе до відкидання цих елементів. Ця функціональність дещо уповільнює роботу, так що має використовуватися лише якщо дійсно необхідний.

**`QuickHashIntSet::DO_NOT_USE_ZEND_ALLOC`**

Забороняє використання вбудованого в PHP менеджера пам'яті внутрішніх структур. Якщо увімкнено цю опцію, то пам'ять, що використовується, не враховуватиметься налаштуванням [memory\_limit](ini.core.md#ini.memory-limit)

**`QuickHashIntSet::HASHER_NO_HASH`**

Вказує, що не потрібно використовувати хешування, а замість неї для пошуку індексу в ланцюжку використовувати модуль. Це не швидше за звичайне хешування і породжує більше колізій.

**`QuickHashIntSet::HASHER_JENKINS1`**

Функція, що хешує, за замовчуванням.

**`QuickHashIntHash::HASHER_JENKINS2`**

Інший хешуючий алгоритм.

## Зміст

-   [QuickHashIntSet::add](quickhashintset.add.md)— Метод додає новий запис до набору
-   [QuickHashIntSet::\_\_construct](quickhashintset.construct.md)— Створює новий об'єкт QuickHashIntSet
-   [QuickHashIntSet::delete](quickhashintset.delete.md)— Метод видаляє запис із набору
-   [QuickHashIntSet::exists](quickhashintset.exists.md)— Метод перевіряє, чи є ключем частиною набору
-   [QuickHashIntSet::getSize](quickhashintset.getsize.md)— Повертає кількість елементів у наборі
-   [QuickHashIntSet::loadFromFile](quickhashintset.loadfromfile.md)— Фабричний метод створює набір із файлу
-   [QuickHashIntSet::loadFromString](quickhashintset.loadfromstring.md)— Фабричний метод створює набір із рядка
-   [QuickHashIntSet::saveToFile](quickhashintset.savetofile.md)— Метод зберігає набір у пам'яті на диску
-   [QuickHashIntSet::saveToString](quickhashintset.savetostring.md)— Метод повертає серіалізовану версію набору
