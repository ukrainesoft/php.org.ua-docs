---
navigation:
  - parallel-events.poll.html: '« parallelEvents::poll'
  - parallel-events-input.add.html: 'parallelEventsInput::add »'
  - index.md: PHP Manual
  - book.parallel.md: parallel
title: Клас parallelEventsInput
---
# Клас parallelEventsInput

## Вхідні дані подій

Об'єкт Input - це контейнер для даних, які об'єкт [parallelEvents](class.parallel-events.html) запише до об'єктів [parallelChannel](class.parallel-channel.html) у міру їхньої доступності. Декілька циклів подій можуть спільно використовувати контейнер введення - parallel не перевіряє вміст контейнера, якщо він встановлений як вхідні дані для об'єкта [parallelEvents](class.parallel-events.md)

> **Зауваження**
> 
> Коли об'єкт [parallelEvents](class.parallel-events.html) виконує запис, мета видаляється з об'єкта вхідних даних, якби був викликаний метод [parallelEventsInput::remove()](parallel-events-input.remove.md)

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

-   [parallelEventsInput::add](parallel-events-input.add.md) - Входи
-   [parallelEventsInput::clear](parallel-events-input.clear.md) - Входи
-   [parallelEventsInput::remove](parallel-events-input.remove.md) - Входи
