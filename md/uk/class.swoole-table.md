---
navigation:
  - swoole-server.tick.md: '« Swoole\\Server::tick'
  - swoole-table.column.md: 'Swoole\\Table::column »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас Swoole\\Table
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Swoole\\Table

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

-   [Swoole\\Table::column](swoole-table.column.md)— Встановлює тип даних та розмір стовпців
-   [Swoole\\Table::\_\_construct](swoole-table.construct.md)— Створює таблицю пам'яті Swoole із фіксованим розміром
-   [Swoole\\Table::count](swoole-table.count.md)— Підраховує рядки у таблиці або підраховує всі елементи у таблиці, якщо $mode = 1
-   [Swoole\\Table::create](swoole-table.create.md) \- Створює таблицю пам'яті swoole
-   [Swoole\\Table::current](swoole-table.current.md)— Отримує поточний рядок
-   [Swoole\\Table::decr](swoole-table.decr.md)— Зменшує значення у таблиці Swoole за $row\_key та $column\_key
-   [Swoole\\Table::del](swoole-table.del.md)— Видаляє рядок у таблиці Swoole за $row\_key
-   [Swoole\\Table::destroy](swoole-table.destroy.md) \- Знищує таблицю Swoole
-   [Swoole\\Table::exist](swoole-table.exist.md)— Перевіряє, чи існує рядок $row\_key
-   [Swoole\\Table::get](swoole-table.get.md)— Отримує значення у таблиці Swoole за $row\_key та $column\_key
-   [Swoole\\Table::incr](swoole-table.incr.md)— Збільшує значення $row\_key та $column\_key
-   [Swoole\\Table::key](swoole-table.key.md)— Отримує ключ поточного рядка
-   [Swoole\\Table::next](swoole-table.next.md)— Переміщує ітератор на наступний рядок
-   [Swoole\\Table::rewind](swoole-table.rewind.md) \- Перемотує ітератор
-   [Swoole\\Table::set](swoole-table.set.md)— Оновлює рядок таблиці $row\_key
-   [Swoole\\Table::valid](swoole-table.valid.md)— Перевіряє, чи поточний рядок є коректним
