---
navigation:
  - parallel-runtime.kill.md: '« parallel\\Runtime::kill'
  - parallel-future.cancel.md: 'parallel\\Future::cancel »'
  - index.md: PHP Manual
  - book.parallel.md: parallel
title: Клас parallel\\Future
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас parallel\\Future

(0.8.0)

## Об'єкти Future

Future представляє значення, що повертається або неперехоплений виняток із завдання і надає API для скасування.

**Приклад #1 Приклад, що показує Future як значення, що повертається**

```php
<?php
$runtime = new \parallel\Runtime;
$future  = $runtime->run(function(){
    return "Мир";
});
printf("Привет, %s\n", $future->value());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Привет, Мир
```

Поведінка Future також дозволяє використовувати його як просту точку синхронізації, навіть якщо завдання не повертає значення явно.

**Приклад #2 Приклад, що показує Future як точку синхронізації**

```php
<?php
$runtime = new \parallel\Runtime;
$future  = $runtime->run(function(){
    echo "в дочернем потоке ";
    for ($i = 0; $i < 500; $i++) {
        if ($i % 10 == 0) {
            echo ".";
        }
    }
    echo " выход из дочернего потока";
});

$future->value();
echo "\nродительский поток продолжает работать\n";
?>
```

Висновок наведеного прикладу буде схожим на:

```
в дочернем потоке .................................................. выход из дочернего потока
родительский поток продолжает работать
```

## Огляд класів

```classsynopsis



    
     
      final
      class parallel\Future
     
     {


    /* Разрешение */
    
   public value(): mixed


    /* Состояние */
    public cancelled(): bool
public done(): bool


    /* Отмена */
    public cancel(): bool


   }
```

## Зміст

-   [parallel\\Future::cancel](parallel-future.cancel.md) \- Припинення
-   [parallel\\Future::cancelled](parallel-future.cancelled.md)— Визначення стану
-   [parallel\\Future::done](parallel-future.done.md)— Визначення стану
-   [parallel\\Future::value](parallel-future.value.md) \- Дозвіл
