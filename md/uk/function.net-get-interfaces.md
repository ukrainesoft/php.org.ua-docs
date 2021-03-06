- [«long2ip](function.long2ip.md)
- [openlog »](function.openlog.md)

- [PHP Manual](index.md)
- [Мережні функції](ref.network.md)
- Отримує мережеві інтерфейси

#net_get_interfaces

(PHP 7 \>= 7.3, PHP 8)

net_get_interfaces — Отримує мережні інтерфейси

### Опис

**net_get_interfaces**(): array\|false

Повертає перелік мережевих інтерфейсів (адаптерів) на локальному
комп'ютер.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає асоціативний масив (array), де ключ – це ім'я інтерфейсу,
а значення – асоціативний масив атрибутів інтерфейсу, або **`false`**
у разі виникнення помилки.

Кожен асоціативний масив інтерфейсу містить:

| Ім'я Опис   |                                                                                           |
|-------------|-------------------------------------------------------------------------------------------|
| description | Необов'язкове рядкове значення для опису інтерфейсу. Тільки Windows.                      |
| mac         | Необов'язкове рядкове значення MAC-адреси інтерфейсу. Тільки Windows.                     |
| mtu         | Цілочисленне значення для максимальної одиниці передачі (MTU) інтерфейсу. Тільки Windows. |
| unicast     | Масив асоціативних масивів, дивіться нижче атрибути одноадресної розсилки.                |
| up          | Логічний статус (увімкнено/вимкнено) інтерфейсу.                                          |

**Interface attributes**

| Ім'я Опис |                                               |
|-----------|-----------------------------------------------|
| flags     | Цілочисленне значення.                        |
| Family    | Цілочисленне значення.                        |
| address   | Рядкове значення адреси в IPv4 або IPv6.      |
| netmask   | Строкове значення маски мережі IPv4 або IPv6. |

**Одноадресні атрибути**

### Помилки

Видає помилку рівня **`E_WARNING`** у разі виникнення помилки при
отримання інформації про інтерфейс.
