- [«ps_findfont](function.ps-findfont.md)
- [ps_get_parameter »](function.ps-get-parameter.md)

- [PHP Manual](index.md)
- [Функції PS](ref.ps.md)
- отримує повний буфер, що містить згенеровані дані PS

#ps_get_buffer

(PECL ps \>= 1.1.0)

ps_get_buffer — Отримує повний буфер, що містить згенеровані дані
PS

### Опис

**ps_get_buffer**(resource `$psdoc`): string

Функція поки що не реалізована. Вона завжди повертатиме порожній рядок.
Ідея для пізнішої реалізації полягає в тому, щоб записати
вміст файлу postscript у внутрішній буфер, якщо потрібно створення
у пам'яті, і отримати вміст буфера за допомогою цієї функції. В
В даний час документи, створені в пам'яті, відправляються в браузер
без буферизації.

**Увага**

На цей час ця функція ще була документована; для
ознайомлення доступний лише список аргументів.

### Список параметрів

`psdoc`
Ідентифікатор ресурсу файлу postscript, повернутий функцією
[ps_new()](function.ps-new.md).

### Дивіться також

- [ps_open_file()](function.ps-open-file.md) - Відкриває файл для
висновку
