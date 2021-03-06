- [«dio_close](function.dio-close.md)
- [dio_open »](function.dio-open.md)

- [PHP Manual](index.md)
- [Функції прямого введення/виводу](ref.dio.md)
- Викликає функцію бібліотеки C fcntl для файлового дескриптора

#dio_fcntl

(PHP 4 \>= 4.2.0, PHP 5 \< 5.1.0)

dio_fcntl — Викликає функцію бібліотеки C fcntl для файлового
дескриптора

### Опис

**dio_fcntl**(resource `$fd`, int `$cmd`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$args` = ?):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

Функція **dio_fcntl()** викликає вказану в `cmd` команду для `fd`.
Якщо команда вимагає додаткових аргументів, вони задаються в
`args`.

### Список параметрів

`fd`
Файловий дескриптор, отриманий із [dio_open()](function.dio-open.md).

`cmd`
Може бути однією з наступних операцій:

- **`F_SETLK`** - Встановлення або скидання блокування. Якщо блокування
кимось утримується, **dio_fcntl()** поверне -1.

- **`F_SETLKW`** - схожа на **`F_SETLK`**, але якщо блокування
будь-ким утримується, **dio_fcntl()** чекатиме її звільнення.

- **`F_GETLK`** - **dio_fcntl()** поверне асоціативний масив (як
описано нижче) якщо хтось заважає отримати блокування. Якщо ніхто
не заважає, то ключ "type" міститиме **`F_UNLCK`**.

- **`F_DUPFD`** - шукає найменший доступний файловий дескриптор,
більший чи рівний `args` і повертає його.

- **`F_SETFL`** - встановлює файловий дескриптор прапори, задані
в `args`, такі як **`O_APPEND`**, **`O_NONBLOCK`** або
**`O_ASYNC`**. Для використання **`O_ASYNC`** вам необхідно
скористатися модулем [PCNTL](ref.pcntl.md).

`args`
`args` - це асоціативний масив, якщо `cmd` встановлений у **`F_SETLK`**
або **`F_SETLLW`**, з такими ключами:

- `start` - усунення початку блокування

- `length` – розмір заблокованої зони. 0 означає кінець файлу

- `whence` - залежить від l_start: може бути **`SEEK_SET`**,
**`SEEK_END`** та **`SEEK_CUR`**

- `type` - тип блокування: може бути **`F_RDLCK`** (читання),
**`F_WRLCK`** (запис) або **`F_UNLCK`** (блокування немає)

### Значення, що повертаються

Повертає результат виклику C-функції.

### Приклади

**Приклад #1 Встановлення та зняття блокування**

`<?php$fd = dio_open('/dev/ttyS0', O_RDWR);if (dio_fcntl($fd, F_SETLK, Array("type"=>F_WRLCK)) == -1) {    "Не можна зняти блокування, воно утримується іншим процесом.";} else {   echo "Блокування успішно встановлено/знято";}dio_close($fd);?> `

### Примітки

> **Примітка**: Для Windows-платформ ця функція не реалізована.
