# Проект: Отправка электронных писем в Ruby on Rails

*Не забывайте использовать Git для фиксации изменений в ваших проектах!*

## Проект: Отправка приветственных писем

Настройка отправки электронных писем является достаточно простой задачей и очень напоминает создание нового контроллера или представления. После того как сделаете это пару раз, все будет делаться естественным образом.

### Ваша задача

Стряхните пыль с [проекта по заказу авиабилетов](/ruby-on-rails/building-advanced-forms) (или с одного из других проектов, где есть регистрация пользователей) и сделайте отправку электронного письма с текстом "Вы заказали электронный билет" каждому пассажиру, когда он совершит заказ.

1. Найдите и загрузите файл проекта.
2. Сделайте несколько отжиманий и попрыгайте на месте. Последнее время вы проводите за компьютером слишком много времени.
2. Сгенерируйте новый мэйлер командой `$ rails generate mailer PassengerMailer`.
3. Установите [гем `letter_opener` (смотрите документацию)](https://github.com/ryanb/letter_opener), чтобы открывать ваши электронные письма в браузере вместо отправки в окружении для разработки.
3. Следуйте шагам из [Rails-гайда](http://rusrails.ru/action-mailer-basics), чтобы создать действие для отправки благодарственного электронного письма.
4. Сделайте две версии благодарственного электронного письма для авиабилета `.html.erb` и `.text.erb`.
5. Проверьте отправку электронных писем создав новый заказ на авиабилет (гем `letter_opener` должен открыть его в браузере, если все настроено верно).
6. Попробуйте еще такой трюк, вызовите мэйлер напрямую из консоли Rails используя что-то подобное `> PassengerMailer.thank_you_email(Passenger.first).deliver!`.
7. Дополнительное задание: cделайте деплой на Heroku и проверьте как это работает. Если вы это сделаете, то будет несколько дополнительных настроек, добавьте [аддон SendGrid (смотрите документацию)](https://devcenter.heroku.com/articles/sendgrid) и убедитесь, что конфигурация настроена верно. В документации описано как это сделать.

### Решения студентов

* [Решение 1](https://github.com/Jberczel/Flight_Booker) | [посмотреть в браузере](http://flight-booker.herokuapp.com/)
* [Решение 2](https://github.com/donaldali/odin-flight-booker) | [посмотреть в браузере](http://dna-flight-booker.herokuapp.com/)
* [Решение 3](https://github.com/imousterian/FlightBooker) | [посмотреть в браузере](https://one-way-ticket.herokuapp.com/)
* [Решение 4](https://github.com/Rodic/private-events)
* [Решение 5](https://github.com/dstodolny/odin-flight-booker)
* [Решение 6](https://github.com/KevinMulhern/flight_booker) | [посмотреть в браузере](https://odin-booker.herokuapp.com/)
* [Решение 7](https://github.com/AtActionPark/odin_flight_booker)
* [Решение 8](https://github.com/antrix1/flight-booker) | [посмотреть в браузере](https://blooming-mountain-4761.herokuapp.com/)
* [Решение 9](https://github.com/dchen71/odin-flight-booker) | [посмотреть в браузере](http://true-syrup-4655.herokuapp.com/)

## Дополнительные ресурсы

*Этот раздел содержит полезные ссылки на дополнительные материалы. Они не обязательны, так что расценивайте их как нечто полезное, если вы хотите поглубже погрузиться в тему*

* [Документация по гему `letter_opener`](https://github.com/ryanb/letter_opener)
* [Создание мэйлера в Rails 3](http://railscasts.com/episodes/206-action-mailer-in-rails-3) (также должно работать в Rails 4).
* [Настройка электронной почты: Rails, Heroku, SendGrid, Figaro](http://howilearnedrails.wordpress.com/2014/02/25/setting-up-email-in-a-rails-4-app-with-action-mailer-in-development-and-sendgrid-in-production-using-heroku/comment-page-1/#comment-79)
