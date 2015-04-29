# Проект: Установки
*Общее время завершения: 3-6 часов*

Один шаг, который может быть излишне раздражающим, заключается в необходимости установить все необходимое на ваш компьютер, чтобы можно было приступить к практике. Практически каждый вчерашний новичок имеет в запасе страшную историю о том, как долго он сражался со своим компьютером и Гуглом, прежде чем сумел правильно установить все, что нужно. И часто вы можете услышать это как причину того, почему люди так долго "раскачиваются", прежде чем начать действовать.

Это может стать испытанием, но если вы заинтересованы в том, чтобы быть хотя бы полу-серьезным веб-разработчиком, вам *потребуется* рано или поздно собрать все необходимое на вашем компьютере, и лучше всего, если это будет сделано как можно раньше. Этот урок посвящен исключительно помощи в установке всего необходимого, чтобы мы погли покончить с этим и двигаться вперед, к более интересным вещам.

Одним вариантом для обучения разработке всегда было использование существующей онлайн-среды. На самом деле, практически все сайты, предназначенные для новичков, сейчас имеют все необходимое, чтобы вы просто написали какой-то код и они тут же выполнили его. Магия! Откровенно говоря, мы считаем, что это некорректный подход. Что случится, когда вам понадобится создать что-то собственное? Но, если вопрос в том, чтобы иметь онлайн-среду (как [Nitrous.io](https://lite.nitrous.io/join/lqMOGUUSEpA?utm_source=nitrous.io&utm_medium=copypaste&utm_campaign=referral)) и у вас нет настроенной рабочей среды, вы можете воспользоваться ею. Мы поговорим об альтернативах ниже.

Если вы застряли в процессе установки, не сдавайтесь! Найдите опытного программиста, который поможет вам и погуглите сообщения об ошибках, чтобы решить встреченные проблемы. Найдите кого-нибудь, кто сможет вам помочь. Все проходят через это, так что не считайте себя сумасшедшим, если ваш компьютер вдруг показался вам злобно настроенным зверем. Сразитесь с ним... в сети множество ресурсов и кто-нибудь уже встречался с вашей проблемой раньше.


## Установка Бэкенд- против Фронтенд-окружения

Мы уже знаем, в чем основные различия между бэкендом (серверной стороной) и фронтендом (клиентской стороной), но вы увидите, что они проявляются вновь, когда дело доходит до установки необходимого софта. Поскольку код клиентской стороны выполняется в браузере, все, что вам нужно, чтобы писать HTML, CSS и Javascript - это браузер, такой как Chrome, Firefox или (брр) Internet Explorer.

Сайты вроде [CodePen](http://codepen.io/) и [JSFiddle](http://jsfiddle.net/) позволят вам создавать маленькие, но динамические веб-страницы прямо в вашем браузере. Они станут несколько громоздкими, когда вы попробуете создать что-либо более значительное, для чего потребуется больше писать в текстовом редакторе, но они чертовски удобны для решения небольших задач. Отсуствие сложного в установке софта является одной из причин, благодаря которым фронтенд-программирование более доступно для пробы новичками.

Серверный код несколько отличается - поскольку каждый язык программирования (например, Ruby или Python) отличается от другого, вам придется установить этот язык непосредственно на ваш компьютер. С Ruby вы установите интерпретатор так же, как любую другую программу. Когда вы запускает код на Ruby, вы на самом деле запускаете программу Ruby. В принципе, это не должно быть слишком сложным, но это дополнительный шаг, в отличие от простого запуска текстовых файлов в браузере.

Другая причина чуть большей сложности бэкенд-среды в том, что программистам нужно не просто писать код, но и иметь в распоряжении разные версии Ruby одновременно (возможно, в процессе работы над старым сайтом в один день и над новым - в другой) и разворачивать нужные сайты на нужных веб-серверах. Каждое из этих улучшений рабочего процесса требует отдельной программы для удобного управления собой.

По сути, установка среды для разработки серверного кода на Ruby сводится всего лишь к установке интерпретатора Ruby и пары программ на ваш компьютер. Это выглядит как куча разных вещей, если вы незнакомы с каждой из них. Мы дадим вам краткое описане каждой из них ниже, а затем вы сможете установить их сами.

## Windows и веб-разработка

Последнее замечание для пользователей Windows: вы можете установить все нужное, но в любом случае иногда вы будете чувствовать себя так, словно плывете против течения. Многие примеры в учебном процессе будут подразумевать, что вы работаете на Mac или Linux, и вам придется постараться, чтобы применить определенные шаги к вашему рабочему процессу. Страдание укрепляет характер. И да, это похоже на это возврат в девяностые, когда приходилось ждать по пол-года, прежде чем выходила Mac-версия для какой-нибудь относительно свежей игры.

Возможно, лучшим вариантом будет попытка начать использовать Linux (признайтесь, вам любопытно...) или использовать онлайн-среду вроде [Nitrous.io](https://lite.nitrous.io/join/lqMOGUUSEpA?utm_source=nitrous.io&utm_medium=copypaste&utm_campaign=referral). Это не обязательно, просто дружеский совет.

## Что вы будете устанавливать

К счастью, все это бесплатно. Вы будете устанавливать каждую необходимую часть окружения, используя руководство, расположенное ниже, но для начала вкратце о каждой из них:

### Ruby

Ruby - это бэкенд-язык, который мы будем использовать для написания серверного кода. Интерпретатор Ruby является программой, так что вам нужно будет убедиться, что он установлен на вашем компьютере и вы имеете подходящую версию (между, скажем, 1.8.7, 1.9.3 и 2.x достаточно много различий).

### Git

Git, система контроля версий, о которой вы уже читали, является еще одним инструментом, требующем установки, это совсем просто. Так же вам нужно будет создать аккаунт на Github, это очень важно, поскольку на нем будет храниться ваше портфолио. Когда люди посещают ваш репозиторий на Github (если он публичный), они видят файлы с исходным кодом, которые вы туда загрузили.

### Heroku

Heroku - облачный хостинг-сервис, который мы будем использовать, чтобы разворачивать наши приложения и выпускать их в Сеть. Отчасти Хероку работает как Github, поскольку вы будете отправлять туда код практически таким же способом, но он выполняет совершенно другую функцию. В то время, как Гитхаб хранит ваши репозитории с исходным кодом, Хероку непосредственно выполняет этот код на сервере таким образом, чтобы ваше приложение могли посещать пользователи. Хероку требует пару установки полезных инструментов, которые сделают вашу жизнь проще, когда вам потребуется развернуть (задеплоить) приложение.

### HTML, CSS и Javascript

Вообще, нам не понадобится устанавливать ничего из перечисленного - они уже встроены в ваш браузер. В более поздних курсах вы сможете использовать Javascript непосредственно на вашем компьютере в качестве серверного языка программирования (Node.js), но сейчас вам нет нужды беспокоиться об этой троице.

### Текстовый редактор

Мы рекомендуем использовать текстовый редактор, такой, как [Sublime Text 3](http://www.sublimetext.com/). Он снабжен огромным количеством полезных горячих клавиш, подсветкой кода и другими удобными возможностями, которые сделают вашу жизнь проще, и это лишь малая часть его достоинств.

Изучите [этот "Быстрый курс по Sublime Text" авторства Дженнифер Манн](http://jennifermann.ghost.io/a-quick-guide-to-sublime-text/), чтобы узнать о некоторых полезных возможностях и трюках. Она ссылается на [этот туториал (~2.5 часов видео) от NetTuts](https://tutsplus.com/course/improve-workflow-in-sublime-text-2/), отчасти объясняющий, почему Sublime Text такой классный. Первая часть видео - самая важная, не беспокойтесь о полном понимании деталей в оставшемся видео (но вам стоит вернуться и пересмотреть его, когда освоитесь с редактором).

### Ruby Gems

Здесь у нас несколько Ruby-гемов (которые являются просто небольшими упакованными библиотеками кода), которы мы установим, чтобы получить инструменты для общения с базой данных и облегченной установки других гемов в будущем.

### RVM

RVM - это способ быть уверенным, что каждый проект Ruby on Rails на вашем компьютере работает независимо от всех остальных. Этот инструмент позволяет устанавливать неколько различных версий Ruby, Rails или любых других гемов на компьютер. Затем вы сможете переключаться между ними, когда это будет необходимо.

Это очень полезно, поскольку иногда вам придется работать над проектом, использующим старую версию Ruby (скажем, 1.9.3), и одновременно взаимодействовать с проектами на более новой версии (2.0.0). Поскольку вы однозначно не захотите удалять и переустанавливать Ruby каждый раз, RVM позволит вам легко выбирать, какой набор гемов использовать для конкретного проекта и ВУАЛЯ! ваша проблема решена.

### Rails

Как насчет Rails? Rails на самом деле является Ruby-гемом, поскольку это просто куча кода на Ruby, заранее упакованная для вас. Вы "устанавливаете" его, загружая гем `rails`.

### Mac: XCode

XCode - интегрированная среда разработки от Apple, используемая для разработки приложений под Mac, iPhone и iPad. Несмотря на то, что мы не будем использовать её в этих целях, она снабжена инструментами командной строки, которые вы будете использовать, так что вам, вероятно, придется установить эту среду (это здоровеный пакет).

## Задания: Праздник установки

These installfests will take you through the steps to install everything on your computer.  It will probably feel like you're doing a whole bunch of things that don't really make sense and moving way too quickly.  Hopefully you've got a basic understanding of what you're about to install, but it's also not super important that you know exactly what's going on or what all the commands mean.  You'll get more familiar with things over time.

1. If you are using a Macintosh, follow the instructions on [Moncef Belyamani's blog](http://www.moncefbelyamani.com/how-to-install-xcode-homebrew-git-rvm-ruby-on-mac/).
2. Otherwise, do the [Railsbridge Installfest](http://installfest.railsbridge.org/installfest/) for your system.
3. Even if you didn't use the Railsbridge installation instructions, verify your installation by following their instructions for [creating a sample Rails app](http://installfest.railsbridge.org/installfest/create_a_rails_app) and then [deploying it](http://installfest.railsbridge.org/installfest/deploy_a_rails_app).
4. Typing `$ ruby -v` on your command line (ignore the $, it stands for the prompt) should output something that includes `2.0.0` or a similar number.  `$ rails -v` should give you something like `4.0.0`.

## Checklist

##### Before moving on, you should have:
* Set up your [github](http://github.com/) account
* Set up your [heroku](http://www.heroku.com/) account
* Created and deployed a sample rails application
* Patted yourself on the back for accomplishing a task that has turned back many brave warriors.

## Oh no! Total Failure!!!

If all else fails, the best web-based development environment to use for coding the back end is [Nitrous.io](https://www.nitrous.io/join/GRrt3VYaHE8?utm_source=nitrous.io&utm_medium=copypaste&utm_campaign=referral).  It's free to use and gives you a brand spanking new Ruby and Rails setup to start coding with. You can even integrate it with your text editor and work collaboratively with other people.

I've often found this to be much easier for Windows users than trying to navigate the regular installations process.  It relies on having an internet connection, but it gives you a command line, a text editor, and the ability to run a local server right out of the box.

So your alternate path is to go to [Nitrous.io](https://www.nitrous.io/join/GRrt3VYaHE8?utm_source=nitrous.io&utm_medium=copypaste&utm_campaign=referral) and set up your account.  You'll be given enough free "credits" to keep a virtual development environment running full time.  The instructions on the website are fairly straightforward.  You can get your text editor and terminal up and running in a couple minutes.  Plus, it works with Git!

## Additional Resources

*This section contains helpful links to other content. It isn't required, so consider it supplemental for if you need to dive deeper into something*

If you've run into issues with your installation and are desperately looking for something else to try, take a deep breath first and go back over the instructions step-by-step to make sure you've followed them properly.  You can run into some odd issues if you start trying to mix together different installation recommendations, because some of them use auto-installers and have you install things in slightly different places so you may end up with a couple copies of key components.  It may work fine on the surface, but some day it'll probably come back and frustrate you again.  But, if you must, here are some other people's installation recommendations:

* Michael Hartl describes the installation in his [Rails Tutorial, Chapter 1](http://ruby.railstutorial.org/ruby-on-rails-tutorial-book#sec-up_and_running), and the chapter also guides you through making and deploying your first bare-bones Rails app just to make sure everything's working properly.
* Treehouse has short videos describing Rails installation for various environments in their [Getting Started with Rails](http://teamtreehouse.com/library/programming/build-a-simple-ruby-on-rails-application/getting-started-with-rails) unit.
* [Rubyonrails.org](http://rubyonrails.org/download) installation section.
* [Guide](http://stackoverflow.com/questions/9440639/sublime-text-from-command-line-win7) for opening Sublime Text via command line in Windows.
* [Rails Installer](http://railsinstaller.org/en) goes in and forces Rails to be installed on your system.  If your computer has been behaving badly, maybe this scorched earth approach is the best.
* Google Google Google
