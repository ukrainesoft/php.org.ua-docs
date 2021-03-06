- [« SplHeap::valid](splheap.valid.md)
- [SplMaxHeap::compare »](splmaxheap.compare.md)

- [PHP Manual](index.md)
- [Структури даних](spl.datastructures.md)
- Клас SplMaxHeap

# Клас SplMaxHeap

(PHP 5 \>= 5.3.0, PHP 7, PHP 8)

## Вступ

Клас SplMaxHeap надає основні функціональні можливості купи,
зберігаючи максимальний елемент зверху.

## Огляд класів

class **SplMaxHeap** extends [SplHeap](class.splheap.md) {

/\* Методи \*/

protected
[compare](splmaxheap.compare.md)([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$value1`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$value2`): int

/\* Наслідувані методи \*/

protected
[SplHeap::compare](splheap.compare.md)([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$value1`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$value2`): int

public [SplHeap::count](splheap.count.md)(): int

public [SplHeap::current](splheap.current.md)():
[mixed](language.types.declarations.md#language.types.declarations.mixed)

public [SplHeap::extract](splheap.extract.md)():
[mixed](language.types.declarations.md#language.types.declarations.mixed)

public
[SplHeap::insert](splheap.insert.md)([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$value`): bool

public [SplHeap::isCorrupted](splheap.iscorrupted.md)(): bool

public [SplHeap::isEmpty](splheap.isempty.md)(): bool

public [SplHeap::key](splheap.key.md)(): int

public [SplHeap::next](splheap.next.md)(): void

public
[SplHeap::recoverFromCorruption](splheap.recoverfromcorruption.md)():
bool

public [SplHeap::rewind](splheap.rewind.md)(): void

public [SplHeap::top](splheap.top.md)():
[mixed](language.types.declarations.md#language.types.declarations.mixed)

public [SplHeap::valid](splheap.valid.md)(): bool

}

## Зміст

- [SplMaxHeap::compare](splmaxheap.compare.md) — Порівнює
елементи, щоб під час сортування коректно розмістити їх у купі
