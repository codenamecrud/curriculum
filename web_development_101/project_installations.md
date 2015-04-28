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



A final note to Windows users -- you can install everything you need to but you'll feel at times like you're swimming against the current.  Many examples throughout the learning process will assume you're working on a mac and you'll have to get good at translating certain steps into your own workflow.  Suffering builds character.  And this is payback for the 90's when it took another six months to come out with a Mac version of any half-decent game.

Your best bet may be to try using Linux (admit it, you've been curious...) or to use a hosted environment like [Nitrous.io](https://www.nitrous.io/join/GRrt3VYaHE8?utm_source=nitrous.io&utm_medium=copypaste&utm_campaign=referral).  Not a requirement, just a friendly tip.

## What You'll Be Installing

Luckily, it's all free.  You'll be installing each of these using the tutorial below, but first here's a brief word about each item:

### Ruby

Ruby is the back end language we'll be using to write our server code.  The Ruby interpreter is a program like any other and so you'll need to make sure it's installed on your computer and you've got the right version (there are some big differences between, say, version 1.8.7 and 1.9.3 or 2.x).


### Git

Git, the version-control system you've read about, is another tool that requires a brief install.  You'll also be asked to create your Github account, which is very important because it'll host your portfolio.  When people visit your repo on Github (if it's public), they see all the source code files you've uploaded.

### Heroku

Heroku is the cloud hosting service which we'll be using to take our web applications "live".  In some ways it acts sort of like Github because you will be pushing your code to Heroku in an almost identical way, but it's performing a very different function.  Where Github keeps repositories of your source code, Heroku actually runs that code on a server for you so your application can be visited by users.  Heroku requires a couple of helpful tools to be installed to make your life easier during the deployment process.

### HTML, CSS and Javascript

Actually, we won't need to install any of these -- they come with your web browser already!  In later courses, you may actually start using Javascript on your computer as a server-programming language (Node.js), but for now you've got nothing to worry about with these three.

### Text Editor

We recommend using a text editor like [Sublime Text 2](http://www.sublimetext.com/) to make sure everyone's using basically the same type of text editor and you'll all be able to work together and ask questions of each other without that getting in the way.  Sublime also has lots of handy shortcuts, code highlighting and other nifty features that'll make your life easier, and that's just on the surface.

Check out [this "Quick Guide to Sublime Text" from Jennifer Mann](http://jennifermann.ghost.io/a-quick-guide-to-sublime-text/) for some helpful hints and tricks.  She refers to [this tutorial (~2.5 hrs of video) from NetTuts](https://tutsplus.com/course/improve-workflow-in-sublime-text-2/) which explains some of the awesomeness of Sublime Text 2 in depth.  The first chunk of the video is the most important, don't stress out about picking up the details in the rest (but you should come back to it once you've gotten more comfortable with the editor).

### Ruby Gems

There will be some Ruby gems (which are just prepackaged little libraries of code) to install to give you the tools necessary to talk to your database and install other gems easily in the future.

### RVM

RVM is a way of making sure that each Ruby or Rails project on your computer is treated independently of each other one.  It allows you to install multiple versions of Ruby and multiple versions of Rails or any other gem on your computer and then you can choose which set to use for a given project.

This is very useful because you'll sometimes work on a project using an older version of Ruby (say 1.9.3) but simultaneously working on other projects using the newer version (2.0.0).  Since you obviously don't want to uninstall and reinstall Ruby each time, RVM just lets you say which gemset you want to use for a given project and PRESTO! your problems are solved.

### Rails

What about Rails?  Rails is actually a Ruby gem of its own since it's really just a bunch of Ruby code prepackaged for you.  You "install" it by downloading the `rails` gem.

### Mac: XCode

XCode is Apple's integrated development environment for creating Mac, iPhone and iPad applications.  Even though we won't be using it for that purpose, it's also got some command line tools that you'll be using so you're probably going to have to install it all (it's a giant package).

## Assignment: Installfest

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
