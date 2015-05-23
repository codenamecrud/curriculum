# Работа с файлама и сериализованными данными
<!-- *Estimated time: 2-4 hrs* -->
До этого времени вы, в основном работали с автономными консольными программами. Самое время попробовать начать взимодействовать с файлами. Файлы, по-сути, представляют собой массив байтов, который вам надо как-нибудь открыть, прочитать в вашей программе, изменить и сохранить. Несмотря на то что многие файлы (например изображения) похожи на гигантские нагоромождения данных, если их открыть текстовым редактором, все равно полезно представлять себе файл как одну длинную строку или поток байтов. Ваша программа прочитает эти байты сверху вниз, выполняя все операции, которые вы опишете.

К счастью для вас, Ruby делает вашу жизнь проще при работе с файлами. С языком идут инструменты, необходимые для чтения длинных потоков байтов в программе и позволяюще работать с ними как с обьектами, с которыми вы уже знакомы. Если вы держите в голове что файлы это всего лишь длинный поток слов/символов/байтов, который считывается сверху вних, то все должно быть интуитивно понятно. Если вы хотите делать более детализированные вещи, такие как запись в определенную позицию в файле, вам сначала необходимо выяснить в каком месте файла вы находитесь, так как вы можете быть где-то в середине файла.

Работая с файлами приводит вас к идее сериализации, которая в основном сводится к тому чтобы преобразовывать любые данные в формат, который хранится как строка. Это может быть полезным если вы хотите сохранить свои обьекты и классы (например, в момент игры) в файл, или если вы желаете передать эти же самые обьекты в веб-браузер (пока есть только один вариант передавать информацию через HTTP - как строку).

Luckily, Ruby again makes things pretty easy for you. There are some generally accepted formats for serializing data and Ruby gives you the tools you'll need to work with all of them.  The two you'll run into again and again are YAML and JSON.  You often see YAML used to save configuration files in Ruby on Rails because it's very lightweight and straightforward.  You can read it easily in a text editor.  JSON is ubiquitous across the web, and is the format of choice to deliver complex or deeply nested data (like objects) from some website to your program via an API (like if you want to interface with Google Maps).

Finally, files and serialization overlaps in a lot of ways with the idea and purpose of databases -- they facilitate the ability to maintain state and permanence for your data.  We'll briefly look into some basic database connections that Ruby provides as well.

## Points to Ponder

*Look through these now and then use them to test yourself after doing the assignment*


* What are two ways to store a file from your hard drive into a string or array in your Ruby script?
* What are three things made possible or much easier by serialization?
* What is JSON?
* What is YAML?
* How do you turn a Ruby object into JSON?
* How do you turn JSON into a Ruby object?

## Your Assignment

1. Refresh yourself on [Ruby Monk's section on the `File` class](http://rubymonk.com/learning/books/1/chapters/42-introduction-to-i-o/lessons/90-using-the-io-class) (this may be review for you)
2. Read through [Ruby Monk's section on Serializing](http://rubymonk.com/learning/books/4-ruby-primer-ascent/chapters/45-more-classes/lessons/104-serializing)
1. Read [Beginning Ruby](http://beginningruby.org/) Chapter 4: `Developing Your First Ruby Application` and follow along with the tutorial.
2. Read [Beginning Ruby](http://beginningruby.org/) Chapter 9: `Files and Databases`.  Much of the databases stuff will be review from the Web Development 101 course and at first you won't often use the connection methods yourself (often an ORM like ActiveRecord for Rails will have that code already written for you), so feel free to skim over it but do try to see what Ruby is capable of.
3. Read the [Chapter on File I/O](http://ruby.bastardsbook.com/chapters/io/) of the Bastard's Book of Ruby.  Much of it will go quickly for you given what you've already read, but there are some new nuggets in there.

## Additional Resources

*This section contains helpful links to other content. It isn't required, so consider it supplemental for if you need to dive deeper into something*


* [Zetcode's section on Input/Output in Ruby](http://zetcode.com/lang/rubytutorial/io/) should be another useful perspective on the material.