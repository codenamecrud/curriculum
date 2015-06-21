# Проекты: Ruby в сети

*Не забывайте использовать Git для фиксации изменений в ваших проектах!*

## Проект 1: Спамбот для Твиттера

Вы уже кратко знакомы с тем, как использовать Ruby для отправки запросов и анализа ответов. Когда вы будете создавать реальное веб-приложения, вам часто будет необходимо взимодействовать с другими приложениями через API.
Если вы не очень хорошо знакомы с API, то вот он ваш шанс. В данном случае Twitter дает вам доступ к связке часто используемых команд (например, отправить твит, доступ к фолловерам и т.д.), но с помощью вашей собственное программы, вместо того чтобы нажимать кнопки на сайте Twitter. Собственно, поэтому это и называется Интерфейс Прикладного Программирования (Application Programming Interface)... Ваше приложение может получить программный доступ к другой системе.
Когда компании делают свои API публичными, они обычно хотят ограничить количество спама и злоупотреблений. Для этого они заставляют пользователей аутентифицироваться при каждом запросе. Как правило, при регистрации приложения в публичном API выдается ключ, используемый для проверки подлинности ваших запросов. Иногда это простая подстановка ключа в URL строку запроса, но в настоящее время часто используется и другой, более гибкий и безопасный способ аутентификации.
Протокол, который обычно используется для этого, называется OAuth. В нашем случае Twitter использует OAuth, и этот же протокол (возможно другую версию, сейчас существуют две мажорных версии протокола) вы будете использовать, если захотите взимодействовать с Facebook, Instagram, Tumblr и пр. Так что стоит получить некий опыт работы с OAuth. Этот протокол не всегда интуитивно понятен, просто стоит помнить, что его основное предназачение в том, чтобы убедиться что запрос приходит именно от авторизованного пользователя API. Если вы создали ключи для работы с Github на предыдущих этапах, то работа с OAuth не сильно отличается от тех действий.
Заметим, что возможно вам стоит завести отдельный аккаунт на Twitter (мой - @ SpamBot26103678), потому что есть вероятность случайно превысить лимиты данных или скорости, или других антиспам механизмов и отправить много тестовых твитов. Нет смысла подвергать риску быть забаненным свой основной аккаунт.

### Ваша задача

1. [Выполните этот проект от Jumpstart Lab](http://tutorials.jumpstartlab.com/projects/microblogger.html). На нем вы научитесь аутентифицироваться и отправлять твиты.
2. Не переживайте насчет последней части Klout.

## Проект 2: настоящий веб сервер и браузер (в консоли)

Одна из причин выполнить этот проект - это узнать как Ruby взаимодействует с веб, потому что это имеет прямое отношение к тому что вы будете делать позже используя Rails. Фреймворк Ruby on Rails - это просто аккуратно упакованный Ruby код. Все что делает Rails, вы можете сделать самостоятельно (учитывая время) с некоторым знанием Ruby.
В данном случае вы будете делать простой веб сервер, который получает запросы и посылает ответы, основанные на запросах. Вы также можете создать простой браузер, который будет посылать запросы - тогда ваш сервер и ваш браузер смогут говорить друг с другом! После выполнения этого проекта, веб должен быть менее «магическим» и таинственным для вас и стать просто полным интересных задач.
В проекте много этапов, и вам надо будет опираться на некоторые из ваших предыдущих знаний, такие как: работа с файлами, и, возможно, регулярные выражения для разбора строки.

### Дополнительные материалы:

Из [Ruby 1.9.x буклет веб-серверы](http://www.scribd.com/doc/20755982/The-Ruby-1-9-x-Web-Servers-Booklet):
> Пример веб сервера
> По сути любой веб сервер - простой бесконечный цикл, который пытается принять соединение на прослушиваемом сокете. Вот очень простой TCP сервер:

```ruby
require 'socket'

# IP address is 0.0.0.0 and it's on port 8080:
server = TCPServer.new("0.0.0.0", 8080)
loop do
    connection = server.accept
    inputline = connection.gets
    ...
    connection.puts outputline
    connection.close
end
```

> серверы отличаются тем, как в них реализован этот цикл и как они обрабатывают входящие соединения. Пример выше показывает блокирующий сервер. Это значит что он может обрабатывать только одно соединение в один момент времени, а остальные запросы будут ожидать пока текущий запрос будет выполнен. Запросы которые выполняются долго могут сделать сервер недоступным на какое-то время. А группа таких запросов быстро сделает сервер невозможным для использования. Существуют несколько стратегий для предотвращения такого поведения сервера. Мы обсудим их  и посмотрим как они реализованы в разных серверах.
> Для того чтобы сервер можно было назвать веб (HTTP) сервером, он должен «общаться» на языке HTTP протокола. Следовательно нам необходим способ разбора входящих HTTP запросов. Каждый серверов предоставляет свой способ решить эту задачу. Но вскоре мы увидим что большинство из них полагаются в этом на какой-либо клон парсера от сервера Mongrel. Если мы включим поддержку HTTP в наш сервер, это будет выглядеть примерно так:

```ruby
require 'socket'
server = TCPServer.new("0.0.0.0", 8080)
loop do
  connection = server.accept
  request = HTTP.parse(connection.gets) # an imaginary HTTP parser
  ...
  connection.puts status
  connection.puts headers
  connection.puts body
  connection.close
end
```

Здесь `socket` - библиотека доступная в Ruby без необходимости скачивать что-то отдельно (это часть стандартной библиотеки, вам надо просто указать Ruby включить (`require`) ее).
В случае с веб сервером действует похожий принцип как и с файлами. Ожидаемый от сервера ответ, просто длинная строка символов или двоичных данных как и файл. Шаги для работы файлами и сервервами практически идентичны:
1. Вам надо сообщить Ruby где находится «файл» (какой IP адрес и какой порт мы отслеживаем?)
2. Открыть файл (или сокет на удаленном сервере)
3. Послать запрос, чтобы начать чтение файла (или что вы хотите сделать на удаленном сервере)
4. Прочесть содержимое файла (или ответ сервера)
5. Закрыть файл (или соединение с сервером)

Круто!

### Ваше задание

1. Прочтите (если еще не прочитали) это [обьяснение как работает HTTP](http://www.jmarshall.com/easy/http/#whatis) до момента где говорится о POST методе (примерно середина).
2. Прочтите этот краткий [туториал по программированию сокетов на Ruby](http://www.tutorialspoint.com/ruby/ruby_socket_programming.htm) от TutorialsPoint, не обращайте много внимания на материал про мультиклиентные серверы, но продолжайте читать и после него.
3. В одном файле реализуйте их "SimpleServer", это легко сделать простым копипастом, но убедитесь что понимаете, что делает каждая строка кода.
  1. Готовы к взрыву мозга? Когда вы вызываете `TCPServer.open`, метод класса `::open` АБСОЛЮТНО тот же самый, что используется в тот момент когда вы вызываете `File.open`, потому что `TCPServer` наследует его (через несколько уровней) от того же самого класса `IO`, как и класс `File`. Другими словами, работа с серверами очень похожа на работу со строками.
  2. `#accept` - просто метод инстанса класса `TCPServer`. Он ждет связи, и когда связь установлена, он возвращает экземпляр `TCPSocket`, представляющий эту связь ([см документацию](http://www.ruby-doc.org/stdlib-1.9.3/libdoc/socket/rdoc/TCPServer.html)).
  3. Теперь когда вы выполняете `#puts` в этот сокет, он поднимается на другой стороне вашим клиентом. Никакой магии, просто поток байтов, как ввод в `STDIN` из командной строки с помощью `#gets`, или вывод в `STDOUT` с помощью `#puts`.
4. В другом файле реализуйте "Simple Client", это должно *действительно* быть похоже на работу с файлами. `localhost` просто представляет адрес вашего компьютера (в отличие от, скажем, `http://www.google.com`). Всякий раз когда вы разрабатываете свое веб приложение, и вам необходимо тестировать его локально перед тем, как выложить его на сервер, вы запускаете локальный веб сервер, чей адрес будет `localhost` и номер порта (часто 3000, но можно выбрать произвольный порт). Так что познакомтесь с ним.
5. В одной вкладке вашего терминала запустите свой сервер. Нажмите `CTRL + c` чтобы прервать бесконечный цикл, когда захотите остановить сервер.
6. В другой вкладке запустите своего клиента. Вы должны увидеть то что вы «велели» вашему серверу вывести в консоль. **Поздравляем, вы только что сделали свой сервер**
7. Теперь давайте немного усложним. Реализуйте "A Tiny Web Browser" из одноименной статьи на TutorialsPoint (первую версию), это, в основном, то же самое что вы делали раньше, только указывая `web`, а не `localhost`.
8. Создайте HTML файл и сохраните его с именем `index.html`. Он должен выглядеть примерно так:

```html
<html>
  <body>
    <h1>Welcome to the Viking Home Page</h1>
  </body>
</html>
```

8. Теперь начнем небольшую развлекательную часть. Измените ваш сервер, чтобы он принимал HTTP запросы от браузера, и, если произведен GET запрос к `/index.html`, возвращал содержимое файла `index.html`.
  1. Вам будет необходимо парсить входящий запрос самостоятельно, чтобы определить какой HTTP глагол был использован, какой файл был запрошен и прочую служебную информацию, которая обычно содержится в HTTP запросе. Опять же посмотрите  [примеры](http://www.jmarshall.com/easy/http/#whatis), как должны выглядеть HTTP запросы. Самой простой способ может быть - использование регулярных выражений.
  2. Отправьте свой правильно оформленный HTTP ответ, включающий код статуса `200`, если файл найден, и актуальное содержимое запрошенного файла. Не забудьте включить в ответ размер (в символах) исходящего файла (это нормальная часть каждого HTTP ответа), чтобы помочь вашему мини-браузеру правильно отобразить файл.
  3. Если запрошен файл, которого не существует на сервере, отправьте код ошибки `404` и соответсвующее (или несоответсвующее) сообщение об ошибке.
9. Измените свой простой браузер так, чтобы он отправлял соответсвующий GET запрос на сервер, как вы делали это раньше с комбинацией клиент/сервер. Проверьте как он работает... Вы должны быть в состоянии запросить и получить файл `index.html` (и вывести его в терминал)! Вам понадобится вспомнить некоторые команды, которые вы использовали для открытия файлов. Вы также должны настроить клиент так, чтобы определить сообщение об ошибке от сервера и отобразить его.
10. Создайте еще один html файл `thanks.html`. Он должен выглядеть примерно так:

```html
<html>
  <body>
    <h1>Thanks for Posting!</h1>
    <h2>Here's what we got from you:</h2>
    <ul>
      <%= yield %>
    </ul>
  </body>
</html>
```

11. Теперь настройте свой мини-браузер, так чтобы он отправлял еще и POST запросы. Там где мы раньше делали вид, что просматриваем страницы, теперь мы собираемся сделать вид, что нажимаем кнопку "Отправить" на форме.
  1. Измените свой клиент, так чтобы она спрашивал пользователя какой запрос посылать.
  2. Если пользователь хочет отправить POST запрос, представьте что вы регистрируете викинга для участия в набеге. Попросите пользователя внести данные викинга, такие как`name` и`email`.
  3. Храните пользовательские данные в хеше, который может выглядеть примерно так `{:viking => {:name=>"Erik the Red", :email=>"erikthered@theodinproject.com"} }`. Почему хеш внутри хеша? Просто именно так будут выглядеть данные, которые браузер посылает из формы, сгенерированной с помощью Rails. Можно использовать и обычный хеш, но это будет не так весело.
  4. При отправке POST запроса, включите этот хеш данных в запрос (опять [смотрите примеры здесь](http://www.jmarshall.com/easy/http/#postmethod)). Если вы захотите использовать JSON для передачи своего хеша, вам стоит добавить `require 'json'` в ваш сервер и клиент для того чтобы использовать библиотеку JSON.
  5. Метод, который конвертирует ваш хеш в чистый JSON для упрощения HTTP передачи, называется `#to_json`.
  6. Вам также потребуется включить размер данных, которые вы отправляете в поле `Content-Length` HTTP пакета.
12. Наконец, настройте свой сервер, чтобы он мог распознать и ответить на POST запрос.
  1. Если сервер обнаруживает POST запрос, он должен определить и разобрать данные из JSON из него (вам может помочь поле `Content-Length`)
  2. Конвертируйте JSON строку обратно в объект, с помощью `JSON.parse` и сохраните его в хеш `params` (опять же потому что Rails называет этот хеш `params`). Ваш код может выглядеть примерно так:  `params = {}; params << JSON.parse(the_post_JSON_string_here)`.
  3. Теперь откройте свой файл `thanks.html` и (не меняя оригинального файла, так как мы будем использовать несколько раз) используйте скрипт, чтобы заменить `<%= yield %>` на `<li>` для каждого элемента данных, которые были введены в "форму" браузера. Выведите их в любом формате как вам удобно, например: `<li>Name: Erik the Red</li><li>Email: erikthered@theodinproject.com</li>`.
  4. Теперь отправьте измененный файл в браузер и выведите его на экран.
13. Поиграйте со своим новым браузером. Попробуйте отправлять разные вещи в поля `name` и `email`, и смотрите как меняется ваш html. Никакой магии, только HTTP и Ruby.

Святая корова! Вы только что сделали свой консольный веб-браузер, который может отправлять правильные HTTP запросы, и свой сервер, который корректно принимает запросы, загружает файлы, изменяет эти файлы, на основе полученных данных и возвращает их в браузер. Потратьте секунду чтобы погладить себя по спине.
Теперь подумайте о том, что вы сделали. Пусть некоторые шаги кажутся странными, например имя хеша `params` или замена строки в файле `thanks.html` `<%= yield %>` динамическим содержимым. Это те вещи которые делает Rails. Иными словами, вы сделали небольшой кусочек Rails. Хорошая работа.

## Дополнительные материалы:

*Этот раздел содержит полезные ссылки на дополнительные материалы. Они не обязательны, так что расценивайте их как нечто полезное, если вы хотите поглубже погрузиться в тему*

* [Проект веб сервер на Ruby от Tuxradar](http://www.tuxradar.com/content/code-project-create-web-server-ruby)
* [Туториал от Люка Франкла по созданию файл сервера](https://practicingruby.com/articles/implementing-an-http-file-server)