- [«Зумовлені константи](bzip2.constants.md)
- [Функції Bzip2 »](ref.bzip2.md)

- [PHP Manual](index.md)
- [Bzip2](book.bzip2.md)
- Приклади

# Приклади

Наступний приклад відкриє тимчасовий файл, запише до нього тестовий рядок,
після чого виведе вміст файлу.

**Приклад #1 Приклад роботи з bzip2**

;bzclose($bz);?> `` <?php$filename = "/tmp/testfile.bz2";$str = "This is a test string.
";// відкриваємо файл для запису$bz = bzopen($filename, "w");// пишеморядок в файлbzwrite($bz, $str);// закриваємо файлbzclose(  $bz = bzopen($filename, "r");// читаємо 10 символівecho bzread($bz, 10);// виводимо все, до кінця| 
