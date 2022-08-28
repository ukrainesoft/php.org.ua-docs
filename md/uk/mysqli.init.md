Ініціалізує MySQLi та повертає об'єкт для використання у функції mysqlirealconnect()

-   [« mysqli::$info](mysqli.info.html)
    
-   [mysqli::$insert\_id »](mysqli.insert-id.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Ініціалізує MySQLi та повертає об'єкт для використання у функції mysqlirealconnect()
    

# mysqli::init

# mysqliinit

(PHP 5, PHP 7, PHP 8)

mysqli::init -- mysqliinit — Ініціалізує MySQLi та повертає об'єкт для використання у функції mysqlirealconnect()

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::init(): ?bool
```

Процедурний стиль

```methodsynopsis
mysqli_init(): mysqli|false
```

Виділяє пам'ять або ініціалізує об'єкт MySQL, придатний для використання у функціях [mysqli\_options()](mysqli.options.html)

> **Зауваження**
> 
> Будь-які подальші виклики mysqli-функцій із цим ресурсом (крім [mysqli\_options()](mysqli.options.html)) зазнають невдачі, доки не буде викликана функція [mysqli\_real\_connect()](mysqli.real-connect.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Метод **mysqli::init()** повертає **`null`** у разі успішного виконання або **`false`** у разі виникнення помилки. Функція **mysqliinit()** повертає об'єкт у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Об'єктно-орієнтований стиль виклику методу **mysqli::init()** застарів. Замініть виклик методу **parent::init()** за допомогою **parent::construct()** |

### Приклади

Дивіться [mysqli\_real\_connect()](mysqli.real-connect.html)

### Дивіться також

-   [mysqli\_options()](mysqli.options.html) - Встановлення налаштувань
-   [mysqli\_close()](mysqli.close.html) - Закриває раніше відкрите з'єднання з базою даних
-   [mysqli\_real\_connect()](mysqli.real-connect.html) - Встановлює з'єднання із сервером mysql
-   [mysqli\_connect()](function.mysqli-connect.html) - Псевдонім mysqli::construct