Клас QuickHashStringIntHash

-   [« QuickHashIntHash::update](quickhashinthash.update.html)
    
-   [QuickHashStringIntHash::add »](quickhashstringinthash.add.html)
    
-   [PHP Manual](index.html)
    
-   [Quickhash](book.quickhash.html)
    
-   Клас QuickHashStringIntHash
    

# Клас QuickHashStringIntHash

(No version information available, might only be in Git)

## Вступ

Клас-обгортка для хеш-таблиці з рядковими ключами та значеннями, що є цілими числами. Також реалізує інтерфейс [ArrayAccess](class.arrayaccess.html)

Клас реалізує інтерфейс [Iterator](class.iterator.html)що дає можливість перебору за допомогою конструкції [`foreach`](control-structures.foreach.html). Порядок проходження елементів не гарантується.

## Огляд класів

```classsynopsis


    
    
     
      class QuickHashStringIntHash
     
     {
    
    /* Константы */
    
     const
     int
      CHECK_FOR_DUPES = 1;

    const
     int
      DO_NOT_USE_ZEND_ALLOC = 2;


    /* Методы */
    
   public add(string $key, int $value): bool
public __construct(int $size, int $options = 0)
public delete(string $key): bool
public exists(string $key): bool
public get(string $key): mixed
public getSize(): int
public static loadFromFile(string $filename, int $size = 0, int $options = 0): QuickHashStringIntHash
public static loadFromString(string $contents, int $size = 0, int $options = 0): QuickHashStringIntHash
public saveToFile(string $filename): void
public saveToString(): string
public set(string $key, int $value): int
public update(string $key, int $value): bool

   }
```

## Обумовлені константи

**`QuickHashIntHash::CHECK_FOR_DUPES`**

Якщо увімкнено, то додавання повторюваних елементів до набору (за допомогою методів [QuickHashStringIntHash::add()](quickhashstringinthash.add.html) або [QuickHashStringIntHash::loadFromFile()](quickhashstringinthash.loadfromfile.html)) призведе до відкидання цих елементів. Ця функціональність дещо уповільнює роботу, так що має використовуватися лише якщо дійсно необхідний.

**`QuickHashIntHash::DO_NOT_USE_ZEND_ALLOC`**

Забороняє використання вбудованого в PHP менеджера пам'яті внутрішніх структур. Якщо увімкнено цю опцію, то пам'ять, що використовується, не враховуватиметься налаштуванням [memory\_limit](ini.core.html#ini.memory-limit)

## Зміст

-   [QuickHashStringIntHash::add](quickhashstringinthash.add.html) — Метод додає новий запис у хеш
-   [QuickHashStringIntHash::\_\_construct](quickhashstringinthash.construct.html) — Створює новий об'єкт QuickHashStringIntHash
-   [QuickHashStringIntHash::delete](quickhashstringinthash.delete.html) — Метод видаляє запис із хешу
-   [QuickHashStringIntHash::exists](quickhashstringinthash.exists.html) — Метод перевіряє, чи є ключ частиною хешу
-   [QuickHashStringIntHash::get](quickhashstringinthash.get.html) — Метод отримує значення з хеша за його ключем.
-   [QuickHashStringIntHash::getSize](quickhashstringinthash.getsize.html) — Повертає кількість елементів у хеші
-   [QuickHashStringIntHash::loadFromFile](quickhashstringinthash.loadfromfile.html) — Фабричний метод створює хеш із файлу
-   [QuickHashStringIntHash::loadFromString](quickhashstringinthash.loadfromstring.html) — Фабричний метод створює хеш із рядка
-   [QuickHashStringIntHash::saveToFile](quickhashstringinthash.savetofile.html) — Метод зберігає хеш у пам'яті на диску
-   [QuickHashStringIntHash::saveToString](quickhashstringinthash.savetostring.html) — Метод повертає серіалізовану версію хешу
-   [QuickHashStringIntHash::set](quickhashstringinthash.set.html) — Метод оновлює запис у хеші новим значенням або додає новий, якщо запис не існує
-   [QuickHashStringIntHash::update](quickhashstringinthash.update.html) — Метод оновлює запис у хеші новим значенням