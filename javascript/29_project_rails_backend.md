# Проект: Использование бэкенда на Rails для создания "Где Уолли"

Этот проект наконец дает возможность связать воедино все то, что вы так долго изучали. Это сложный проект, так что задачи лучше решать постепенно, шаг за шагом. Хотя работа с бэкендом на Rails относительно проста, вам придется повозиться и с функциональностью во фронтенде. Эта задача похожа на те, с которыми сталкиваются настоящие программисты в своей работе. Вы готовы???

Надеюсь, вы играли в "Где Уолли" ([если нет, то посмотрите информацию здесь](https://ru.wikipedia.org/wiki/Где_Уолли%3F)), будучи ребенком. Вам дается фотография, полная предметов, на которой вы должны найти несколько определенных вещей.

## Ваше задание

Ваша программа будет похожа на приложение для создания фотометок (тэгов). Возьмите большое фото с изображениями, которые предстоит найти пользователю, например с Уолли, Волшебником и Вильмой... или назовите своим именем, поместив свои фотографии. Пользователь будет делать выбор между именами, а программа определит, угадал он или нет.

Для начала, выберите фотографию, определите место расположения персонажей на ней и занесите его в базу. При клике на фотографии, на месте клика должна создаваться область выбора, содержащая список персонажей.

После выбора пользователем одного из них, с помощью бэкенда вы должны проверить, содержится ли выбранный пользователем персонаж в указанной области. Сообщите пользователю о результате (если он ошибся, выдайте соответствующее сообщение). Если же ответ верный, то пометьте маркером этот участок карты. В любом случае, удалите выбранную область перед тем, как пользователь кликнет еще раз.

Отслеживайте время между первой загрузкой фотографии и угадыванием всех персонажей (это необходимо делать на сервере, иначе пользователь может изменить свой результат). После окончания игры, запросите у пользователя его имя и впишите его время в таблицу рекордов.

1. Создайте репозиторий на Github для проекта. Если возникли сложности, посмотрите инструкции на [этой странице](/basics-of-web-development/project-html-css).
2. Подумайте, что вам будет необходимо для получения работающего приложения. Настоятельно рекомендую в данном проекте набросать схему на бумаге перед тем, как вообще садиться за компьютер. Лучше сейчас подумать несколько лишних минут, чем потом переделывать программу, теряя часы впустую.
3. Создайте приложение, которое на данный момент будет содержать только код, загружающий HTML страницу.
4. Создайте фронтенд, который пока не обращается к бэкенду. Особенно это касается создания кода Javascript, который при нажатии пользователем на фотографии выделяет на ней участок и раскрывает выпадающее меню, а при повторном нажати его убирает.
5. Создайте валидацию с бэкендом, проверяющую, кликнул ли пользователь на какого-либо персонажа.
6. Свяжите ее с фронтендом, чтобы вы могли легко выбирать персонажей, сравнивать их и помечать фотографию маркером, если выбор оказался правильным.
7. Добавьте возможность вести тайминг от загрузки страницы, отображайте "счет" (время) до момента угадывания всех персонажей. Создайте всплывающее окно для ввода имени, если пользователь попал в таблицу рекордов.
8. Играйте!
9. Отправьте проект на Github. Это серьезный проект, примите поздравления!

### Опционально:

1. Загрузите несколько изображений в базу данных и позвольте пользователю выбрать одну из них перед игрой.


## Решения студентов

* [Решение 1](https://github.com/donaldali/wheres-waldo) | [Посмотреть в браузере](http://dna-wheres-waldo.herokuapp.com/ "Where's Waldo")
* [Решение 2](https://github.com/AtActionPark/odin_waldo) | [Посмотреть в браузере](https://hidden-sierra-6699.herokuapp.com/)


## Дополнительные ресурсы

*Этот раздел содержит полезные ссылки на дополнительные материалы. Это не обязательно, так что расценивайте их как нечто полезное, если вы хотите поглубже погрузиться в тему*
