- [« Історія PHP](history.php.md)
- [Книги про PHP »](history.php.books.md)

- [PHP Manual](index.md)
- [Історія PHP та суміжних проектів](history.md)
- Історія суміжних з PHP проектів

## Історія суміжних з PHP проектів

### PEAR

[»PEAR](https://pear.php.net/)
(`PHP Extension and Application Repository` - Репозиторій Додатків
та Модуль PHP. Спочатку, PHP Extension and Add-on Repository -
Репозиторій Доповнень і Модуль PHP) - це PHP-версія базових класів.
У майбутньому можливе його зростання та становлення ключовим способом публікації
модулів PHP серед розробників

PEAR зародився під час дискусій на зустрічі розробників PHP (PHP
Developers' Meeting - PDM), що проходила в січні 2000 року в Тель-Авіві.
Автором PEAR є Стіг С. Баккен (Stig S. Bakken), який присвятив
розробку своєї першої дочки, Мелін Баккен (Malin Bakken).

З початку 2000 року PEAR виріс до величезного проекту з великою кількістю
розробників, які працюють над реалізацією загального та повторного
використовуваного функціоналу на благо для всієї спільноти PHP. В даний
час PEAR включає широкий спектр класів для роботи з базами
даних, кешування контенту, математичних обчислень, електронної
комерції та багато іншого.

Додаткову інформацію про PEAR можна знайти в
[»Документації](https://pear.php.net/manual/).

### Ініціатива Гарантії Якості PHP

Група [» Ініціативи Гарантії Якості PHP](https://qa.php.net/) була
заснована навесні 2000 у відповідь на критику недостатнього бета-тестування
PHP для виробничого оточення. Зараз ця група складається з людей,
чудово розуміють основу коду PHP. Ці розробники витрачають безліч
часу на виявлення та усунення помилок у PHP. Крім того, багато
інших членів команди тестують ці виправлення та повідомляють про результати
їх роботи на різних платформах.

### PHP-GTK

[» PHP-GTK](http://gtk.php.net/) є модулем PHP для написання
GUI-додатків, що працюють на стороні клієнта. Андрій Зміївський (Andrei
Zmievski) згадує процес планування та розробки PHP-GTK:

> Я завжди цікавився GUI-програмуванням, і я знаходжу Gtk+ дуже
> приємним засобом розробки, за винятком того, що працювати з ним на C
> трохи втомлює. Після перегляду PyGtk та GTK-Perl, я вирішив
> спробувати написати інтерфейс PHP для роботи з Gtk+, хай з
> мінімальними можливостями. Починаючи з серпня 2000 року, у мене
> з'явилося трохи більше вільного часу, і я почав експерименти. В
> розробці я базувався на PyGtk, який має великий
> кількістю можливостей та приємною об'єктно-орієнтованою
> інтерфейсом. Джеймс Хенстридж (James Henstridge), автор PyGtk, давав
> дуже корисні поради протягом перших етапів розробки.
>
> Написання вручну інтерфейсів до всіх функцій Gtk+ навіть не
> розглядалося. Я зупинився на ідеї генератора коду, схожого на
> аналогічний генератор PyGtk. Генератор читає `.defs` файли,
> що містять інформацію про класи, константи та методи Gtk+ та
> генерує C-код, що є інтерфейсом PHP. Те, що не могло бути
> згенеровано автоматично, створюється вручну в `.overrides` файлах.
>
> Робота над генератором коду та самою інфраструктурою йшла достатньо
> довго, зважаючи на те, що я не мав достатньо вільного часу для
> роботи. Після того, як я показав PHP-GTK Френку Кромману (Frank
> Kromman), він зацікавився і почав допомагати мені з генератором коду та
> версією Win32. Коли ми написали та запустили першу програму
> Hello World це було дуже захоплююче. Потрібно було кілька
> місяців для надання PHP-GTK презентабельного вигляду та перша версія
> вийшла 1 березня 2001 року. Історія швидко потрапила до SlashDot.
>
> Відчуючи, що PHP-GTK може зростати, я створив окремі поштові
> конференції, CVS-репозиторій, а також сайт gtk.php.net за допомогою
> Коліна Вієброка (Colin Viebrock). Була потрібна документація і тут на
> допомога прийшов Джеймс Мур (James Moore).
>
> З часів створення PHP-GTK отримав широку популярність. У нас є
> своя група документування люди починають писати модулі для PHP-GTK
> і все більше і більше прекрасних програм з його допомогою.
