---
navigation:
  - class.parallel-channel.html: « parallelChannel
  - parallel-channel.make.html: 'parallelChannel::make »'
  - index.html: PHP Manual
  - class.parallel-channel.html: parallelChannel
title: 'parallelChannel::construct'
---
# parallelChannel::construct

parallelChannel::construct - Конструктор класу Channel

### Опис

```methodsynopsis
public parallel\Channel::__construct()
```

Створює анонімний небуферизований канал

```methodsynopsis
public parallel\Channel::__construct(int $capacity)
```

Створює анонімний буферизований канал із заданою ємністю.

### Список параметрів

`capacity`

Може бути Channel::Infinite або позитивним цілим числом.
