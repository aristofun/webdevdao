# Задачи на собеседованиях

1. **Тыры-пыры, она же foo-bar**. Напишите программу, которая выводит на экран числа от 1 до 100. При этом вместо чисел, кратных 3, программа должна выводить слово «Hi», а вместо чисел, кратных 5 — слово «By». Если число кратно и 3, и 5, то программа должна выводить слово «HiBy».
1. Имеется строка набранная в разном регистре, например: «ВотТакаяСтрока» требуется получить в результате строку где буквы меняют регистр, то есть: «вОТтАКАЯсТРОКА». Напишите, пожалуйста, код.
1. Дана строка `s` и словарь `dict` , содержащий некие слова. Определите, можно ли строку `s` сегментировать в последовательность разделенных пробелом слов, содержащихся в словаре `dict`.

    Пример: дано, `s` = «двадесятка», `dict` = [«два», «десятка», «девятка»]. Программа должна вернуть `true`, потому что «двадесятка» могут быть сементированы как «два десятка».

1. Найдите непрерывный подмассив в массиве (содержащем как минимум 1 элемент), который имеет максимальную сумму элементов.

    Пример: [-1, -13, -2, 1, -3, 4, -1, 2, 1, -5, 4] должно вернуть [4, -1, 2, 1].

1. Дан треугольник. Найдите минимальный путь от вершины до основания. На каждом шаге вы можете двигаться только на соседние цифры, находящиеся в ряду ниже.

    Пример:

    ```
    [
         [2],
        [3,4],
       [6,5,7],
      [4,1,8,3]
    ]
    ```

    Здесь длина минимального пути от вершины до основания равна 11 (т.к 2+3+5+1 = 11).

1. У компании имеется следующий склад (см. рис), три ряда стеллажей, стоящие в ряд по 700 ед. Каждый стеллаж содержит 5 полок. Каждая полка содержит 6 ячеек. Между рядами стеллажей есть проходы. Между стеллажами в одном ряду проходов нет. Ширина полок одинакова и равна ширине прохода. Зеленым цветом обозначены проходы.

    Кладовщику выдается случайный перечень ячеек, из которых требуется взять товар. Помогите составить маршрут передвижения кладовщика по складу, начиная движение от стола, таким образом, чтобы он затратил минимально возможный путь.

    1. Достаточно описать шаги алгоритма решения задачи.
    1. Объясните почему решение оптимальное.

        ![Оптимальное решение](images/sklad.jpg)

1. Найдите минимальную разницу в минутах между двумя моментами времени из списка.

    Например, если массив такой `["2:10pm", "1:30pm", "10:30am", "4:42pm"]`, программа должна вернуть 40, потому что минимальная разница — между 1:30pm и 2:10pm и она равна 40 минутам.

    На вход всегда передается массив из как минимум двух элементов, все элементы массива заданы в корректном формате и уникальны.

1. Написать функцию `get_change(money, price)`, которая рассчитывает сдачу для суммы и возвращает массив монет, набор монет 1c, 5с, 10с, 25с, 50с, 1$. Возвращаемый массив это массив из шести элементов, где каждый элемент это количество монет каждого типа.

    ```
    getChange(3.14, 1.99) => [0, 1, 1, 0, 0, 1]
    getChange(3, 0.01) => [4, 0, 2, 1, 1, 2]
    getChange(4, 3.14) => [1, 0, 1, 1, 1, 0]
    getChange(0.45, 0.34) => [1, 0, 1, 0, 0, 0]
    ```

1. **Palindrome Swapper**: Have the function `PalindromeSwapper(str)` take the `str` parameter being passed and determine if a palindrome can be created by swapping two adjacent characters in the string. If it is possible to create a palindrome, then your program should return the palindrome, if not then return the string `-1`. The input string will only contain alphabetic characters.

    For example: if `str` is `"rcaecar"` then you can create a palindrome by swapping the second and third characters, so your program should return the string `racecar` which is the final palindromic string.

    Examples:

    * Input: `"anna"`, Output: `anna`
    * Input: `"kyaak"`, Output: `kayak`

1. Реализовать возможность скрытия логина скайпа (логин может быть разделен точкой). Символ скрытия по умолчанию `"ххх"`.

    Логин может встретиться в двух местах:

    1. В строчке. skype:some.login
    1. В html тэге <a></a>. Пример `<a href=\"skype:some.login?call\">skype</a>`

1. Реализовать возможность скрытия произвольного количества цифр телефонного номера. По умолчанию скрывается 3 последние цифры. По умолчанию символ замены цифр `"х"`.

    Формат номера `+1 111 111 11 11`. Результат выполнения: `+1 111 111 1х хх`.

    Пробелов между цифрами может быть сколько угодно, но результат выполнения должен приводиться к формату `+1 111 111 11 11`.

1. Пользователь вводит строки, содержащие цифры, разделенные запятыми. Например "1,2,3,4". Пустая строка означает окончание ввода. После окончания ввода одной строки, запрашивается следующая и т.д. Две пустых строки подряд означает, что пользователь закончил ввод данных. Необходимо проверить что введенная матрица является квадратной (количество строк равно количеству столбцов). Если матрица является квадратной, то посчитать ее определитель.

1. **HTML Elements**: Have the function `HTMLElements(str)` read the `str` parameter being passed which will be a string of HTML DOM elements and plain text. The elements that will be used are: `b, i, em, div, p`.

   For example: if `str` is `"<div><b><p>hello world</p></b></div>"` then this string of DOM elements is nested correctly so your program should return the string `true`.

   If a string is not nested correctly, return the first element encountered where, if changed into a different element, would result in a properly formatted string. If the string is not formatted properly, then it will only be one element that needs to be changed.

   For example: if `str` is `"<div><i>hello</i>world</b>"` then your program should return the string `div` because if the first `<div>` element were changed into a `<b>`, the string would be properly formatted.

   Examples:

   * Input: `"<div><div><b></b></div></p>"`, Output: `div`
   * Input: `"<div>abc</div><p><em><i>test test test</b></em></p>"`, Output: `i`

1. **K Unique Characters**: Have the function `KUniqueCharacters(str)` take the `str` parameter being passed and find the longest substring that contains `k` unique characters, where `k` will be the first character from the string. The substring will start from the second position in the string because the first character will be the integer `k`.

   For example: if `str` is `"2aabbacbaa"` there are several substrings that all contain 2 unique characters, namely: `["aabba", "ac", "cb", "ba"]`, but your program should return `"aabba"` because it is the longest substring. If there are multiple longest substrings, then return the first substring encountered with the longest length. `k` will range from 1 to 6.

   Examples:

   * Input: `"3aabacbebebe"`, Output: `"cbebebe"`
   * Input: `"2aabbcbbbadef"`, Output: `"bbcbbb"`

1. **Сумма квадратов**: Программа должна вернуть строку `'true'`, если заданное число является суммой квадратов и `'false'`, если не является.

   Например:

   * 25 должно вернуть `'true'`, потому что `25 = 3² + 4²`
   * 1601 должно вернуть `'true'`, потому что `1601 = 40² + 1²`

1. **Сравнение массивов**: Даны два массива массивов. Сравнить массивы и вернуть `true`, если массивы массивов одинаковы. Элементы в массиве могут быть переставлены местами, и значения внутри этих массивов могут тоже быть переставлены.

   Например:
   * ```# func([[5, 0], [5, 0], [5, 0]], [[5, 0], [5, 0], [0, 5]]) #=> true```
   * ```# func([[2, 3], [5, 0]], [[5, 0], [3,2]]) #=> true```

1. **Покупка/продажа зерна**: Дан массив с ценами на зерно по дням. Цена покупки и продажи одинакова в этот день. Найти **индексы дня** покупки и последующей продажи для получения максимальной выгоды.

   Вернуть массив из 2х элементов: индекс дня покупки и индекс дня продажи или пустой массив.

   Например:
   * ``` profit([13, 6, 3, 4, 10, 2, 3])    #=> [2, 4] ```
   * ``` profit([13, 6, 3, 1])   #=> [] ```

1. **Сумма цифр**: Написать функцию, которая принимает на вход число, суммирует цифры в нём, потом, если получилось число из 2 и более цифр, суммирует цифры в нём и так далее, пока не получится однозначное число, которе функция возвращает. Такое число называется «цифровым корнем» исходного числа.
