---
navigation:
  - parallel-future.value.md: '« parallel\\Future::value'
  - parallel-channel.construct.md: 'parallel\\Channel::\_\_construct »'
  - index.md: PHP Manual
  - book.parallel.md: parallel
title: Клас parallel\\Channel
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас parallel\\Channel

(0.9.0)

## Небуферизовані канали

Небуферизований канал блокуватиметься під час дзвінків [parallel\\Channel::send()](parallel-channel.send.md) до тих пір, поки не з'явиться одержувач, і блокуватись при викликах [parallel\\Channel::recv()](parallel-channel.recv.md) доти, доки з'явиться відправник. Це означає, що небуферизований канал - це спосіб обміну даними між завданнями, а й простий метод синхронізації.

Небуферизований канал - це найшвидший спосіб обміну даними між завданнями, що вимагає найменшої кількості копіювання.

## Буферизовані канали

Буферизований канал не блокуватиметься під час дзвінків [parallel\\Channel::send()](parallel-channel.send.md) до заповнення буфера, а дзвінки [parallel\\Channel::recv()](parallel-channel.recv.md) блокуватимуться до тих пір, поки в буфері є дані.

## Замикання поверх каналів

Потужна особливість паралельних каналів у тому, що дозволяють обмінюватися замиканнями між завданнями (і середовищами виконання).

Коли замикання відправляється по каналу, воно буферизується, не змінює буферизацію каналу, що передає замикання, але воно впливає на статичну область видимості всередині замикання: одне і те ж замикання, відправлене в різні середовища виконання або в те саме середовище виконання, не ділитися своєю статичною областю.

Це означає, що кожного разу, коли виконується замикання, яке було передане каналом, статичний стан буде таким, яким воно було при буферизації замикання.

## Анонімні канали

Конструктор анонімного каналу дозволяє програмісту уникати присвоєння імен кожному каналу: parallel генерує унікальне ім'я анонімних каналів.

## Огляд класів

```classsynopsis



    
     
      final
      class parallel\Channel
     
     {


    /* Анонимный конструктор */
    
   public __construct()
public __construct(int $capacity)


    /* Доступ */
    public make(string $name): Channel
public make(string $name, int $capacity): Channel
public open(string $name): Channel


    /* Совместное использование */
    public recv(): mixed
public send(mixed $value): void


    /* Закрытие */
    public close(): void


    /* Константа для бесконечной буферизации */
    
     const
      Infinite;


   }
```

## Зміст

-   [parallel\\Channel::\_\_construct](parallel-channel.construct.md) \- Конструктор класу Channel
-   [parallel\\Channel::make](parallel-channel.make.md) \- Доступ
-   [parallel\\Channel::open](parallel-channel.open.md) \- Доступ
-   [parallel\\Channel::recv](parallel-channel.recv.md) \- Спільне використання
-   [parallel\\Channel::send](parallel-channel.send.md) \- Спільне використання
-   [parallel\\Channel::close](parallel-channel.close.md) \- Закриття
