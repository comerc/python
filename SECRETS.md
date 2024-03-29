- Оператор возведения в степень (`**`) является правоассоциативным (значение выражения вычисляется справа налево) в соответствии с правилами математики. Таким образом, выражение `x ** y ** z` вычисляется как `x ** (y ** z)`.
- Операторы `//` и `%` имеют такой же приоритет, как и операторы умножения и обычного деления.
- Наивысший приоритет имеет оператор возведения в степень `**`.
- `num=17; a=num%10; b=num//10; print(a,b) # 7 1`
- `num=754; a=num%10; b=(num%100)//10; c=num//100; print(a,b,c) # 4 5 7`
- Строки (но не переменные) могут быть объединены без использования '`+`': `"Привет " "мир!"`
- Эквивалент тернарного оператора '`?:`' в C: `"да!" if 0 > 1 else "нет!"`
- Операторы сравнения в Python можно объединять в цепочки (в отличии от большинства других языков программирования, где для этого нужно использовать логические связки), например, `a == b == c` или `1 <= x <= 10`.
- Операция равенства является транзитивной. Это означает, что если `a == b` и `b == c`, то из этого следует, что `a == c`.
- Операция неравенства (`!=`), в отличие от операции равенства (`==`), является нетранзитивной. То есть из того, что `a != b` и `b != c`,вовсе не следует, что `a != c`.
- Приоритеты логических операторов: `not`, `and`, `or`
- Для удобного чтения чисел можно использовать символ подчеркивания: `num1 = 25_000_000`
- Можно умножать строку на число: `s = 'Hi' * 4; print(s) # HiHiHiHi`
- Для извлечения квадратного корня можно воспользоваться кодом `n ** 0.5`, вместо `math.sqrt(n)`.
- Умножение и деление имеют одинаковый приоритет, поэтому они выполняются слева направо.
- Python: `for v in range(10)` VS GoLang: `for v := range [10]int{}`
- `True` & `False` - булевы литералы с большой буквы
- Python допускает необязательный блок `else` в конце циклов `while` и `for`. Если внутри цикла прерывание по `break`, то блок `else` не выполняется.
- В отличие от многих языков программирования, в Python есть возможность работы с отрицательными индексами. Если первый символ строки имеет индекс `0`, то последнему элементу присваивается индекс `-1`.
- Итерирование строк: `for c in s: print(c)`
- В Python строки являются неизменяемыми.
- Как вывести строку в обратном порядке: `s = 'abc'; print(s[::-1])`
- Список может содержать значения разных типов данных: `info = ['Timur', 1992, 61.5]`
- Кортеж может содержать значения разных типов данных: `info = ('Timur', 1992, 61.5)`
- Обратите внимание, что кортежи неизменяемы, что означает, что мы не можем изменять, добавлять или удалять элементы после создания кортежа. Это отличает их от списков в Python, которые являются изменяемыми.
- Срез `numbers[:]` возвращает копию исходного списка.
- строки — неизменяемые объекты, а списки – изменяемые
- Оператор `del` работает и со срезами: мы можем удалить целый диапазон элементов списка. `del numbers[2:7]  # удаляем элементы с 2 по 6 включительно`
- Распаковка списка: `numbers = [0, 1, 2, 3, 4, 5, 6]; print(*numbers, sep='\n')`
- Как создать список, заполненный нулями: `zeros = [0] * 10`
- Как создать список, где каждый элемент - индекс: `l = list(range(3))`
- Как работает join: `words = ['Hello', 'world']; s = ' '.join(words)`
- Существует большая разница между результатами вызова методов `s.split()` и `s.split(' ')`.
- Строковый метод `join()` работает только со списком строк. Иначе ошибка.
- Существует большая разница между вызовом метода `names.reverse()` и использованием среза `names[::-1]`. Метод `reverse()` меняет порядок элементов на обратный в текущем списке, а срез создает копию списка, в котором элементы следуют в обратном порядке.
- list comprehension: `numbers = [i for i in range(10)]`
- Объявление функции должно предшествовать ее вызову.
- Заглушка функции: `def do_nothing(): pass`
- Аргумент – это любая порция данных, которая передается в функцию, когда функция вызывается. Параметр – это переменная, которая получает аргумент, переданный в функцию.
- `global x` разрешает отсылаться к глобальной переменной внутри текущей области видимости.
- Функция может возвращать несколько значений: `return a, b, c`
- приоритет оператора `not` выше, чем у оператора `and`, приоритет которого, в свою очередь, выше, чем у оператора `or`.
- Поскольку `True` равно `1`, а `False` равно `0`, сложение логических значений вместе – это быстрый способ подсчета количества значений `True`.
- Операторы `and` и `or` ленивые.
- В программировании функция, которая возвращает значение `True` или `False`, называется предикатом.
- При проверке типов обычно вместо функции `type()` используется функция `isinstance()`, так как она принимает во внимание иерархию типов (ООП).
- Для сравнения переменной с `None` всегда используйте оператор `is`. Для встроенных типов поведение `is` и `==` абсолютно одинаково, однако с пользовательскими типами могут возникнуть проблемы, так как в Python есть возможность переопределения операторов сравнения в пользовательских типах.
- Значение `None` не отождествляется с значениями `0`, `False`, `''`.
- При использовании срезов со списками мы также можем опускать второй параметр в срезе `numbers[x:]` (но поставить двоеточие), тогда срез берется до конца списка. Аналогично если опустить первый параметр `numbers[:y]`, то можно взять срез от начала списка (невключительно).
- `numbers.pop(2)` удалит элемент по индексу: `[10, 20, 30, 40]` -> `[10, 20, 40]`
- `numbers.pop()` удалит последний элемент: `[10, 20, 30, 40]` -> `[10, 20, 30]`
- `del` удалит диапазон: `numbers = [10, 20, 30, 40]; del numbers[1:-1] # [10, 40]`
- как заменить диапазон: `numbers = [10, 20, 30, 40]; numbers[1:-1] = [21, 31] # [10, 21, 31, 40]`
- Индексы `i` и `j` элементов на главной диагонали связаны соотношением `i = j`. Индексы `i` и `j` элементов на побочной диагонали связаны соотношением `i + j + 1 = n` (или `j = n - i - 1`), где `n` — размерность матрицы.
- как заполнить переменные элементами списка: `x, y = list(input())`
- как заполнить переменные элементами списка: `n, m = map(int, input().split())`
- Одну матрицу можно умножать на другую только тогда, когда количество столбцов в первой матрице совпадает с количеством строк во второй матрице.
- Функции, возвращающие несколько значений - возвращают именно кортежи.
- Срез кортежа остаётся кортежем (а не трансформируется в список).
- Кантор определял множество как "любое собрание определенных и различимых между собой объектов нашей интуиции или интеллекта, мыслимое как единое целое".
- Создать пустое множество с помощью пустых фигурных скобок нельзя (зарезервировано на словари), только через `set()`.
- множество - изменяемый тип, но элементы множества должны быть неизменяемыми
- Оператор принадлежности `in` работает очень быстро на множествах – намного быстрее, чем на списках. Поэтому если требуется часто осуществлять поиск в коллекции уникальных данных, то множество – подходящий выбор.
- Обратите внимание на то, что функция `sorted(set_v, reverse)` возвращает отсортированный список, а не множество. Не путайте встроенную функцию `sorted()` и списочный метод `sort()`. Множества не содержат метода `sort()`.
- [методы множеств и соответствующие им операторы](./assets/set-methods.png) следующие: `union() |` (or), `intersection() &` (and), `difference() -` (не является коммутативной операцией), `symmetric_difference() ^` (xor)
- Кортеж (тип `tuple`) – неизменяемая версия списка (тип `list`), а замороженное множество (тип `frozenset`) – неизменяемая версия обычного множества (тип `set`).
- Начиная с версии Python 3.6, словари являются упорядоченными, то есть сохраняют порядок следования ключей в порядке их внесения в словарь.
- Словарные методы `items()`, `keys()`, `values()` возвращают не совсем обычные списки. Типы этих списков - `dict_items`, `dict_keys`, `dict_values` соответственно, в отличие от обычных списков `list`. Методы обычных списков недоступны для списков типа `dict_items`, `dict_keys`, `dict_values`. Используйте явное преобразование с помощью функции `list()` для получения доступа к методам списков.
- В Python 3.9 появились операторы `|` и `|=`, которые реализуют операцию конкатенации словарей (в дополнение к методу словаря `update()`)
- Удобные константы:
```py
print(string.ascii_letters)
print(string.ascii_uppercase)
print(string.ascii_lowercase)
print(string.digits)
print(string.hexdigits)
print(string.octdigits)
print(string.punctuation)
print(string.printable)
```
- неверно создавать `decimal` числа из `float`, например: `print(Decimal(0.1)) # 0.100000000000000005`
- Создать `Fraction` число можно несколькими способами:
  - из целых чисел, передав значения числителя и знаменателя дроби,
  - из строки на основании десятичного представления;
  - из строки на основании обыкновенной дроби;
  - из числа с плавающей точкой (не рекомендуется).
- Мнимая единица i обладает интересным свойством: каждый раз при умножении на i она "циклически" проходит через 4 различных значения:
  - `1 * i = i`
  - `i * i = -1`
  - `-1 * i = -i`
  - `-i * i = 1`
- Значение по умолчанию для параметра создается единожды при определении функции (обычно при загрузке модуля) и становится атрибутом (свойством) функции. Поэтому, если значение по умолчанию изменяемый объект, то его изменение повлияет на каждый следующий вызов функции. 
```py
print(append(10)) # [10]
print(append(5)) # [10, 5]
print(append(1)) # [10, 5, 1]
```
- Для решения проблемы можно использовать константу None в качестве значения параметра по умолчанию (общепринятый подход), а в теле функции устанавливать нужное значение: 
```py
def append(element, seq=None):
    if seq is None:
        seq = []
    seq.append(element)
    return seq
```
- Термин «аргумент» подразумевает, что конкретно и какой конкретной функции было передано, а «параметр» — в каком качестве функция применила это принятое. То есть вызывающий код передает аргумент в параметр, который определен в описании (заголовке) функции.
- Параметр `args` в определении функции пишется после позиционных параметров перед первым параметром со значением по умолчанию.
- По соглашению, параметр, получающий подобный кортеж значений, принято называть `args` (от слова arguments).
- По соглашению параметр, получающий подобный словарь, принято называть `kwargs` (от словосочетания keyword arguments).
- Параметр `*args` применяется между позиционными параметрами и параметра со значением по умолчанию; а параметр `**kwargs` применяется в самом конце, после последнего параметра со значением по умолчанию. При этом функция может содержать и `*args` и `**kwargs` параметры: `def my_func(a, b, *args, name='Gvido', age=17, **kwargs):`.
- Замыкания – вложенные функции, ссылающиеся на переменные, объявленные вне определения этой функции, и не являющиеся её параметрами.
- Функции `max()` и `min()` возвращают первый максимальный или минимальный элемент, если таковых несколько.
- Встроенной функции `filter()` можно в качестве первого параметра `func` передать значение `None`. В таком случае каждый элемент последовательности будет проверен на соответствие значению `True`. Если элемент в логическом контексте возвращает значение `False`, то он не будет добавлен в возвращаемый результат.
- `data = ['год', 'дело', 'день', 'рука', 'раз', 'лицо', 'друг', 'глаз', 'дом', 'мир', 'сила', 'вид']; print(*sorted(data, key=lambda v: (len(v), v)))` - в лямбду можно запихнуть кортеж, чтобы сначала сортировал по длине, а потом по лексикографическом порядке
- Если переданный итерируемый объект пустой, то функция `all()` возвращает значение `True`. Но: `print(all([[], []])) # False`.
- Вместо экранирования символов можно использовать сырые строки (raw strings). Для этого следует снабдить строковый литерал префиксом в виде буквы r. Например: `test_file = open(r'C:\Users\temp\test.txt', 'w')`
- Построчное чтение файла:
```py
file = open('languages.txt', 'r', encoding='utf-8')
for line in file:
    print(line.rstrip())
file.close()
```