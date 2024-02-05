---
navigation:
  - class.random-engine-pcgoneseq128xslrr64.md: « Random\\Engine\\PcgOneseq128XslRr64
  - random-engine-pcgoneseq128xslrr64.debuginfo.md: 'Random\\Engine\\PcgOneseq128XslRr64::\_\_debugInfo »'
  - index.md: PHP Manual
  - class.random-engine-pcgoneseq128xslrr64.md: Random\\Engine\\PcgOneseq128XslRr64
title: 'Random\\Engine\\PcgOneseq128XslRr64::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Random\\Engine\\PcgOneseq128XslRr64::\_\_construct

(PHP 8 >= 8.2.0)

Random\\Engine\\PcgOneseq128XslRr64::\_\_construct - Створює новий двигун PCG Oneseq 128 XSL RR 64

### Опис

public**Random\\Engine\\PcgOneseq128XslRr64::\_\_construct**(string|int|null`$seed` **`null`**) .

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`seed`

Спосіб наповнення внутрішнього 128-бітного (16-байтного) стану, що складається з одного 128-бітного цілого числа без знака, залежить від типу, що використовується як параметр `seed`

| Тип | Опис |
| --- | --- |
| null | Заповнює стан 16 випадковими байтами, що згенеровані за допомогою CSPRNG. |
| int | Заповнює стан, встановлюючи стан у , просуваючи двигун на один крок, додаючи значення параметра `seed`, що інтерпретується як 64-бітове ціле число без знака і просуваючи двигун ще на один крок. |
| string | Заповнює стан інтерпретуючи 16-байтовий рядок (string) як little-endian 128-бітове ціле число без знака. |

### Помилки

-   Якщо довжина строкового (string) параметра`seed`не дорівнює 16 байтам, буде видана помилка[ValueError](class.valueerror.md)

### Приклади

**Пример #1 Пример использования**Random\\Engine\\PcgOneseq128XslRr64::\_\_construct()\*\*\*\*

```php
<?php
// Использование случайного 128-битного значения.
$e = new \Random\Engine\PcgOneseq128XslRr64();

$r = new \Random\Randomizer($e);
?>
```

**Приклад #2 Виведення значення рядка (string)**

```php
<?php
$string = "My string seed";

// Хеширование строки усечённым SHA-256, используя двоичный вывод,
// чтобы превратить $string в 128-битное значение. Использование одной и той же
// строки приведёт к одной и той же случайной последовательности.
$e = new \Random\Engine\PcgOneseq128XslRr64(
    substr(hash('sha256', $string, binary: true), 0, 16)
);

echo bin2hex($e->generate()), "\n";
?>
```

Результат виконання наведеного прикладу:

```
8333ef59315b16d8
```
