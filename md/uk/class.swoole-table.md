---
navigation:
  - swoole-server.tick.md: '« SwooleServer::tick'
  - swoole-table.column.md: 'SwooleTable::column »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас SwooleTable
---
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

-   [SwooleTable::column](swoole-table.column.md) — Встановлює тип даних та розмір стовпців
-   [SwooleTable::construct](swoole-table.construct.md) — Створює таблицю пам'яті Swoole із фіксованим розміром
-   [SwooleTable::count](swoole-table.count.md) — Підраховує рядки у таблиці або підраховує всі елементи у таблиці, якщо $mode = 1
-   [SwooleTable::create](swoole-table.create.md) - Створює таблицю пам'яті swoole
-   [SwooleTable::current](swoole-table.current.md) — Отримує поточний рядок
-   [SwooleTable::decr](swoole-table.decr.md) — Зменшує значення у таблиці Swoole за $rowkey та $columnkey
-   [SwooleTable::del](swoole-table.del.md) — Видаляє рядок у таблиці Swoole за $rowkey
-   [SwooleTable::destroy](swoole-table.destroy.md) - Знищує таблицю Swoole
-   [SwooleTable::exist](swoole-table.exist.md) — Перевіряє, чи існує рядок $rowkey
-   [SwooleTable::get](swoole-table.get.md) — Отримує значення у таблиці Swoole за $rowkey та $columnkey
-   [SwooleTable::incr](swoole-table.incr.md) — Збільшує значення $rowkey та $columnkey
-   [SwooleTable::key](swoole-table.key.md) — Отримує ключ поточного рядка
-   [SwooleTable::next](swoole-table.next.md) — Переміщує ітератор на наступний рядок
-   [SwooleTable::rewind](swoole-table.rewind.md) - Перемотує ітератор
-   [SwooleTable::set](swoole-table.set.md) — Оновлює рядок таблиці $rowkey
-   [SwooleTable::valid](swoole-table.valid.md) — Перевіряє, чи поточний рядок є коректним
