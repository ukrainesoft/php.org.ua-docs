Конструктор класу Channel

-   [« parallelChannel](class.parallel-channel.html)
    
-   [parallelChannel::make »](parallel-channel.make.html)
    
-   [PHP Manual](index.html)
    
-   [parallelChannel](class.parallel-channel.html)
    
-   Конструктор класу Channel
    

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