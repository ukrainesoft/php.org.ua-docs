- [«dio_read](function.dio-read.md)
- [dio_stat »](function.dio-stat.md)

- [PHP Manual](index.md)
- [Функції прямого введення/виводу](ref.dio.md)
- Перемістити вказівник у файловому дескрипторі

#dio_seek

(PHP 4 \>= 4.2.0, PHP 5 \< 5.1.0)

dio_seek — Перемістити вказівник у файловий дескриптор

### Опис

**dio_seek**(resource `$fd`, int `$pos`, int `$whence` = SEEK_SET): int

Функція **dio_seek()** використовується для зміни вказівника всередині
файлу.

### Список параметрів

`fd`
Файловий дескриптор, отриманий із [dio_open()](function.dio-open.md).

`pos`
нова позиція.

`whence`
Вказує, як треба інтерпретувати `pos`:

- **`SEEK_SET`** (за замовчуванням) - вказує, що `pos` відраховується
від початку файлу.

- **`SEEK_CUR`** - вказує, що `pos` відраховується від поточної
позиції. Можливо негативним.

- **`SEEK_END`** - вказує, що `pos` відраховується від кінця файлу.
Негативне число визначає позицію всередині поточного файлу;
позитивна кількість визначає позицію після поточного кінця. Якщо ви
вкажіть позицію за межами поточного кінця файлу та почнете запис,
то шматок файлу, що бракує, буде заповнений нулями.

### Значення, що повертаються

### Приклади

**Приклад #1 Позиціонування всередині файлу**

` <?php$fd =dio_open('/dev/ttyS0', O_RDWR);dio_seek($fd, 10, SEEK_SET);// Поточна позиція - 10 байт від початкуdio_seek(2$ Текущая позиция - 8 байт от началаdio_seek($fd, -5, SEEK_END);// Текущая позиция - 5 байт от концаdio_seek($fd, 10, SEEK_END);// Текущая позиция - 10 байт дальше конца файла// 10 байт от кінця файла до поточної позиції заповнені нулямиdio_close($fd);?> `
