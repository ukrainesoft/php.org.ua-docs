---
navigation:
  - parallel-events.poll.md: '« parallel\\Events::poll'
  - parallel-events-input.add.md: 'parallel\\Events\\Input::add »'
  - index.md: PHP Manual
  - book.parallel.md: parallel
title: Клас parallel\\Events\\Input
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас parallel\\Events\\Input

(0.9.0)

## Вхідні дані подій

Об'єкт Input - це контейнер для даних, які об'єкт [parallel\\Events](class.parallel-events.md) запише до об'єктів [parallel\\Channel](class.parallel-channel.md) у міру їхньої доступності. Декілька циклів подій можуть спільно використовувати контейнер введення - parallel не перевіряє вміст контейнера, якщо він встановлений як вхідні дані для об'єкта [parallel\\Events](class.parallel-events.md)

> **Зауваження** :
> 
> Коли об'єкт [parallel\\Events](class.parallel-events.md) виконує запис, мета видаляється з об'єкта вхідних даних, як би був викликаний метод [parallel\\Events\\Input::remove()](parallel-events-input.remove.md)

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

-   [parallel\\Events\\Input::add](parallel-events-input.add.md) \- Входи
-   [parallel\\Events\\Input::clear](parallel-events-input.clear.md) \- Входи
-   [parallel\\Events\\Input::remove](parallel-events-input.remove.md) \- Входи
