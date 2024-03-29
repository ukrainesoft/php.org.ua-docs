---
navigation:
  - security.cgi-bin.force-redirect.md: 'Варіант 2: використання cgi.force\_redirect'
  - security.cgi-bin.shell.md: 'Варіант 4: PHP поза деревом веб-документів »'
  - index.md: PHP Manual
  - security.cgi-bin.md: Якщо PHP встановлено як CGI
title: 'Варіант 3: використання опцій doc\_root або user\_dir'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Варіант 3: використання опцій doc\_root або user\_dir

Розміщення динамічного контенту, такого як скрипти або інших виконуваних файлів, в директорії веб-сервера робить його потенційно небезпечним. У випадку, якщо в конфігурації сервера допущена помилка, можлива ситуація, коли скрипти не виконуються, а відображаються у браузері, як звичайні HTML-документи, що може призвести до витоку конфіденційної інформації (наприклад, паролів) або інформації, що є інтелектуальною власністю. Виходячи з таких міркувань, багато системних адміністраторів вважають за краще використовувати для зберігання скриптів окрему директорію, працюючи з усіма розміщеними в ній файлами за CGI-інтерфейсом.

Якщо неможливо гарантувати, що запити не перенаправляються, як було показано в попередньому розділі, необхідно вказувати змінну doc\_root, яка відрізняється від кореневої директорії веб-документів.

Ви можете встановити кореневу директорію для PHP-скриптів, налаштувавши параметр [doc\_root](ini.core.md#ini.doc-root)в[конфігураційному файлі](configuration.file.md), або встановивши змінну оточення PHP\_DOCUMENT\_ROOT. У випадку, якщо PHP використовується за допомогою CGI, повний шлях до файлу, що відкривається, буде побудований на підставі значення змінної `doc_root` та зазначеного у запиті шляху. Таким чином, ви можете бути впевнені, що скрипти будуть виконуватися тільки всередині вказаної директорії (крім директорії `user_dir`, Яка описана нижче).

Ще одна опція, що використовується при налаштуванні безпеки - [user\_dir](ini.core.md#ini.user-dir). Якщо змінна user\_dir не встановлена, шлях до файлу, що відкривається, будується відносно `doc_root`. Запит виду [http://my.host/~user/doc.php](http://my.host/~user/doc.php) призводить до виконання скрипта, що знаходиться не в домашньому каталозі відповідного користувача, а що знаходиться в підкаталозі doc\_root скрипта~user/doc.php (так, ім'я директорії починається з символу \`~\`).

Але якщо user\_dir встановлена, наприклад, значення public\_php, то запит виду [http://my.host/~user/doc.php](http://my.host/~user/doc.php) відкриє файл doc.php, що знаходиться в домашньому каталозі користувача, в директорії public\_php. Наприклад, якщо домашній каталог користувача /home/user, буде виконано файл /home/user/public\_php/doc.php.

Установка опции`user_dir`происходит независимо от установки`doc_root`, таким чином ви можете контролювати кореневу директорію веб-сервера та користувальницькі директорії незалежно один від одного.
