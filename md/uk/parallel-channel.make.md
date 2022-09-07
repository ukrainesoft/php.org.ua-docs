---
navigation:
  - parallel-channel.construct.md: '« parallelChannel::construct'
  - parallel-channel.open.md: 'parallelChannel::open »'
  - index.md: PHP Manual
  - class.parallel-channel.md: parallelChannel
title: 'parallelChannel::make'
---
# parallelChannel::make

parallelChannel::make — Доступ

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

Викидає parallelChannelErrorExistence якщо канал вже існує.
