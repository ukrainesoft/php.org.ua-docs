---
navigation:
  - function.ob-iconv-handler.md: « ob\_iconv\_handler
  - intro.intl.md: Вступ "
  - index.md: PHP Manual
  - refs.international.md: Підтримка мов та кодувань
title: Функції інтернаціоналізації
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Функції інтернаціоналізації

-   [Вступ](intro.intl.md)
-   [Встановлення та налаштування](intl.setup.md)
    -   [Вимоги](intl.requirements.md)
    -   [Установка](intl.installation.md)
    -   [Налаштування під час виконання](intl.configuration.md)
    -   [Типи ресурсів](intl.resources.md)
-   [Обумовлені константи](intl.constants.md)
-   [Приклади](intl.examples.md)
    -   [Основи використання модуля](intl.examples.basic.md)
-   [Collator](class.collator.md) \- Клас Collator
    -   [Collator::asort](collator.asort.md)— Сортує масив із збереженням асоціації індексу
    -   [Collator::compare](collator.compare.md)— Порівнює два рядки Unicode
    -   [Collator::\_\_construct](collator.construct.md) \- Створює новий екземпляр Collator
    -   [Collator::create](collator.create.md) \- Створює новий екземпляр Collator
    -   [Collator::getAttribute](collator.getattribute.md)— Отримує значення атрибуту зіставлення
    -   [Collator::getErrorCode](collator.geterrorcode.md)— Отримує останній код помилки Collator
    -   [Collator::getErrorMessage](collator.geterrormessage.md)— Отримує текст для останньої помилки коду Collator
    -   [Collator::getLocale](collator.getlocale.md) \- Отримує назву локалі для Collator
    -   [Collator::getSortKey](collator.getsortkey.md)— Отримує ключ сортування рядка
    -   [Collator::getStrength](collator.getstrength.md)— Отримує поточну силу зіставлення
    -   [Collator::setAttribute](collator.setattribute.md) \- Встановлює атрибут зіставлення
    -   [Collator::setStrength](collator.setstrength.md) \- Встановлює силу зіставлення
    -   [Collator::sortWithSortKeys](collator.sortwithsortkeys.md)— Сортує масив із використанням зазначеного Collator та ключів сортування
    -   [Collator::sort](collator.sort.md)— Сортує масив із використанням зазначеного засобу сортування
-   [NumberFormatter](class.numberformatter.md)— The NumberFormatter class
    -   [NumberFormatter::create](numberformatter.create.md)— Створює засіб форматування чисел
    -   [NumberFormatter::formatCurrency](numberformatter.formatcurrency.md) \- Форматує значення валюти
    -   [NumberFormatter::format](numberformatter.format.md) \- Форматує число
    -   [NumberFormatter::getAttribute](numberformatter.getattribute.md)— Отримує атрибут
    -   [NumberFormatter::getErrorCode](numberformatter.geterrorcode.md)— Отримує останній код помилки засобу форматування
    -   [NumberFormatter::getErrorMessage](numberformatter.geterrormessage.md)— Отримує останнє повідомлення про помилку засобу форматування
    -   [NumberFormatter::getLocale](numberformatter.getlocale.md)— Отримує локаль засобу форматування
    -   [NumberFormatter::getPattern](numberformatter.getpattern.md)— Отримує шаблон засобу форматування
    -   [NumberFormatter::getSymbol](numberformatter.getsymbol.md)— Отримує значення символу
    -   [NumberFormatter::getTextAttribute](numberformatter.gettextattribute.md)— Отримує текстовий атрибут
    -   [NumberFormatter::parseCurrency](numberformatter.parsecurrency.md) \- Розбирає номер валюти
    -   [NumberFormatter::parse](numberformatter.parse.md) \- Розбирає число
    -   [NumberFormatter::setAttribute](numberformatter.setattribute.md) \- Встановлює атрибут
    -   [NumberFormatter::setPattern](numberformatter.setpattern.md)— Встановлює шаблон засобу форматування
    -   [NumberFormatter::setSymbol](numberformatter.setsymbol.md)— Встановлює значення символу
    -   [NumberFormatter::setTextAttribute](numberformatter.settextattribute.md) \- Встановлює текстовий атрибут
-   [Locale](class.locale.md) \- Клас Locale
    -   [Locale::acceptFromHttp](locale.acceptfromhttp.md) — Спробувати визначити найкращу локаль на основі заголовку HTTP "Accept-Language"
    -   [Locale::canonicalize](locale.canonicalize.md) \- Канонізувати рядок локалі
    -   [Locale::composeLocale](locale.composelocale.md)— Повертає коректно відсортовані та розділені ідентифікатори локалі
    -   [Locale::filterMatches](locale.filtermatches.md)— Перевірити, чи тег фільтра мови локалі відповідає
    -   [Locale::getAllVariants](locale.getallvariants.md)— Отримання варіантів із переданої локалі
    -   [Locale::getDefault](locale.getdefault.md) — Отримання значення локалі INTL за замовчуванням із опції 'default\_locale'
    -   [Locale::getDisplayLanguage](locale.getdisplaylanguage.md)— Повертає відповідним чином локалізоване ім'я мови для заданої локалі
    -   [Locale::getDisplayName](locale.getdisplayname.md) \- Повертає відповідним чином локалізоване ім'я локалі
    -   [Locale::getDisplayRegion](locale.getdisplayregion.md)— Повертає відповідним чином локалізовану назву регіону для заданої локалі
    -   [Locale::getDisplayScript](locale.getdisplayscript.md)— Повертає відповідним чином локалізовану назву алфавіту для заданої локалі
    -   [Locale::getDisplayVariant](locale.getdisplayvariant.md)— Повертає відповідним чином локалізовану назву варіанта для заданої локалі
    -   [Locale::getKeywords](locale.getkeywords.md)— Отримати ключові слова для локалі
    -   [Locale::getPrimaryLanguage](locale.getprimarylanguage.md)— Отримати первинну мову для локалі
    -   [Locale::getRegion](locale.getregion.md)— Отримати регіон для локалі
    -   [Locale::getScript](locale.getscript.md) \- Отримати алфавіт для локалі
    -   [Locale::lookup](locale.lookup.md)— Пошук мовних позначок найбільш відповідних заданої локалі
    -   [Locale::parseLocale](locale.parselocale.md)— Здобути асоціативний масив усіх підтегів локалі
    -   [Locale::setDefault](locale.setdefault.md)— Встановити локаль за умовчанням під час виконання
-   [Normalizer](class.normalizer.md) \- Клас Normalizer
    -   [Normalizer::getRawDecomposition](normalizer.getrawdecomposition.md)— Витягує властивість Decomposition\_Mapping для заданого символу UTF-8
    -   [Normalizer::isNormalized](normalizer.isnormalized.md)— Перевірити, чи переданий рядок відповідає заданій формі нормалізації
    -   [Normalizer::normalize](normalizer.normalize.md) \- Нормалізація рядка
-   [MessageFormatter](class.messageformatter.md) \- Клас MessageFormatter
    -   [MessageFormatter::create](messageformatter.create.md)— Створює засіб форматування повідомлень
    -   [MessageFormatter::formatMessage](messageformatter.formatmessage.md)— Швидко форматує повідомлення
    -   [MessageFormatter::format](messageformatter.format.md)— Форматує повідомлення
    -   [MessageFormatter::getErrorCode](messageformatter.geterrorcode.md)— Повертає код помилки останньої операції
    -   [MessageFormatter::getErrorMessage](messageformatter.geterrormessage.md)— Повертає текст помилки останньої операції
    -   [MessageFormatter::getLocale](messageformatter.getlocale.md)— Повертає локаль, для якої було створено засіб форматування
    -   [MessageFormatter::getPattern](messageformatter.getpattern.md)— Повертає шаблон, який використовує засіб форматування
    -   [MessageFormatter::parseMessage](messageformatter.parsemessage.md)— Швидко розбирає вхідний рядок
    -   [MessageFormatter::parse](messageformatter.parse.md)— Розбирає рядок згідно з шаблоном
    -   [MessageFormatter::setPattern](messageformatter.setpattern.md)— Встановлює шаблон, який використовує засіб форматування
-   [IntlCalendar](class.intlcalendar.md) \- Клас IntlCalendar
    -   [IntlCalendar::add](intlcalendar.add.md) \- Додає кількість (зі знаком) часу в полі
    -   [IntlCalendar::after](intlcalendar.after.md) \- Визначає, час цього об'єкта пізніше часу переданого об'єкта
    -   [IntlCalendar::before](intlcalendar.before.md)— Визначає, час цього об'єкта раніше переданого об'єкта
    -   [IntlCalendar::clear](intlcalendar.clear.md)— Очищає поле чи всі поля
    -   [IntlCalendar::\_\_construct](intlcalendar.construct.md)— Закритий конструктор для заборони створення екземплярів
    -   [IntlCalendar::createInstance](intlcalendar.createinstance.md)— Створює новий об'єкт IntlCalendar
    -   [IntlCalendar::equals](intlcalendar.equals.md)— Порівнює час двох об'єктів IntlCalendar щодо рівності
    -   [IntlCalendar::fieldDifference](intlcalendar.fielddifference.md)— Обчислює різницю між заданим часом та часом об'єкта
    -   [IntlCalendar::fromDateTime](intlcalendar.fromdatetime.md)— Створює IntlCalendar з об'єкта чи рядка DateTime
    -   [IntlCalendar::get](intlcalendar.get.md)— Отримує значення поля
    -   [IntlCalendar::getActualMaximum](intlcalendar.getactualmaximum.md)— Максимальне значення для поля з урахуванням поточного часу об'єкта
    -   [IntlCalendar::getActualMinimum](intlcalendar.getactualminimum.md)— Мінімальне значення для поля з урахуванням поточного часу об'єкта
    -   [IntlCalendar::getAvailableLocales](intlcalendar.getavailablelocales.md)— Отримує масив мовних стандартів, для яких є дані
    -   [IntlCalendar::getDayOfWeekType](intlcalendar.getdayofweektype.md)— Повідомляє, чи є день буднім, вихідним чи днем ​​із переходом між ними
    -   [IntlCalendar::getErrorCode](intlcalendar.geterrorcode.md)— Отримує останній код помилки об'єкта
    -   [IntlCalendar::getErrorMessage](intlcalendar.geterrormessage.md)— Отримує останнє повідомлення про помилку об'єкта
    -   [IntlCalendar::getFirstDayOfWeek](intlcalendar.getfirstdayofweek.md)— отримує перший день тижня для мовного стандарту календаря
    -   [IntlCalendar::getGreatestMinimum](intlcalendar.getgreatestminimum.md)— Отримує найбільше локальне мінімальне значення поля
    -   [IntlCalendar::getKeywordValuesForLocale](intlcalendar.getkeywordvaluesforlocale.md)— Набір значень ключових слів мовного стандарту
    -   [IntlCalendar::getLeastMaximum](intlcalendar.getleastmaximum.md)— Отримує найменший локальний максимум для поля
    -   [IntlCalendar::getLocale](intlcalendar.getlocale.md)— Отримує мовний стандарт, пов'язаний із об'єктом
    -   [IntlCalendar::getMaximum](intlcalendar.getmaximum.md)— Отримує глобальне максимальне значення поля
    -   [IntlCalendar::getMinimalDaysInFirstWeek](intlcalendar.getminimaldaysinfirstweek.md)— Отримує мінімальну кількість днів, яка може бути у першому тижні на рік чи місяць
    -   [IntlCalendar::getMinimum](intlcalendar.getminimum.md)— Отримує глобальне мінімальне значення поля
    -   [IntlCalendar::getNow](intlcalendar.getnow.md)— Отримує число, що становить поточний час
    -   [IntlCalendar::getRepeatedWallTimeOption](intlcalendar.getrepeatedwalltimeoption.md)— Отримує поведінку для обробки часу процесора, що повторюється.
    -   [IntlCalendar::getSkippedWallTimeOption](intlcalendar.getskippedwalltimeoption.md)— Отримує поведінку для обробки пропущеного часу процесора
    -   [IntlCalendar::getTime](intlcalendar.gettime.md)— Отримує час, представлений на даний момент об'єктом
    -   [IntlCalendar::getTimeZone](intlcalendar.gettimezone.md)— Отримує часовий пояс об'єкту
    -   [IntlCalendar::getType](intlcalendar.gettype.md)— Отримує тип календаря
    -   [IntlCalendar::getWeekendTransition](intlcalendar.getweekendtransition.md)— Отримує час, коли вихідні починаються або закінчуються.
    -   [IntlCalendar::inDaylightTime](intlcalendar.indaylighttime.md)— Визначає, чи час об'єкта переходить на літній час.
    -   [IntlCalendar::isEquivalentTo](intlcalendar.isequivalentto.md)— Визначає, чи дорівнює інший календар, але для іншого часу
    -   [IntlCalendar::isLenient](intlcalendar.islenient.md)— Визначає, чи інтерпретація дати/часу є м'якою.
    -   [IntlCalendar::isSet](intlcalendar.isset.md)— Визначає, чи встановлено поле
    -   [IntlCalendar::isWeekend](intlcalendar.isweekend.md)— Визначає, чи доводиться певна дата/час на вихідні
    -   [IntlCalendar::roll](intlcalendar.roll.md)— Додає значення в поле без перенесення до найважливіших полів
    -   [IntlCalendar::set](intlcalendar.set.md)— Встановлює поле часу або одразу кілька спільних полів
    -   [IntlCalendar::setDate](intlcalendar.setdate.md) \- Встановлює поля дати
    -   [IntlCalendar::setDateTime](intlcalendar.setdatetime.md)— Встановлює поля дати та часу
    -   [IntlCalendar::setFirstDayOfWeek](intlcalendar.setfirstdayofweek.md)— Встановлює день, який є початком тижня
    -   [IntlCalendar::setLenient](intlcalendar.setlenient.md)— Встановлює, чи інтерпретація дати/часу повинна бути м'якою.
    -   [IntlCalendar::setMinimalDaysInFirstWeek](intlcalendar.setminimaldaysinfirstweek.md)— Встановлює мінімальну кількість днів, яка може бути у першому тижні на рік чи місяць
    -   [IntlCalendar::setRepeatedWallTimeOption](intlcalendar.setrepeatedwalltimeoption.md)— Встановлює поведінку для обробки часу процесора, що повторюється, при негативних переходах зміщення часового поясу.
    -   [IntlCalendar::setSkippedWallTimeOption](intlcalendar.setskippedwalltimeoption.md)— Встановлює поведінку для обробки пропущеного часу процесора при позитивних переходах усунення часового поясу
    -   [IntlCalendar::setTime](intlcalendar.settime.md)— Встановлює календарний час у мілісекундах від початку епохи Unix
    -   [IntlCalendar::setTimeZone](intlcalendar.settimezone.md)— Встановлює часовий пояс, який використовується календарем.
    -   [IntlCalendar::toDateTime](intlcalendar.todatetime.md)— Перетворює об'єкт IntlCalendar на об'єкт DateTime
-   [IntlGregorianCalendar](class.intlgregoriancalendar.md) \- Клас IntlGregorianCalendar
    -   [IntlGregorianCalendar::\_\_construct](intlgregoriancalendar.construct.md) \- Конструктор класу григоріанського календаря
    -   [IntlGregorianCalendar::createFromDate](intlgregoriancalendar.createfromdate.md)— Створює новий екземпляр Intel GregorianCalendar із дати
    -   [IntlGregorianCalendar::createFromDateTime](intlgregoriancalendar.createfromdatetime.md)— Створює новий екземпляр Intel GregorianCalendar із дати та часу
    -   [IntlGregorianCalendar::getGregorianChange](intlgregoriancalendar.getgregorianchange.md)— Отримує дату зміни григоріанського календаря
    -   [IntlGregorianCalendar::isLeapYear](intlgregoriancalendar.isleapyear.md)— Визначає, чи цей рік є високосним.
    -   [IntlGregorianCalendar::setGregorianChange](intlgregoriancalendar.setgregorianchange.md)— Встановлює дату зміни у григоріанському календарі
-   [IntlTimeZone](class.intltimezone.md)— Клас IntlTimeZone
    -   [IntlTimeZone::\_\_construct](intltimezone.construct.md) \- Конструктор класу, який забороняє пряме створення екземпляра
    -   [IntlTimeZone::countEquivalentIDs](intltimezone.countequivalentids.md)— Отримати кількість ідентифікаторів у групі схожих часових поясів, включаючи цей ідентифікатор
    -   [IntlTimeZone::createDefault](intltimezone.createdefault.md)— Створити нову копію часового поясу за промовчанням для поточного хоста
    -   [IntlTimeZone::createEnumeration](intltimezone.createenumeration.md)— Отримати перерахування з ідентифікаторів часових поясів за вказаною країною або усунення
    -   [IntlTimeZone::createTimeZone](intltimezone.createtimezone.md)— Створити об'єкт часового поясу по заданому ідентифікатору
    -   [IntlTimeZone::createTimeZoneIDEnumeration](intltimezone.createtimezoneidenumeration.md)— Отримати перерахування з ідентифікаторів системних часових поясів за умовами фільтрації
    -   [IntlTimeZone::fromDateTimeZone](intltimezone.fromdatetimezone.md)— Створити об'єкт часового поясу з DateTimeZone
    -   [IntlTimeZone::getCanonicalID](intltimezone.getcanonicalid.md)— Отримати канонічний системний ідентифікатор часового поясу або нормалізований ідентифікатор часового поясу по заданому ідентифікатору часового поясу
    -   [IntlTimeZone::getDisplayName](intltimezone.getdisplayname.md)— Отримати ім'я часового поясу для відображення користувача
    -   [IntlTimeZone::getDSTSavings](intltimezone.getdstsavings.md)— Отримати кількість мілісекунд, яку потрібно додати до місцевого поясного часу, щоб отримати літній час
    -   [IntlTimeZone::getEquivalentID](intltimezone.getequivalentid.md)— Отримати ідентифікатор у групі схожих часових поясів, включаючи заданий ідентифікатор
    -   [IntlTimeZone::getErrorCode](intltimezone.geterrorcode.md)— Отримати останній код про помилку в об'єкті
    -   [IntlTimeZone::getErrorMessage](intltimezone.geterrormessage.md)— Отримати останнє повідомлення про помилку в об'єкті
    -   [IntlTimeZone::getGMT](intltimezone.getgmt.md)— Створити часовий пояс GMT (UTC)
    -   [IntlTimeZone::getID](intltimezone.getid.md)— Отримати ідентифікатор часового поясу
    -   [IntlTimeZone::getIDForWindowsID](intltimezone.getidforwindowsid.md)— Перетворити часовий пояс для Windows на системний часовий пояс
    -   [IntlTimeZone::getOffset](intltimezone.getoffset.md)— Отримати необроблене значення часового поясу та усунення за Грінвічем (GMT) за заданим моментом часу
    -   [IntlTimeZone::getRawOffset](intltimezone.getrawoffset.md)— Отримати необроблене значення зсуву за Грінвічем (GMT) без урахування літнього часу
    -   [IntlTimeZone::getRegion](intltimezone.getregion.md)— Отримати код регіону, який відповідає заданому ідентифікатору системного часового поясу
    -   [IntlTimeZone::getTZDataVersion](intltimezone.gettzdataversion.md)— Отримати версію даних про часовий пояс, який зараз використовується в ICU
    -   [IntlTimeZone::getUnknown](intltimezone.getunknown.md)— Отримати невідомий часовий пояс (unknown)
    -   [IntlTimeZone::getWindowsID](intltimezone.getwindowsid.md)— Перетворити часовий пояс на часовий пояс для Windows
    -   [IntlTimeZone::hasSameRules](intltimezone.hassamerules.md)— Перевірити, що в іншому часовому поясі використовуються ті самі правила та усунення, що й у першому заданому
    -   [IntlTimeZone::toDateTimeZone](intltimezone.todatetimezone.md)— Перетворити на об'єкт DateTimeZone
    -   [IntlTimeZone::useDaylightTime](intltimezone.usedaylighttime.md)— Перевірити, що в даному часовому поясі використовується літній час
-   [IntlDateFormatter](class.intldateformatter.md) \- Клас IntlDateFormatter
    -   [IntlDateFormatter::create](intldateformatter.create.md)— Створює засіб форматування дати
    -   [IntlDateFormatter::format](intldateformatter.format.md)— Форматує значення дати/часу у вигляді рядка
    -   [IntlDateFormatter::formatObject](intldateformatter.formatobject.md) \- Форматує об'єкт
    -   [IntlDateFormatter::getCalendar](intldateformatter.getcalendar.md)— Отримує тип календаря для об'єкта IntlDateFormatter
    -   [IntlDateFormatter::getDateType](intldateformatter.getdatetype.md)— Отримує тип дати, який використовується IntlDateFormatter
    -   [IntlDateFormatter::getErrorCode](intldateformatter.geterrorcode.md)— Отримує код помилки останньої операції
    -   [IntlDateFormatter::getErrorMessage](intldateformatter.geterrormessage.md)— Отримує текст помилки останньої операції
    -   [IntlDateFormatter::getLocale](intldateformatter.getlocale.md)— Отримує мовний стандарт, який використовується засобом форматування
    -   [IntlDateFormatter::getPattern](intldateformatter.getpattern.md)— Отримує шаблон, який використовується IntlDateFormatter
    -   [IntlDateFormatter::getTimeType](intldateformatter.gettimetype.md)— Отримує тип часу, який використовується IntlDateFormatter
    -   [IntlDateFormatter::getTimeZoneId](intldateformatter.gettimezoneid.md)— Отримує ідентифікатор часового поясу, який використовується IntlDateFormatter
    -   [IntlDateFormatter::getCalendarObject](intldateformatter.getcalendarobject.md)— Отримує копію об'єкта календаря засобу форматування
    -   [IntlDateFormatter::getTimeZone](intldateformatter.gettimezone.md)— Отримує часовий пояс засобу форматування
    -   [IntlDateFormatter::isLenient](intldateformatter.islenient.md)— Отримує поблажливість, яка використовується для IntlDateFormatter
    -   [IntlDateFormatter::localtime](intldateformatter.localtime.md)— Перетворює рядок на значення часу на основі поля
    -   [IntlDateFormatter::parse](intldateformatter.parse.md)— Перетворює рядок на значення позначки часу
    -   [IntlDateFormatter::setCalendar](intldateformatter.setcalendar.md)— Встановлює тип календаря за допомогою форматування.
    -   [IntlDateFormatter::setLenient](intldateformatter.setlenient.md) \- Встановлює м'який режим аналізатора
    -   [IntlDateFormatter::setPattern](intldateformatter.setpattern.md)— Встановлює шаблон, який використовується IntlDateFormatter
    -   [IntlDateFormatter::setTimeZone](intldateformatter.settimezone.md)— Встановлює часовий пояс засобу форматування
-   [ResourceBundle](class.resourcebundle.md) \- Клас ResourceBundle
    -   [ResourceBundle::count](resourcebundle.count.md)— Отримати кількість елементів у пакеті
    -   [ResourceBundle::create](resourcebundle.create.md) \- Створити пакет ресурсів
    -   [ResourceBundle::getErrorCode](resourcebundle.geterrorcode.md)— Отримати останній код помилки пакета
    -   [ResourceBundle::getErrorMessage](resourcebundle.geterrormessage.md)— Отримати останнє повідомлення про помилку пакета
    -   [ResourceBundle::get](resourcebundle.get.md)— Отримати дані з пакета
    -   [ResourceBundle::getLocales](resourcebundle.locales.md)— Отримати підтримувані локалі
-   [Spoofchecker](class.spoofchecker.md) \- Клас Spoofchecker
    -   [Spoofchecker::areConfusable](spoofchecker.areconfusable.md)— Перевірити, чи є рядки підозрілими
    -   [Spoofchecker::\_\_construct](spoofchecker.construct.md) \- Конструктор класу
    -   [Spoofchecker::isSuspicious](spoofchecker.issuspicious.md)— Перевіряє, чи текст містить підозрілі символи
    -   [Spoofchecker::setAllowedLocales](spoofchecker.setallowedlocales.md)— Локаль для використання у перевірках
    -   [Spoofchecker::setChecks](spoofchecker.setchecks.md)— Встановити набір перевірок
    -   [Spoofchecker::setRestrictionLevel](spoofchecker.setrestrictionlevel.md) \- Встановлює рівень обмеження
-   [Transliterator](class.transliterator.md) \- Клас Transliterator
    -   [Transliterator::\_\_construct](transliterator.construct.md) \- Приватний конструктор
    -   [Transliterator::create](transliterator.create.md) \- Створити транслітератор
    -   [Transliterator::createFromRules](transliterator.createfromrules.md) \- Створити транслітератор на основі правил
    -   [Transliterator::createInverse](transliterator.createinverse.md) \- Створити інвертований транслітератор
    -   [Transliterator::getErrorCode](transliterator.geterrorcode.md)— Отримати код останньої помилки
    -   [Transliterator::getErrorMessage](transliterator.geterrormessage.md)— Отримати останнє повідомлення про помилку
    -   [Transliterator::listIDs](transliterator.listids.md)— Отримати ідентифікатори транслітератора
    -   [Transliterator::transliterate](transliterator.transliterate.md)— Транслітерувати рядок
-   [IntlBreakIterator](class.intlbreakiterator.md) \- Клас IntlBreakIterator
    -   [IntlBreakIterator::\_\_construct](intlbreakiterator.construct.md)— Закритий конструктор, який забороняє створення екземплярів об'єкту
    -   [IntlBreakIterator::createCharacterInstance](intlbreakiterator.createcharacterinstance.md)— Створює ітератор переривання меж комбінування послідовностей символів.
    -   [IntlBreakIterator::createCodePointInstance](intlbreakiterator.createcodepointinstance.md)— Створює ітератор переривання меж кодових точок.
    -   [IntlBreakIterator::createLineInstance](intlbreakiterator.createlineinstance.md)— Створює ітератор переривання для логічно можливих розривів рядків
    -   [IntlBreakIterator::createSentenceInstance](intlbreakiterator.createsentenceinstance.md) \- Створює ітератор переривання для розривів речень
    -   [IntlBreakIterator::createTitleInstance](intlbreakiterator.createtitleinstance.md) \- Створює ітератор переривання для розривів заголовків
    -   [IntlBreakIterator::createWordInstance](intlbreakiterator.createwordinstance.md) \- Створює ітератор переривання для розривів слів
    -   [IntlBreakIterator::current](intlbreakiterator.current.md)— Повертає індекс поточної позиції
    -   [IntlBreakIterator::first](intlbreakiterator.first.md)— Встановлює позицію першого символу в тексті
    -   [IntlBreakIterator::following](intlbreakiterator.following.md)— Переміщає ітератор до першого кордону після вказаного усунення
    -   [IntlBreakIterator::getErrorCode](intlbreakiterator.geterrorcode.md)— Повертає останній код помилки об'єкту
    -   [IntlBreakIterator::getErrorMessage](intlbreakiterator.geterrormessage.md)— Повертає останнє повідомлення про помилку об'єкта
    -   [IntlBreakIterator::getLocale](intlbreakiterator.getlocale.md)— Повертає локаль, пов'язану з об'єктом
    -   [IntlBreakIterator::getPartsIterator](intlbreakiterator.getpartsiterator.md)— створює ітератор для переміщення фрагментів між кордонами.
    -   [IntlBreakIterator::getText](intlbreakiterator.gettext.md)— Повертає текст, що сканується.
    -   [IntlBreakIterator::isBoundary](intlbreakiterator.isboundary.md)— Повідомляє, чи є усунення зміщенням кордону
    -   [IntlBreakIterator::last](intlbreakiterator.last.md)— Встановлює позицію ітератора до індексу за останнім символом
    -   [IntlBreakIterator::next](intlbreakiterator.next.md)— Переміщує ітератор до наступного кордону
    -   [IntlBreakIterator::preceding](intlbreakiterator.preceding.md)— Встановлює позицію ітератора до першого кордону перед усуненням
    -   [IntlBreakIterator::previous](intlbreakiterator.previous.md)— Встановлює позицію ітератора на кордоні безпосередньо перед поточною
    -   [IntlBreakIterator::setText](intlbreakiterator.settext.md)— Встановлює сканований текст
-   [IntlRuleBasedBreakIterator](class.intlrulebasedbreakiterator.md)— Клас IntlRuleBasedBreakIterator
    -   [IntlRuleBasedBreakIterator::\_\_construct](intlrulebasedbreakiterator.construct.md) \- Створює ітератор на основі набору правил
    -   [IntlRuleBasedBreakIterator::getBinaryRules](intlrulebasedbreakiterator.getbinaryrules.md)— Отримати бінарні дані зі скомпілованих правил
    -   [IntlRuleBasedBreakIterator::getRules](intlrulebasedbreakiterator.getrules.md)— Отримати набір правил, які використовуються під час створення цього об'єкта
    -   [IntlRuleBasedBreakIterator::getRuleStatus](intlrulebasedbreakiterator.getrulestatus.md)— Отримати найбільше значення статусу правил зупинки, що визначило поточну позицію зупинки
    -   [IntlRuleBasedBreakIterator::getRuleStatusVec](intlrulebasedbreakiterator.getrulestatusvec.md)— отримати значення статусів із правил зупинки, які визначили поточну позицію зупинки
-   [IntlCodePointBreakIterator](class.intlcodepointbreakiterator.md)— Клас IntlCodePointBreakIterator
    -   [IntlCodePointBreakIterator::getLastCodePoint](intlcodepointbreakiterator.getlastcodepoint.md)— Отримати останній код символу, виданий під час переміщення ітератора вперед або назад
-   [IntlDatePatternGenerator](class.intldatepatterngenerator.md) \- Клас IntlDatePatternGenerator
    -   [IntlDatePatternGenerator::create](intldatepatterngenerator.create.md)— Створює новий екземпляр IntlDatePatternGenerator
    -   [IntlDatePatternGenerator::getBestPattern](intldatepatterngenerator.getbestpattern.md)— Визначає найбільш підходящий формат дати/часу
-   [IntlPartsIterator](class.intlpartsiterator.md) \- Клас IntlPartsIterator
    -   [IntlPartsIterator::getBreakIterator](intlpartsiterator.getbreakiterator.md)— Отримати IntlBreakIterator, зберігаючи ітератор цієї частини
-   [UConverter](class.uconverter.md) \- Клас UConverter
    -   [UConverter::\_\_construct](uconverter.construct.md)— Створити об'єкт UConverter
    -   [UConverter::convert](uconverter.convert.md)— Конвертувати рядок з одного кодування в інше
    -   [UConverter::fromUCallback](uconverter.fromucallback.md) — Callback-функція за промовчанням для "from"
    -   [UConverter::getAliases](uconverter.getaliases.md)— Отримати псевдоніми для цього імені
    -   [UConverter::getAvailable](uconverter.getavailable.md)— Отримати доступні імена канонічних конверторів
    -   [UConverter::getDestinationEncoding](uconverter.getdestinationencoding.md)— Отримати кодування призначення
    -   [UConverter::getDestinationType](uconverter.getdestinationtype.md)— Отримати тип конвертера призначення
    -   [UConverter::getErrorCode](uconverter.geterrorcode.md)— Отримати код останньої помилки об'єкта
    -   [UConverter::getErrorMessage](uconverter.geterrormessage.md)— Отримати останнє повідомлення про помилку в об'єкті
    -   [UConverter::getSourceEncoding](uconverter.getsourceencoding.md)— Отримати вихідне кодування
    -   [UConverter::getSourceType](uconverter.getsourcetype.md)— Отримати тип конвертера джерела
    -   [UConverter::getStandards](uconverter.getstandards.md)— Отримати стандарти, пов'язані з іменами конвертерів
    -   [UConverter::getSubstChars](uconverter.getsubstchars.md)— Отримати заміну символів
    -   [UConverter::reasonText](uconverter.reasontext.md)— Отримати рядкове подання причини зворотного виклику
    -   [UConverter::setDestinationEncoding](uconverter.setdestinationencoding.md)— Встановити кодування призначення
    -   [UConverter::setSourceEncoding](uconverter.setsourceencoding.md)— Встановити вихідне кодування
    -   [UConverter::setSubstChars](uconverter.setsubstchars.md)— Встановлення символів підстановки
    -   [UConverter::toUCallback](uconverter.toucallback.md) - Callback-функція за промовчанням для "to"
    -   [UConverter::transcode](uconverter.transcode.md)— Перетворює рядок з одного кодування символів на інший
-   [Функції Grapheme](ref.intl.grapheme.md)
    -   [grapheme\_extract](function.grapheme-extract.md)— Функція для вилучення послідовності кластерів за замовчуванням графем з текстового буфера, яка повинна бути закодована в UTF-8
    -   [grapheme\_stripos](function.grapheme-stripos.md)— Знаходить позицію (в одиницях графеми) першої появи рядка без урахування регістру
    -   [grapheme\_stristr](function.grapheme-stristr.md)— Повертає частину рядка haystack від першої появи needle без урахування регістру до кінця haystack
    -   [grapheme\_strlen](function.grapheme-strlen.md)— Отримує довжину рядка в одиницях графеми
    -   [grapheme\_strpos](function.grapheme-strpos.md) \- Знаходить позицію (в одиницях графеми) першого входження рядка
    -   [grapheme\_strripos](function.grapheme-strripos.md)— Знаходить позицію (в одиницях графеми) останнього входження рядка без урахування регістру
    -   [grapheme\_strrpos](function.grapheme-strrpos.md)— Знаходить позицію (в одиницях графеми) останнього входження рядка
    -   [grapheme\_strstr](function.grapheme-strstr.md)— Повертає частину рядка haystack від першої появи needle до кінця haystack
    -   [grapheme\_substr](function.grapheme-substr.md)— Повертає частину рядка
-   [Функції IDN](ref.intl.idn.md)
    -   [idn\_to\_ascii](function.idn-to-ascii.md)— Перетворює доменне ім'я на формат IDNA ASCII
    -   [idn\_to\_utf8](function.idn-to-utf8.md)— Перетворення доменного імені з IDNA ASCII на Unicode
-   [IntlChar](class.intlchar.md)
    -   [IntlChar::charAge](intlchar.charage.md) — Отримати "вік" символьного коду
    -   [IntlChar::charDigitValue](intlchar.chardigitvalue.md)— Отримати десяткову цифру із символу десяткової цифри
    -   [IntlChar::charDirection](intlchar.chardirection.md)— Отримати категорію напряму листа для символу
    -   [IntlChar::charFromName](intlchar.charfromname.md)— Знайти символ Unicode на його ім'я та повернути його код
    -   [IntlChar::charMirror](intlchar.charmirror.md) — Отримати "дзеркальний" символ за кодом
    -   [IntlChar::charName](intlchar.charname.md)— Отримати ім'я Unicode
    -   [IntlChar::charType](intlchar.chartype.md)— Отримати головну категорію, до якої входить символ
    -   [IntlChar::chr](intlchar.chr.md)— Отримати символ Unicode за його кодом
    -   [IntlChar::digit](intlchar.digit.md)— Отримати десяткове число із символу Unicode із заданою основою
    -   [IntlChar::enumCharNames](intlchar.enumcharnames.md)— Перелічує всі присвоєні символи Unicode у заданому діапазоні
    -   [IntlChar::enumCharTypes](intlchar.enumchartypes.md)— Перелік послідовностей символів Unicode згрупованих за ними.
    -   [IntlChar::foldCase](intlchar.foldcase.md)— Перетворює регістр заданого символу.
    -   [IntlChar::forDigit](intlchar.fordigit.md)— Отримати символ, який представляє задане число в заданій основі
    -   [IntlChar::getBidiPairedBracket](intlchar.getbidipairedbracket.md)— Отримати парну дужку для символу
    -   [IntlChar::getBlockCode](intlchar.getblockcode.md)— Отримати блок розміщення символу Unicode
    -   [IntlChar::getCombiningClass](intlchar.getcombiningclass.md)— Отримати комбінуючий клас для символу
    -   [IntlChar::getFC\_NFKC\_Closure](intlchar.getfc-nfkc-closure.md) \- Отримати властивість FC\_NFKC\_Closure для символу
    -   [IntlChar::getIntPropertyMaxValue](intlchar.getintpropertymaxvalue.md)— Отримати мінімальне значення для властивості Unicode
    -   [IntlChar::getIntPropertyMinValue](intlchar.getintpropertyminvalue.md)— Отримати мінімальне значення для властивості Unicode
    -   [IntlChar::getIntPropertyValue](intlchar.getintpropertyvalue.md)— Отримати значення властивості Unicode для символу
    -   [IntlChar::getNumericValue](intlchar.getnumericvalue.md)— Отримати числову виставу для символу Unicode
    -   [IntlChar::getPropertyEnum](intlchar.getpropertyenum.md)— Отримати значення константи властивості на його ім'я
    -   [IntlChar::getPropertyName](intlchar.getpropertyname.md) \- Отримати Unicode ім'я властивості
    -   [IntlChar::getPropertyValueEnum](intlchar.getpropertyvalueenum.md)— Повернути числовий ідентифікатор властивості на його ім'я
    -   [IntlChar::getPropertyValueName](intlchar.getpropertyvaluename.md)— Отримати ім'я Unicode для значення властивості
    -   [IntlChar::getUnicodeVersion](intlchar.getunicodeversion.md)— Отримати версію Unicode
    -   [IntlChar::hasBinaryProperty](intlchar.hasbinaryproperty.md)— Перевірити бінарну властивість Unicode для символу
    -   [IntlChar::isalnum](intlchar.isalnum.md)— Перевірити, чи є символ буквою чи цифрою
    -   [IntlChar::isalpha](intlchar.isalpha.md)— Перевірити, чи є символ літерою
    -   [IntlChar::isbase](intlchar.isbase.md)— Перевірити, чи символ є базовим
    -   [IntlChar::isblank](intlchar.isblank.md) - Перевірити, чи є символ "порожнім" або "горизонтальним пропуском"
    -   [IntlChar::iscntrl](intlchar.iscntrl.md)— Перевірити, чи є символ керуючим
    -   [IntlChar::isdefined](intlchar.isdefined.md)— Перевірити, чи є символ.
    -   [IntlChar::isdigit](intlchar.isdigit.md)— Перевірити, чи символ є цифрою
    -   [IntlChar::isgraph](intlchar.isgraph.md)— Перевірити, чи є символом графічним символом
    -   [IntlChar::isIDIgnorable](intlchar.isidignorable.md)— Перевірити, чи символ ігнорується
    -   [IntlChar::isIDPart](intlchar.isidpart.md)— Перевірити, чи можна використовувати символ в ідентифікаторі
    -   [IntlChar::isIDStart](intlchar.isidstart.md)— Перевірити, чи можна використовувати символ на початку ідентифікатора
    -   [IntlChar::isISOControl](intlchar.isisocontrol.md)— Перевірити, чи є символ керуючим відповідно до ISO
    -   [IntlChar::isJavaIDPart](intlchar.isjavaidpart.md)— Перевірити, чи символ допустимий в ідентифікаторі Java
    -   [IntlChar::isJavaIDStart](intlchar.isjavaidstart.md)— Перевірити, чи символ може бути першим в ідентифікаторі Java
    -   [IntlChar::isJavaSpaceChar](intlchar.isjavaspacechar.md)— Перевірити, чи є символ пробельним з точки зору Java
    -   [IntlChar::islower](intlchar.islower.md)— Перевірити, чи у нижньому регістрі символ
    -   [IntlChar::isMirrored](intlchar.ismirrored.md)— Перевірити, якщо символ має властивість Bidi\_Mirrored
    -   [IntlChar::isprint](intlchar.isprint.md)— Перевіряє, чи символ відображається.
    -   [IntlChar::ispunct](intlchar.ispunct.md)— Перевіряє, чи є символом пунктуації.
    -   [IntlChar::isspace](intlchar.isspace.md)— Перевіряє, чи символ є пробельним.
    -   [IntlChar::istitle](intlchar.istitle.md)— Перевірити, чи символ є титульним (Titlecase)
    -   [IntlChar::isUAlphabetic](intlchar.isualphabetic.md)— Перевірити, чи встановлено символ символу Alphabetic
    -   [IntlChar::isULowercase](intlchar.isulowercase.md)— Перевірити, чи символ є символом у нижньому регістрі
    -   [IntlChar::isupper](intlchar.isupper.md) — Перевірити, чи входить символ у категорію "Lu" (літера у верхньому регістрі)
    -   [IntlChar::isUUppercase](intlchar.isuuppercase.md)— Перевірити, чи символ є символом у верхньому регістрі
    -   [IntlChar::isUWhiteSpace](intlchar.isuwhitespace.md)— Перевірити, чи має символ властивість White\_Space (пробіловий символ)
    -   [IntlChar::isWhitespace](intlchar.iswhitespace.md)— Перевірити, чи символ є пробільним з точки зору ICU
    -   [IntlChar::isxdigit](intlchar.isxdigit.md)— Перевіряє, чи кодова точка відноситься до шістнадцяткової цифри.
    -   [IntlChar::ord](intlchar.ord.md)— Отримати код символ Unicode
    -   [IntlChar::tolower](intlchar.tolower.md)— Перетворює символ Unicode на нижній регістр
    -   [IntlChar::totitle](intlchar.totitle.md)— Перетворює символ Unicode на титульний регістр (titlecase)
    -   [IntlChar::toupper](intlchar.toupper.md)— Перетворює символ Unicode у верхній регістр
-   [IntlException](class.intlexception.md)— Клас винятків для помилок intl
-   [IntlIterator](class.intliterator.md) \- Клас IntlIterator
    -   [IntlIterator::current](intliterator.current.md)— Отримати поточний елемент
    -   [IntlIterator::key](intliterator.key.md)— Отримати ключ поточного елемента
    -   [IntlIterator::next](intliterator.next.md)— Перейти до наступного елементу
    -   [IntlIterator::rewind](intliterator.rewind.md)— Перейти до першого елементу
    -   [IntlIterator::valid](intliterator.valid.md)— Перевірити, чи поточна позиція коректна
-   [Функції intl](ref.intl.md)
    -   [intl\_error\_name](function.intl-error-name.md)— Отримати ім'я помилки за її кодом
    -   [intl\_get\_error\_code](function.intl-get-error-code.md)— Отримати код останньої помилки
    -   [intl\_get\_error\_message](function.intl-get-error-message.md)— Отримати опис помилки
    -   [intl\_is\_failure](function.intl-is-failure.md)— Перевірити, чи є код помилки ознакою збою
