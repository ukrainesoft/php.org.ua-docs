---
navigation:
  - parallel-channel.construct.md: '« parallel\\Channel::\_\_construct'
  - parallel-channel.open.md: 'parallel\\Channel::open »'
  - index.md: PHP Manual
  - class.parallel-channel.md: parallel\\Channel
title: 'parallel\\Channel::make'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# parallel\\Channel::make

(0.9.0)

parallel\\Channel::make — Доступ

### Опис

```methodsynopsis
public parallel\Channel::make(string $name): Channel
```

Створює небуферизований канал із заданим ім'ям

```methodsynopsis
public parallel\Channel::make(string $name, int $capacity): Channel
```

Створює буферизований канал із заданим ім'ям та ємністю.

### Список параметрів

`name`

Назва каналу.

`capacity`

Може бути Channel::Infinite або позитивним цілим числом

### Помилки

**Увага**

Викидає parallel\\Channel\\Error\\Existence якщо канал вже існує.
