- [« Приклади](shmop.examples.md)
- [Поділ, що розділяється (shared) пам'ять »](ref.shmop.md)

- [PHP Manual](index.md)
- [Приклади](shmop.examples.md)
- Базове використання

## Базове використання

**Приклад #1 Огляд операцій з пам'яттю, що розділяється**

` <?php// Создание блока с идентификатором 0xff3 и размером в 100 байт.$shm_id = shmop_open(0xff3, "c", 0644, 100);if (!$shm_id) {    echo "Невозможно зарезервировать блок в сегменте памяти
";}// Отримання розміру блоку в розділеної пам'яті$shm_size = shmop_size($shm_id);echo "Ділянка пам'яті, розміром: " . $shm_size . . |
";// Проверочная запись некоторой строки в разделяемую память$shm_bytes_written = shmop_write($shm_id, "Мой маленький блок", 0);if ($shm_bytes_written != strlen("Мой маленький блок")) {    echo "Не удалось записать весь розмір даних
";}// Отримання збереженої рядки з розділеної пам'яті$my_string = shmop_read($shm_id, 0, $shm_size);if (!$my_string) {    echo "Неможливо  
";}echo "Дані, розміщені в поділеної пам'яті: " . $my_string . "
";// Видалення блоку і закриття сегменту поділеної пам'ятіif (!shmop_delete($shm_id)) {    echo "Неможливо відмітити ділянку пам'яті для з$|
