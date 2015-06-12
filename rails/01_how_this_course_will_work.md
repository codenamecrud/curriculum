# Как будет работать этот курс

Добро пожаловать в Rails! Возможно, вы сразу начали с этого курса (если вы хотите начать делать сайты), или вы уже прошли курс, посвященный Ruby и имеете крепкую основу для изучения Rails. В любом случае, мы здесь неплохо повеселимся.

Вы уже должны иметь представление о том, что такое Rails, поскольку мы рассказывали об этом в предыдущих уроках (смотрите раздел "Что нужно знать" чуть ниже). Теперь пора воспользоваться приобретенными теоретическими знаниями и начать создавать сайты. Эта часть учебного плана будет больше сосредоточена на практических задачах, нежели остальные. Вам по-прежнему придется читать документацию, посты в блогах и смотреть видео перед написанием кода, но в основном мы будем больше сосредоточены на практических проектах.

После каждого урока или двух вам будет дана задача: создать один или несколько независимых проектов, удовлетворяющих изученным концепциям (что мы и делали до текущего момента). Так же вам нужно будет пройти 1-2 главы из [Туториала по Ruby on Rails](http://rails.method.kz) Майкла Хартла (по ссылке доступен русскоязычный перевод последней версии руководства).

Этот туториал нередко оказывается излишне глубоким для новичков в Rails, но мы будем использовать его как пример создания большого цельного проекта, по одной главе за раз по мере того, как вы проходите уроки этого курса. У вас должно будет сложиться лучшее представление о том, что происходит в руководстве, чем у типичного новичка, поскольку мы будем рассматривать каждый соответствущий принцип перед тем, как непосредственно писать код, следуя руководству.



## План действий

Мы начнем с обзора таких важных тем, как HTTP, MVC, REST, API, Cookies и аутентификация, чтобы немного освоиться в них прежде, чем взяться за самое интересное.

Мы будем двигаться "задом наперед", начав с роутинга, затем будут контроллеры и представления (так же их называют "вьюхи" (views)), чтобы сделать функциональный (хотя пока и не особо красивый) интерфейс для отображения данных. Далее вы узнаете о хранении и поиске информации в базах данных при помощи SQL и о том, как обернуть этот SQL в запросы Active Record. Затем мы расскажем о формах, области, которая намного больше действует "за кулисами", чем вы ожидали, об аутентификации, которая является ключом к безопасности вашего приложения. Завершим изучением таких полезных тем, как состояния и assets pipeline, чтобы плавно закрыть начальный этап изучения Rails.

Но мы не можем здесь остановиться, так что придется вернуться к ActiveRecord и дать вам инструменты, которые реально заставят ваши данные плясать, а так же больше рассказать о формах, которые нужны, чтобы предоставлять пользователю расширенные возможности. Это действительно важная часть Rails, так что мы потратим некоторое время на её изучение.

Наконец, мы рассмотрим еще несколько полезных тем: отправка почты из вашего приложения, создание и взаимодействие с API, шаблоны дизайна, метапрограммирование и продвинутый роутинг. Эти темы будут освещены до того, как вы возьметесь за создание финального проекта.

## Наши инструменты и тексты

The most important resources that we'll leverage are the [Rails Guides](http://guides.rubyonrails.org/) and the [Ruby on Rails Tutorial](http://ruby.railstutorial.org/ruby-on-rails-tutorial-book).  Together, they comprise a near-complete set of open-source resources for learning Rails.

The Guides are comprehensive, basically a completely open-source textbook and reference manual for Rails.  At times they'll get a bit more technical than you might like, and it may be okay to skim some of that.  When you Google for a solution later, if it's not showing up on Stack Overflow then it's probably going to give you a link to the Guides.

The Ruby on Rails Tutorial (aka the Hartl Tutorial, after its author) is another open source resource which builds (over several hundred pages) a full featured web application (Twitter clone), including introducing you to testing your code using RSpec along the way.

My typical workflow for a long time went sort of like this:

1. I know I want to implement a feature... Google search to see if anyone implemented the same feature.  Land on a Stack Overflow post that describes how to implement a similar feature.
2. The SO post shows me the right direction to take, so I Google for the specific method it mentioned that I don't understand.  I end up on the Rails Guides page that talks about it.
3. I pull up my completed version of the Rails Tutorial to make sure I've got the syntax correct and possibly to help write tests while I implement the feature.

As you can see, I frequently relied on the main resources you'll be learning from and you'll find them to be helpful long after you've completed this course, so it makes sense to get familiar with them!

## Prerequisites

**If you haven't completed these, be sure to do so before getting started:**

* Your software should be installed, as listed in the [Installfest section](/web-development-101/installations).
* You should really have gone through the full [Web Development 101](/web-development-101) course, but the most important parts are listed below.

    * Read the full [Back End section](/web-development-101/#section-the-back-end) of the Web Development 101 section for an introduction to Ruby.
    * Complete at least the full [Basic Ruby](/web-development-101/ruby-basics) lesson (all readings and projects) to have a solid grounding in Ruby basics.
    * Read the [Rails portion of the Web Development 101](/web-development-101/ruby-on-rails-basics) section for an overview of Rails.
    * Build the [Rails project from the Web Dev 101 section](/web-development-101/ruby-on-rails) to get your hands dirty with Rails first.

## Additional Resources

*This section contains helpful links to other content. It isn't required, so consider it supplemental for if you need to dive deeper into something*

* [StackOverflow: Summary of Ruby on Rails Fundamental Concepts](http://stackoverflow.com/questions/5205002/summary-of-ruby-on-rails-fundamental-concepts)
* If you want to dive right into a full on interactive Rails course in the browser, give [Code Learn](http://www.codelearn.org/ruby-on-rails-tutorial) a shot (and let us know what you think)
