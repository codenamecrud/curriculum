### Расширенные базовые элементы Ruby

Этот урок освещает темы, которые пока мало затрагивались в нашем курсе. Мы подробно рассмотрим такие темы как: управление процессом исполнения программы, циклы, массивы, хеши, блоки и строки. Все это будет рассмотрено подробнее, чем в предыдущих разделах. Проекты в секции Задания рассчитаны на самостоятельную работу, потому что Codeacademy может дать всю информацию которая может понадобиться.

### Пункты для размышления

*Посмотрите эти пункты сейчас, а затем с их помощью проверьте себя после выполнения задания.*

**Внимание:** Это опять огромный список вопросов. Просмотрите его сейчас, потом глубоко вдохните, сделайте задание и уже после этого возвращайтесь к нему.

* Условия и управление процессом исполнения

	* Что такое `boolean`?
	* Какие значения возвращают `true`?
	* Что вернут `nil`, `0`, `"0"`, `""`, `1`, `[]`, `{}` and `-1`, `true` или `false`?
	* Когда используется `elsif`?
	* Когда используется `unless`?
	* Что делает `<=>`?
	* Зачем может понадобиться определять свой метод `<=>`?
	* Что делают операторы `||`, `&&` и `!`?
	* Что вернет вызов `puts("woah") || true`?
	* Что такое `||=`?
	* Что такое тернарный оператор?
	* Когда используется оператор `case`?

* Итерации

	* Что делает `loop`?
	* Какими двумя способами можно определить блок кода?
	* Что такое индексная переменная?
	* Как вывести на экран каждый элемент массива `[1,3,5,7]` с помощью:
		* `loop`?
       * `while`?
       * `for`?
       * `#each`?
       * `#times`?
   * Какая разница между `while` и `until`?
   * Как остановить цикл?
   * Как пропустить следующую итерацию цикла?
   * Как запустить цикл заново?
   * Какие основные различия между ситуациями когда стоит использовать `while` или `#times`или `#each`?
   * Что значит "внутренные циклы" и когда их стоит использовать?

* Блоки, Proc и лямбды:
	* Чем блок схож с функцией?
	* Чем блок отличается от функции?
	* Какими двумя способами объявить блок?
	* Как вернуть данные из блока?
	* Что происходит когда вы включаете оператор `return` в блок?
	* Для чего стоит использовать блок вместо простого объявления метода?
	* Что делает `yield`?
	* Как передать аргументы в блок изнутри метода?
	* Как проверить вызывался ли блок?
	* Что такое proc?
	* Какая разница между proc и блоком?
	* Когда стоит использовать proc вместо блока?
	* Что такое замыкание (closure)?
	* Что такое лямбда?
	* Какая разница между лямбдой и proc?
	* Что такое `Method` (с большой М)?
	* Что Методы позволяют сделать такого, что возможно будет полезным в дальнейшем при разработке более продвинутых программ?

* Перечисления (Enumerable) и модули
	* Что такое модули?
	* Чем полезны модули?
	* Что делает `#each`?
	* Что возвращает `#each`?
	* Что делает `#map`?
	* Что возвращает `#map`?
	* В чем разница между `#map` и `#collect`?
	* Что делает `#select`?
	* Что возвращает `#select`?
	* Какая разница между `#each`, `#map` и `#select`?
	* Что делает `#inject`?
	* Для чего можно использовать `#inject`?
	* Как проверить, удовлетворяет ли каждый элемент в хеше определенному условию?
	* Что будет, если ни один из элементов не удовлетворяет условию?
	* Что такое (в основном) `enumerator`?

* Написание методов
	* Сколько вещей должен делать метод в идеале?
	* Какие типы объектов должен модифицировать метод?
	* Как стоит называть методы?
	* Что значит `self`?
	* Что надо сделать чтобы создать свой файл Ruby скрипта?
	* Как запустить свой Ruby скрипт из командной строки?
	* Как убедиться, что что ваш скрипт был запущен из командной строки?
	* Что делает "shebang" строка?
	* Что делает `require`?
	* Что делает `load`?
	* В чем разница между `load` и `require`?
	* Как получить доступ к параметрам, которые были переданы файлу скрипта из командной строки?
	* Что делает `#send`?
	* Отличается ли использование `#send` от обычного вызова метода объекта?

## Ваше задание

1. Выполнить [Секции 2-6 курса от Codeacademy](http://www.codecademy.com/tracks/ruby), включая:
	1. [Управление процессом выполнения](http://www.codecademy.com/courses/ruby-beginner-en-NFCZ7)
	2. [Проект: Thith Meanth War!](http://www.codecademy.com/courses/ruby-beginner-en-JdNDe?curriculum_id=5059f8619189a5000201fbcb)
	3. [Циклы в Ruby](http://www.codecademy.com/courses/ruby-beginner-en-XYcN1?curriculum_id=5059f8619189a5000201fbcb)
	4. [Проект: Redacted!](http://www.codecademy.com/courses/ruby-beginner-en-mzrZ6?curriculum_id=5059f8619189a5000201fbcb)
	5. [Массивы и Хеши](http://www.codecademy.com/courses/ruby-beginner-en-F3loB?curriculum_id=5059f8619189a5000201fbcb)
	6. [Проект: Create a Histogram](http://www.codecademy.com/courses/ruby-beginner-en-693PD?curriculum_id=5059f8619189a5000201fbcb)
	7. [Блоки и Сортировка](http://www.codecademy.com/courses/ruby-beginner-en-ET4bU?curriculum_id=5059f8619189a5000201fbcb)
	8. [Проект: Ordering your Library](http://www.codecademy.com/courses/ruby-beginner-en-nOho7?curriculum_id=5059f8619189a5000201fbcb)
	9. [Хеши и Символы](http://www.codecademy.com/courses/ruby-beginner-en-Qn7Qw?curriculum_id=5059f8619189a5000201fbcb)
	10. [Проект: A Night at the Movies](http://www.codecademy.com/courses/ruby-beginner-en-0i8v1?curriculum_id=5059f8619189a5000201fbcb)
	11. [Блоки, Proc и лямбды](http://www.codecademy.com/courses/ruby-beginner-en-L3ZCI?curriculum_id=5059f8619189a5000201fbcb)

2. Завершить [Beginning Ruby](http://beginningruby.org/) Глава 3: `Ruby's Building Blocks: Data, Expressions, and Flow Control` (страницы 50-76)
3. Посмотреть следующие посты Эрика Траутмана для более углубленного понимания
	1. [Ruby Explained: Conditionals and Flow Control](http://www.eriktrautman.com/posts/ruby-explained-conditionals-and-flow-control)
    2. [Ruby Explained: Iteration](http://www.eriktrautman.com/posts/ruby-explained-iteration)
    3. [Ruby Explained: Blocks, Procs, and Lambdas, aka "Closures"](http://www.eriktrautman.com/posts/ruby-explained-blocks-procs-and-lambdas-aka-closures)
    4. [Ruby Explained: Map, Select, and Other Enumerable Methods](http://www.eriktrautman.com/posts/ruby-explained-map-select-and-other-enumerable-methods)
    5. [Ruby Explained: Writing and Running Methods](http://www.eriktrautman.com/posts/ruby-explained-writing-and-running-methods)

## Проверьте себя

 Убедитесь, что вы можете пройти следующие тесты от [Code Quizzes](http://www.codequizzes.com/). Они не требуют много времени и могут дать вам понимание, чего вам не хватает.

1. [Beginner Ruby Quiz #2](http://www.codequizzes.com/learn-ruby/arrays-conditionals-loops)
2. [Quiz #3](http://www.codequizzes.com/learn-ruby/variable-scope-methods)
3. [Quiz #4](http://www.codequizzes.com/learn-ruby/symbols-array-methods-hashes)
4. [Quiz #6](http://www.codequizzes.com/learn-ruby/iteration-nested-data-structures)

## Дополнительные ресурсы

*Здесь собраны полезные ссылки на другие источники информации. Изучать их необязательно, но они могут быть полезны для более глубокого погружения в материал*

* До сих пор неуверены в `Enumerable`? Прочтите [Главу про Enumerable в Bastard's Book](http://ruby.bastardsbook.com/chapters/enumerables/)
* Гист на гитхабе про [Truthiness](https://gist.github.com/jfarmer/2647362)
* Посмотрите [эти ответы про оператор Spaceship](http://stackoverflow.com/questions/827649/what-is-the-ruby-spaceship-operator)
* Прочтите [раздел про управление процессом исполнения от Zetcode](http://zetcode.com/lang/rubytutorial/flowcontrol/) для более глубокого погружения в тему.
* Если хотите немного большего [запись про циклы и итераторы в Ruby от Skork](http://www.skorks.com/2009/09/a-wealth-of-ruby-loops-and-iterators/)
* [Понимание Blocks Procs and Lambdas](http://www.reactive.io/tips/2008/12/21/understanding-ruby-blocks-procs-and-lambdas/)
* [Почему существуют различные варианты передачи блока методу: неочевидный с помощью yield и очевидный - с указанием наличия блока в числе аргументов? Какая разница? (с SO)](http://stackoverflow.com/questions/1410160/ruby-proccall-vs-yield)
* [Написание собственных методов](http://rubylearning.com/satishtalim/writing_own_ruby_methods.html)
* Краткое руководство по написанию методов [wikibooks](http://en.wikibooks.org/wiki/Ruby_Programming/Writing_methods)
* [Введение в Hello World](http://en.wikibooks.org/wiki/Ruby_Programming/Hello_world)
* [LRTHW главы 13-14](http://ruby.learncodethehardway.org/book/)
