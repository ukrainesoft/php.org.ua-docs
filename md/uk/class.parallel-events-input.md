Клас parallelEventsInput

-   [« parallel\\Events::poll](parallel-events.poll.html)
    
-   [parallel\\Events\\Input::add »](parallel-events-input.add.html)
    
-   [PHP Manual](index.html)
    
-   [parallel](book.parallel.html)
    
-   Клас parallelEventsInput
    

# Клас parallelEventsInput

## Вхідні дані подій

Об'єкт Input - це контейнер для даних, які об'єкт [parallel\\Events](class.parallel-events.html) запише до об'єктів [parallel\\Channel](class.parallel-channel.html) у міру їхньої доступності. Декілька циклів подій можуть спільно використовувати контейнер введення - parallel не перевіряє вміст контейнера, якщо він встановлений як вхідні дані для об'єкта [parallel\\Events](class.parallel-events.html)

> **Зауваження**
> 
> Коли об'єкт [parallel\\Events](class.parallel-events.html) виконує запис, мета видаляється з об'єкта вхідних даних, якби був викликаний метод [parallel\\Events\\Input::remove()](parallel-events-input.remove.html)

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

-   [parallel\\Events\\Input::add](parallel-events-input.add.html) - Входи
-   [parallel\\Events\\Input::clear](parallel-events-input.clear.html) - Входи
-   [parallel\\Events\\Input::remove](parallel-events-input.remove.html) - Входи