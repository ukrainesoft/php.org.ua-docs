- [« Черга](class.ds-queue.md)
- [Ds\Queue::capacity »](ds-queue.capacity.md)

- [PHP Manual](index.md)
- [Черга](class.ds-queue.md)
- Виділяє пам'ять під зазначену місткість

# Ds\Queue::allocate

(PECL ds \>= 1.0.0)

Ds\Queue::allocate — Виділяє пам'ять під зазначену місткість

### Опис

public **Ds\Queue::allocate**(int `$capacity`): void

Гарантує, що виділено достатньо пам'яті під задану місткість
(кількість значень). Дозволяє уникнути динамічного
перерозподіл пам'яті при додаванні значень.

> **Примітка**:
>
> Значення місткості округляється до найближчого ступеня двійки (тобто 8,
> 16, 32, 64, 128 і т.д.)

### Список параметрів

`capacity`
Місткість. Очікувана кількість значень.

> **Примітка**:
>
> Якщо нове значення місткості менше поточного, вона не зміниться.

> **Примітка**:
>
> Значення місткості округляється до найближчого ступеня двійки (тобто 8,
> 16, 32, 64, 128 і т.д.)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **Ds\Queue::allocate()****

` <?php$queue = new \Ds\Queue();var_dump($queue->capacity());$queue->allocate(100);var_dump($queue->capacity());?> `

Результатом виконання цього прикладу буде щось подібне:

int(8)
int(128)
