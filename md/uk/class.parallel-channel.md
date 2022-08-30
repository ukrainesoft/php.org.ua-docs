Клас parallelChannel

-   [« parallelFuture::value](parallel-future.value.html)
    
-   [parallelChannel::construct »](parallel-channel.construct.html)
    
-   [PHP Manual](index.html)
    
-   [parallel](book.parallel.html)
    
-   Клас parallelChannel
    

# Клас parallelChannel

## Небуферизовані канали

Небуферизований канал блокуватиме виклики [parallelChannel::send()](parallel-channel.send.html) до тих пір, поки не буде одержувач і блокуватиме дзвінки [parallelChannel::recv()](parallel-channel.recv.html) доти, доки відправник. Це означає, що небуферизований канал - це спосіб обміну даними між завданнями, а й простий метод синхронізації.

Небуферизований канал – це найшвидший спосіб обміну даними між завданнями, що вимагає найменшої кількості копіювання.

## Буферизовані канали

Буферизований канал не блокуватиметься під час дзвінків [parallelChannel::send()](parallel-channel.send.html) доти, доки не буде досягнуто ємності, виклики [parallelChannel::recv()](parallel-channel.recv.html) буде блокуватись, поки в буфері не з'являться дані.

## Замикання поверх каналів

Потужна особливість паралельних каналів полягає в тому, що вони дозволяють обмінюватися замикання між завданнями (і середовищами виконання).

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

-   [parallelChannel::construct](parallel-channel.construct.html) - Конструктор класу Channel
-   [parallelChannel::make](parallel-channel.make.html) - Доступ
-   [parallelChannel::open](parallel-channel.open.html) - Доступ
-   [parallelChannel::recv](parallel-channel.recv.html) - Спільне використання
-   [parallelChannel::send](parallel-channel.send.html) - Спільне використання
-   [parallelChannel::close](parallel-channel.close.html) - Закриття