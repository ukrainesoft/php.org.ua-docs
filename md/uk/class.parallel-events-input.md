Клас parallelEventsInput

-   [« parallelEvents::poll](parallel-events.poll.html)
    
-   [parallelEventsInput::add »](parallel-events-input.add.html)
    
-   [PHP Manual](index.md)
    
-   [parallel](book.parallel.md)
    
-   Клас parallelEventsInput
    

# Клас parallelEventsInput

## Вхідні дані подій

Об'єкт Input - це контейнер для даних, які об'єкт [parallelEvents](class.parallel-events.html) запише до об'єктів [parallelChannel](class.parallel-channel.html) у міру їхньої доступності. Декілька циклів подій можуть спільно використовувати контейнер введення - parallel не перевіряє вміст контейнера, якщо він встановлений як вхідні дані для об'єкта [parallelEvents](class.parallel-events.html)

> **Зауваження**
> 
> Коли об'єкт [parallelEvents](class.parallel-events.html) виконує запис, мета видаляється з об'єкта вхідних даних, якби був викликаний метод [parallelEventsInput::remove()](parallel-events-input.remove.html)

## Огляд класів

```classsynopsis



    
     
      final
      class parallel\Events\Input
     
     {


    
   public add(string $target, mixed $value): void

    public remove(string $target): void

    public clear(): void


   }
```

## Зміст

-   [parallelEventsInput::add](parallel-events-input.add.html) - Входи
-   [parallelEventsInput::clear](parallel-events-input.clear.html) - Входи
-   [parallelEventsInput::remove](parallel-events-input.remove.html) - Входи