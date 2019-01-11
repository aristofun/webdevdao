# Вопросы по Ruby

1. Что такое `loop`, `while`, `map`, `each`?

    <details>
      <summary>Ответ</summary>

      `loop`, `while` — это управляющие конструкции, создающие циклы, повторение кода по условию/без условий.

      `each`, `map` — итераторы, перебирают все элементы у объекта (унаследованы от `Numerable`).

      Итераторы — это методы, которые принимают блоки и выполняют код в блоках для элементов коллекций (массивов, интервалов или хэшей).

      https://www.rubyguides.com/ruby-tutorial/loops/

      https://www.rubyguides.com/2018/10/ruby-map-method/

      http://rubycode.ru/ruby/osnovy/57-chislovye-iteratory.html

      http://queirozf.com/entries/ruby-map-each-collect-inject-reject-select-quick-reference
    </details>

1. Какие еще циклы вы знаете?

    <details>
      <summary>Ответ</summary>

      `times`, `upto`, `downto`, `until`, `for * in *`

      https://i-love-ruby.gitlab.io/#_loops
    </details>

1. Какие переменные бывают, где они используются, где они доступны (поле видимости)?

    <details>
      <summary>Ответ</summary>

      Локальные переменные `variable` — локальная переменная, она доступна только в той области видимости, где была определена.

      Переменные экземпляра класса `@variable` — доступны только в методах экземпляра класса, где они определены. При первом вызове возвращают `nil`.

      Глобальные переменные `$variable` — область видимости — вся программа (опасно использовать, т.к. потом сложно изменить, где и кто её поменял).

      Переменные класса `@@variable` — область видимости — класс в котором они определены и все экземпляры данного класса.

      http://rubycode.ru/ruby/osnovy/54-oblast-vidimosti-i-tipy-obektov.html
    </details>

1. Что такое переменная с одной @ и переменная с двумя @@?

    <details>
      <summary>Ответ</summary>

      Переменные экземпляра класса `@variable` — начинаются с `@`. Переменные экземпляра класса доступны в методах экземпляра класса, где они определены.

      Переменные класса `@@variable` — начинаются с двух символов `@`. Их область видимости — класс в котором они определены и все экземпляры данного класса.
    </details>

1. Чем require отличается от require_relative?

    <details>
      <summary>Ответ</summary>

      http://ruby.qkspace.com/ruby-require-require_relative
    </details>

1. Что такое гемы? Как с ними работать?
1. Как создать геттер и сеттер методы в ruby?
1. Что такое `attr_reader, `attr_writer`, `attr_accessor`?
1. Что означает ключевое слово `self`?
1. Что такое `super`-методы и как они работают/где применяются?
1. Что такое модуль в ruby? Какая разница между классом и модулем?
1. Какие виды наследования поддерживаются в ruby?
1. Чем отличается `include` от `extend`? Что такое `prepend`?

    <details>
      <summary>Ответ</summary>

      https://habr.com/post/143483/

      https://inet777.ru/comments/8436/metod-module-prepend-v-ruby-2
    </details>

1. Реализация множественного наследования в ruby?
1. Какие есть способы вызова методов в ruby?
1. Что такое `proc`, `lambda`, `block`? И какие отличия есть между ними?
1. Многопоточность в ruby?
1. Какие структуры есть в ruby?
