Клас QuickHashIntHash

-   [« QuickHashIntSet::saveToString](quickhashintset.savetostring.html)
    
-   [QuickHashIntHash::add »](quickhashinthash.add.html)
    
-   [PHP Manual](index.html)
    
-   [Quickhash](book.quickhash.html)
    
-   Клас QuickHashIntHash
    

# Клас QuickHashIntHash

(PECL quickhash >= Unknown)

## Вступ

Клас-обгортка для хеш-таблиці з ключами та значеннями, що є цілими числами. Також реалізує інтерфейс [ArrayAccess](class.arrayaccess.html)

Клас реалізує інтерфейс [Iterator](class.iterator.html)що дає можливість перебору за допомогою конструкції [`foreach`](control-structures.foreach.html). Порядок проходження елементів не гарантується.

## Огляд класів

```classsynopsis


    
    
     
      class QuickHashIntHash
     
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
    
   public add(int $key, int $value = ?): bool
public __construct(int $size, int $options = ?)
public delete(int $key): bool
public exists(int $key): bool
public get(int $key): int
public getSize(): int
public static loadFromFile(string $filename, int $options = ?): QuickHashIntHash
public static loadFromString(string $contents, int $options = ?): QuickHashIntHash
public saveToFile(string $filename): void
public saveToString(): string
public set(int $key, int $value): bool
public update(int $key, int $value): bool

   }
```

## Обумовлені константи

**`QuickHashIntHash::CHECK_FOR_DUPES`**

Якщо увімкнено, то додавання повторюваних елементів до набору (за допомогою методів [QuickHashIntHash::add()](quickhashinthash.add.html) або [QuickHashIntHash::loadFromFile()](quickhashinthash.loadfromfile.html)) призведе до відкидання цих елементів. Ця функціональність дещо уповільнює роботу, так що має використовуватися лише якщо дійсно необхідний.

**`QuickHashIntHash::DO_NOT_USE_ZEND_ALLOC`**

Забороняє використання вбудованого в PHP менеджера пам'яті внутрішніх структур. Якщо увімкнено цю опцію, то пам'ять, що використовується, не враховуватиметься налаштуванням [memory\_limit](ini.core.html#ini.memory-limit)

**`QuickHashIntHash::HASHER_NO_HASH`**

Вказує, що не потрібно використовувати функцію хешування, а замість неї для пошуку індексу в ланцюжку використовувати модуль. Це не швидше за звичайне хешування і породжує більше колізій.

**`QuickHashIntHash::HASHER_JENKINS1`**

Функція, що хешує, за замовчуванням.

**`QuickHashIntHash::HASHER_JENKINS2`**

Інший хешуючий алгоритм.

## Зміст

-   [QuickHashIntHash::add](quickhashinthash.add.html) — Додати елемент у хеш
-   [QuickHashIntHash::\_\_construct](quickhashinthash.construct.html) — Створює об'єкт QuickHashIntHash
-   [QuickHashIntHash::delete](quickhashinthash.delete.html) — Метод видаляє запис із хешу
-   [QuickHashIntHash::exists](quickhashinthash.exists.html) — Метод перевіряє, чи є ключ частиною хешу
-   [QuickHashIntHash::get](quickhashinthash.get.html) — Метод отримує значення з хеша за його ключем.
-   [QuickHashIntHash::getSize](quickhashinthash.getsize.html) — Повертає кількість елементів у хеші
-   [QuickHashIntHash::loadFromFile](quickhashinthash.loadfromfile.html) — Фабричний метод створює хеш із файлу
-   [QuickHashIntHash::loadFromString](quickhashinthash.loadfromstring.html) — Фабричний метод створює хеш із рядка
-   [QuickHashIntHash::saveToFile](quickhashinthash.savetofile.html) — Метод зберігає хеш у пам'яті на диск
-   [QuickHashIntHash::saveToString](quickhashinthash.savetostring.html) — Метод повертає серіалізовану версію хешу
-   [QuickHashIntHash::set](quickhashinthash.set.html) — Метод оновлює запис у хеші новим значенням або додає новий, якщо запис не існує
-   [QuickHashIntHash::update](quickhashinthash.update.html) — Метод оновлює запис у хеші новим значенням