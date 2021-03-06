- [« Варіант 2: використання cgi.force_redirect](security.cgi-bin.force-redirect.md)
- [Варіант 4: PHP поза деревом веб-документів »](security.cgi-bin.shell.md)

- [PHP Manual](index.md)
- [Якщо PHP встановлено як CGI](security.cgi-bin.md)
- Варіант 3: використання опцій doc_root чи user_dir

## Варіант 3: використання опцій doc_root або user_dir

Розміщення динамічного контенту, такого як скрипти або будь-які інші
виконуваних файлів, у директорії веб-сервера робить його потенційно
небезпечним. Якщо у конфігурації сервера припущена помилка, можлива
ситуація, коли скрипти не виконуються, а відображаються у браузері, як
звичайні HTML-документи, що може призвести до витоку конфіденційної
інформації (наприклад, паролів), або інформації, що є
інтелектуальною власністю. Виходячи з таких міркувань, багато хто
системні адміністратори вважають за краще використовувати для зберігання скриптів
окрему директорію, працюючи з усіма розміщеними в ній файлами по
CGI-інтерфейс.

Якщо неможливо гарантувати, що запити не
перенаправляються, як було показано в попередньому розділі, необхідно
вказувати змінну doc_root, яка відрізняється від кореневої директорії
веб-документи.

Ви можете встановити кореневу директорію для PHP-скриптів, настроївши
параметр [doc_root](ini.core.md#ini.doc-root) у [конфігураційному файлі](configuration.file.md), або встановивши змінну оточення
`PHP_DOCUMENT_ROOT`. Якщо PHP використовується за допомогою CGI,
повний шлях до файлу, що відкривається, буде побудований на підставі значення
змінної `doc_root` та вказаної у запиті шляху. таким чином, ви
можете бути впевнені, що скрипти будуть виконуватись лише всередині
вказаної вами директорії (крім директорії `user_dir`, яка описана
нижче).

Ще одна опція, що використовується при налаштуванні безпеки -
[user_dir](ini.core.md#ini.user-dir). Якщо змінна
user_dir не встановлена, шлях до файлу, що відкривається, будується відносно
`doc_root`. Запит виду `http://my.host/~user/doc.php` призводить до
виконання скрипта, що знаходиться не в домашньому каталозі відповідного
користувача, а скрипта, що знаходиться в підкаталозі doc_root
`~user/doc.php` (так, ім'я директорії починається з символу `~`).

Але якщо user_dir встановлена, наприклад, значення "public_php", то
запит виду `http://my.host/~user/doc.php` відкриє файл `doc.php`,
що знаходиться в домашньому каталозі користувача, в директорії `public_php`.
Наприклад, якщо домашній каталог користувача `/home/user`, буде
виконано файл `/home/user/public_php/doc.php`.

Встановлення опції `user_dir` відбувається незалежно від установки
`doc_root`, таким чином ви можете контролювати кореневу директорію
веб-сервера та власні директорії незалежно один від одного.
