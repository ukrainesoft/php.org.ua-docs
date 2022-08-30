Клас QuickHashIntStringHash

-   [« QuickHashStringIntHash::update](quickhashstringinthash.update.md)
    
-   [QuickHashIntStringHash::add »](quickhashintstringhash.add.md)
    
-   [PHP Manual](index.md)
    
-   [Quickhash](book.quickhash.md)
    
-   Клас QuickHashIntStringHash
    

# Клас QuickHashIntStringHash

(PECL quickhash >= Unknown)

## Вступ

Клас-обгортка для хеш-таблиці з цілими ключами і значеннями, що є рядками. Також реалізує інтерфейс [ArrayAccess](class.arrayaccess.md)

Клас реалізує інтерфейс [Iterator](class.iterator.md)що дає можливість перебору за допомогою конструкції [`foreach`](control-structures.foreach.html). Порядок проходження елементів не гарантується.

## Огляд класів

```classsynopsis


    
    
     
      class QuickHashIntStringHash
     
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
    
   public add(int $key, string $value): bool
public __construct(int $size, int $options = 0)
public delete(int $key): bool
public exists(int $key): bool
public get(int $key): mixed
public getSize(): int
public static loadFromFile(string $filename, int $size = 0, int $options = 0): QuickHashIntStringHash
public static loadFromString(string $contents, int $size = 0, int $options = 0): QuickHashIntStringHash
public saveToFile(string $filename): void
public saveToString(): string
public set(int $key, string $value): int
public update(int $key, string $value): bool

   }
```

## Обумовлені константи

**`QuickHashIntHash::CHECK_FOR_DUPES`**

Якщо увімкнено, то додавання повторюваних елементів до набору (за допомогою методів [QuickHashIntStringHash::add()](quickhashintstringhash.add.md) або [QuickHashIntStringHash::loadFromFile()](quickhashintstringhash.loadfromfile.md)) призведе до відкидання цих елементів. Ця функціональність дещо уповільнює роботу, так що має використовуватися лише якщо дійсно необхідний.

**`QuickHashIntHash::DO_NOT_USE_ZEND_ALLOC`**

Забороняє використання вбудованого в PHP менеджера пам'яті внутрішніх структур. Якщо увімкнено цю опцію, то пам'ять, що використовується, не враховуватиметься налаштуванням [memorylimit](ini.core.html#ini.memory-limit)

**`QuickHashIntHash::HASHER_NO_HASH`**

Вказує, що не потрібно використовувати функцію хешування, а замість неї для пошуку індексу в ланцюжку використовувати модуль. Це не швидше за звичайне хешування і породжує більше колізій.

**`QuickHashIntHash::HASHER_JENKINS1`**

Функція, що хешує, за замовчуванням.

**`QuickHashIntHash::HASHER_JENKINS2`**

Інший хешуючий алгоритм.

## Зміст

-   [QuickHashIntStringHash::add](quickhashintstringhash.add.md) — Метод додає новий запис у хеш
-   [QuickHashIntStringHash::construct](quickhashintstringhash.construct.md) — Створює новий об'єкт QuickHashIntStringHash
-   [QuickHashIntStringHash::delete](quickhashintstringhash.delete.md) — Метод видаляє запис із хешу
-   [QuickHashIntStringHash::exists](quickhashintstringhash.exists.md) — Метод перевіряє, чи є ключ частиною хешу
-   [QuickHashIntStringHash::get](quickhashintstringhash.get.md) — Метод отримує значення з хеша за його ключем.
-   [QuickHashIntStringHash::getSize](quickhashintstringhash.getsize.md) — Повертає кількість елементів у хеші
-   [QuickHashIntStringHash::loadFromFile](quickhashintstringhash.loadfromfile.md) — Фабричний метод створює хеш із файлу
-   [QuickHashIntStringHash::loadFromString](quickhashintstringhash.loadfromstring.md) — Фабричний метод створює хеш із рядка
-   [QuickHashIntStringHash::saveToFile](quickhashintstringhash.savetofile.md) — Метод зберігає хеш у пам'яті на диску
-   [QuickHashIntStringHash::saveToString](quickhashintstringhash.savetostring.md) — Метод повертає серіалізовану версію хешу
-   [QuickHashIntStringHash::set](quickhashintstringhash.set.md) — Метод оновлює запис у хеші новим значенням або додає новий, якщо запис не існує
-   [QuickHashIntStringHash::update](quickhashintstringhash.update.md) — Метод оновлює запис у хеші новим значенням