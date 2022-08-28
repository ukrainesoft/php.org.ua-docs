Клас SwooleTable

-   [« Swoole\\Server::tick](swoole-server.tick.html)
    
-   [Swoole\\Table::column »](swoole-table.column.html)
    
-   [PHP Manual](index.html)
    
-   [Swoole](book.swoole.html)
    
-   Клас SwooleTable
    

# Клас SwooleTable

(PECL swoole >= 1.9.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class Swoole\Table
     

     implements 
       Iterator,  Countable {

    /* Константы */
    
     const
     int
      TYPE_INT = 1;

    const
     int
      TYPE_STRING = 7;

    const
     int
      TYPE_FLOAT = 6;


    /* Методы */
    
   public column(string $name, string $type, int $size = ?): ReturnType
public count(): int
public create(): void
public current(): array
public decr(string $key, string $column, int $decrby = ?): ReturnType
public del(string $key): void
public destroy(): void
public exist(string $key): bool
public get(string $row_key, string $column_key): int
public incr(string $key, string $column, int $incrby = ?): void
public key(): string
public next(): ReturnType
public rewind(): void
public set(string $key, array $value): VOID
public valid(): bool

   }
```

## Обумовлені константи

**`Swoole\Table::TYPE_INT`**

**`Swoole\Table::TYPE_STRING`**

**`Swoole\Table::TYPE_FLOAT`**

## Зміст

-   [Swoole\\Table::column](swoole-table.column.html) — Встановлює тип даних та розмір стовпців
-   [Swoole\\Table::\_\_construct](swoole-table.construct.html) — Створює таблицю пам'яті Swoole із фіксованим розміром
-   [Swoole\\Table::count](swoole-table.count.html) — Підраховує рядки у таблиці або підраховує всі елементи у таблиці, якщо $mode = 1
-   [Swoole\\Table::create](swoole-table.create.html) - Створює таблицю пам'яті swoole
-   [Swoole\\Table::current](swoole-table.current.html) — Отримує поточний рядок
-   [Swoole\\Table::decr](swoole-table.decr.html) — Зменшує значення у таблиці Swoole за $rowkey та $columnkey
-   [Swoole\\Table::del](swoole-table.del.html) — Видаляє рядок у таблиці Swoole за $rowkey
-   [Swoole\\Table::destroy](swoole-table.destroy.html) - Знищує таблицю Swoole
-   [Swoole\\Table::exist](swoole-table.exist.html) — Перевіряє, чи існує рядок $rowkey
-   [Swoole\\Table::get](swoole-table.get.html) — Отримує значення у таблиці Swoole за $rowkey та $columnkey
-   [Swoole\\Table::incr](swoole-table.incr.html) — Збільшує значення $rowkey та $columnkey
-   [Swoole\\Table::key](swoole-table.key.html) — Отримує ключ поточного рядка
-   [Swoole\\Table::next](swoole-table.next.html) — Переміщує ітератор на наступний рядок
-   [Swoole\\Table::rewind](swoole-table.rewind.html) - Перемотує ітератор
-   [Swoole\\Table::set](swoole-table.set.html) — Оновлює рядок таблиці $rowkey
-   [Swoole\\Table::valid](swoole-table.valid.html) — Перевіряє, чи поточний рядок є коректним