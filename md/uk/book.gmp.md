Обчислення над цілими числами з довільною точністю (GNU Multiple Precision)

-   [« bcsub](function.bcsub.html)
    
-   [Введение »](intro.gmp.html)
    
-   [PHP Manual](index.html)
    
-   [Математичні модулі](refs.math.html)
    
-   Обчислення над цілими числами з довільною точністю (GNU Multiple Precision)
    

# Обчислення над цілими числами з довільною точністю (GNU Multiple Precision)

-   [Введение](intro.gmp.html)
-   [Установка и настройка](gmp.setup.html)
    -   [Требования](gmp.requirements.html)
    -   [Установка](gmp.installation.html)
    -   [Настройка во время выполнения](gmp.configuration.html)
-   [Предопределённые константы](gmp.constants.html)
-   [Примеры](gmp.examples.html)
-   [GMP Функції](ref.gmp.html)
    -   [gmpabs](function.gmp-abs.html) - Абсолютна величина
    -   [gmpadd](function.gmp-add.html) - Додавання чисел
    -   [gmpand](function.gmp-and.html) - Побітове І
    -   [gmpbinomial](function.gmp-binomial.html) - Обчислює біноміальний коефіцієнт
    -   [gmpclrbit](function.gmp-clrbit.html) - Скидання біта
    -   [gmpcmp](function.gmp-cmp.html) - Порівняння чисел
    -   [gmpcom](function.gmp-com.html) - Обчислює доповнення до одиниці числа
    -   [gmpdivдо](function.gmp-div-q.html) - Розподіл чисел
    -   [gmpdivгр](function.gmp-div-qr.html) — Поділ чисел та отримання приватного та залишку
    -   [gmpdivр](function.gmp-div-r.html) — Залишок від поділу чисел
    -   [gmpdiv](function.gmp-div.html) - Псевдонім gmpdivдо
    -   [gmpdivexact](function.gmp-divexact.html) - Розподіл чисел без залишку
    -   [gmpexport](function.gmp-export.html) — Експортувати до бінарного рядка
    -   [gmpfact](function.gmp-fact.html) - Факторіал
    -   [gmpgcd](function.gmp-gcd.html) - Обчислення найбільшого спільного дільника
    -   [gmpgcdext](function.gmp-gcdext.html) — Обчислення НОД та множників
    -   [gmphamdist](function.gmp-hamdist.html) - Відстань Хеммінга
    -   [gmpimport](function.gmp-import.html) — Імпортувати з бінарного рядка
    -   [gmpinit](function.gmp-init.html) - Створення GMP числа
    -   [gmpintval](function.gmp-intval.html) — Перетворення числа GMP на ціле число
    -   [gmpinvert](function.gmp-invert.html) - Інверсія залишку від поділу
    -   [gmpjacobi](function.gmp-jacobi.html) - Символ Якобі
    -   [gmpkronecker](function.gmp-kronecker.html) - Символ Кронекера - Якобі
    -   [gmplcm](function.gmp-lcm.html) — Вираховує найменше загальне кратне
    -   [gmplegendre](function.gmp-legendre.html) - Символ Лежандра
    -   [gmpmod](function.gmp-mod.html) — Обчислення залишку від цілого розподілу
    -   [gmpmul](function.gmp-mul.html) — Збільшення чисел
    -   [gmpneg](function.gmp-neg.html) - Зміна знака числа
    -   [gmpnextprime](function.gmp-nextprime.html) - Пошук наступного простого числа
    -   [gmpор](function.gmp-or.html) - Побітове АБО
    -   [gmpperfectpower](function.gmp-perfect-power.html) — Перевірити, чи є число "досконалим ступенем"
    -   [gmpperfectsquare](function.gmp-perfect-square.html) - Перевірка числа на точний квадрат
    -   [gmppopcount](function.gmp-popcount.html) — Кількість одиниць у двійковому записі числа
    -   [gmppow](function.gmp-pow.html) — Зводить число до ступеня
    -   [gmppowm](function.gmp-powm.html) - Зводить число в ступінь і виробляє розподіл за модулем
    -   [gmpprobprime](function.gmp-prob-prime.html) - Перевіряє, чи є число "ймовірно простим"
    -   [gmprandombits](function.gmp-random-bits.html) - Випадкове число
    -   [gmprandomrange](function.gmp-random-range.html) - Випадкове число
    -   [gmprandomseed](function.gmp-random-seed.html) - Встановити початковий стан RNG
    -   [gmprandom](function.gmp-random.html) - Випадкове число
    -   [gmproot](function.gmp-root.html) - Витягти корінь ступеня N і повернути його цілу частину
    -   [gmprootrem](function.gmp-rootrem.html) - Витягти корінь ступеня N і повернути його цілу частину і залишок
    -   [gmpscan0](function.gmp-scan0.html) - Пошук нуля в числі
    -   [gmpscan1](function.gmp-scan1.html) - Пошук одиниці в числі
    -   [gmpsetbit](function.gmp-setbit.html) - Встановлення біта
    -   [gmpsign](function.gmp-sign.html) - Знак числа
    -   [gmpsqrt](function.gmp-sqrt.html) - Обчислення квадратного кореня
    -   [gmpsqrtrem](function.gmp-sqrtrem.html) - Квадратний корінь із залишком
    -   [gmpstrval](function.gmp-strval.html) — Перетворення GMP числа в рядок
    -   [gmpsub](function.gmp-sub.html) — Віднімання чисел
    -   [gmptestbit](function.gmp-testbit.html) - Перевірка, чи встановлений біт в 1
    -   [gmpxor](function.gmp-xor.html) — Побітове, що виключає АБО
-   [GMP](class.gmp.html) - Клас GMP
    -   [GMP::serialize](gmp.serialize.html) - Серіалізує об'єкт GMP
    -   [GMP::unserialize](gmp.unserialize.html) — Десеріалізує параметр data в об'єкті GMP