# Области видимости и замыкания в Javascript

Со всеми этими функциями, нам необходимо следить за областью видимости! Какие переменные где определены? Кто имеет к ним доступ? Что за загадочная переменная `this`, которая видимо воплощает все странное и загадочное, касающееся области видимости в Javascript?

Все эти области (и использование замыканий) важны, потому что функции в JS могут быть вызваны в разное время и из разных участков кода, особенно если они связаны с событиями (где они вызываются в виде коллбэков - которые вы уже видели, но мы рассмотрим их подробнее в следующем уроке).

## Points to Ponder

* Чему равна `this`? (непростой вопрос...)
* Как поместить переменную в какую-либо область видимости?
* Зачем определять переменную `that`?
* Why is id naughty to modify or reference variables from outside your scope?
* Почему "приватные" переменные на самом деле не совсем "приватные"?
* Функции всегда должны возвращать то же самое значение... или.. ?
* Как способ вызова функции (в виде функции, метода...) оказывает влияние на область видимости (и `this`)?

## Ваши задания

1. Прочтите [Что вам надо знать об областях видимости в Javascript от Smashing Magazine](http://coding.smashingmagazine.com/2009/08/01/what-you-need-to-know-about-javascript-scope/)
2. Прочтите [о Замыканиях в Javascript от learn.jquery.com](http://learn.jquery.com/javascript-101/closures/)
2. Прочтите ответы на [SO по вопросу "Как работают замыкания в Javascript?"](http://stackoverflow.com/questions/111102/how-do-javascript-closures-work) для лучшего понимания нюансов.
3. Прочтите [о `this` в Javascript](http://javascriptissexy.com/understand-javascripts-this-with-clarity-and-master-it/)
4. Прочтите о [методах Javascript `apply`, `call` и `bind`](http://javascriptissexy.com/javascript-apply-call-and-bind-methods-are-essential-for-javascript-professionals/)
4. Прочтите о [Function.Prototype.Bind](http://coding.smashingmagazine.com/2014/01/23/understanding-javascript-function-prototype-bind/) для глубокого понимания 'bind'. Возможно, вам придется вернуться к этому материалу попозже из-за его сложности.

## Дополнительные ресурсы

*Этот раздел содержит полезные ссылки на дополнительные материалы. Это не обязательно, так что расценивайте их как нечто полезное, если вы хотите поглубже погрузиться в тему*

* [Разбираем замыкания в JS](http://javascriptissexy.com/understand-javascript-closures-with-ease/)
* [Понимание области видимости переменных и их поднятия в JS](http://javascriptissexy.com/javascript-variable-scope-and-hoisting-explained/)
