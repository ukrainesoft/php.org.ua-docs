- [«imagecreatefromgd2part](function.imagecreatefromgd2part.md)
- [imagecreatefromgif]](function.imagecreatefromgif.md)

- [PHP Manual](index.md)
- [Функції GD та функції для роботи із зображеннями](ref.image.md)
- Створення нового зображення на основі GD файлу або URL

#imagecreatefromgd

(PHP 4 \>= 4.0.7, PHP 5, PHP 7, PHP 8)

imagecreatefromgd — Створення нового зображення на основі файлу GD або
URL

### Опис

**imagecreatefromgd**(string `$filename`):
[GdImage](class.gdimage.md)\|false

Створення нового зображення на основі файлу GD або URL.

**Підказка**

Для цієї функції ви можете використовувати URL як ім'я файлу, якщо
була включена опція [fopen wrappers](filesystem.configuration.md#ini.allow-url-fopen). Дивіться
докладнішу інформацію про визначення імені файлу в описі функції
[fopen()](function.fopen.md). Дивіться також список підтримуваних
оберток URL, їх можливості, зауваження щодо використання та список
визначених констант у розділі [Підтримувані протоколи та обертки](wrappers.md).

### Список параметрів

`filename`
Шлях до файлу GD.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання або
**`false`** у разі виникнення помилки.

### Список змін

| Версія | Опис                                                                                                                           |
| ------ | ------------------------------------------------------------------------------------------------------------------------------ |
| 8.0.0  | У разі успішного виконання, функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagecreatefromgd()****

` <?php// завантаження зображення$im = @imagecreatefromgd('./test.gd');// перевірка, завантажилося або зображенняif(!$im){     die('Не удалося завантажити } Операції з зображенням можна здійснити тут// Збереження зображенняimagegd($im, './test_updated.gd');imagedestroy($im);?> `

### Примітки

**Увага**

Формати зображень GD та GD2 є пропрієтарними форматами
зображень libgd. Вони повинні розглядатися як застарілі і повинні
використовуватися тільки з метою розробки та тестування.
