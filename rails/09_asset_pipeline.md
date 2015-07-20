# Asset Pipeline

## Вступление

Вы узнали о Моделях, Вьюхах и Контроллерах. Это немало, но впереди еще множество полезных и интересных вещей, которые делают Rails еще более полезным. В этом уроке мы поговорим об Assets Pipeline и некоторых других темах, которые не совсем подходят для других уроков, но о них лучше сказать, чем не сказать.

## Пункты для размышления

*Постарайтесь ответить на предложенные вопросы. После выполнения задания попробуйте ответить на них ещё раз*

* Что такое "Asset Pipeline"?
* Что такое "файлы манифеста"?
* Зачем помещать файлы стилей в отдельные неймспейсы?
* Что значит "экранировать" HTML?

## Asset Pipeline

Ассеты в вашем приложении - это традиционно файлы, которые вызываются браузером после того, как получит первичный HTML-файл. Они включают в себя такие вещи, как CSS-стили, файлы Javascript, изображения, видео, и так далее. В общем-то все, что требует дополнительного запроса, чтобы быть полученным.

Зачастую для разработки проще всего организовать код во множество различных файлов, среди которых можно с удобством ориентироваться и перемещаться. Но если браузер будет вынужден брать пачки разных CSS-файлов, он будет брать их каждый по отдельности, а значит, процесс загрузки страницы существенно замедлится. Слишком много реквестов - и вы уничтожили положительный пользовательский опыт в вашем приложении.

Подобная организационная проблема существует в отношении хранения файлов, таких, как изображения. Их удобно хранить отдельно и в отдельной директории, но вы хотите, чтобы на них было легко ссылаться.

Rails предлагает решение всех этих проблем: собрать все воедино и отдавать браузеру по одному файлу для каждого типа. Процесс называется "конкатенацией" и выполняется как раз через Assets Pipeline. Для ваших CSS это значит, что Rails соберет каждый отдельный `.css`-файл, а затем последовательно объединит их в один большой файл. Во время этого процесса будет запущена "аглификация" (или, по-русски, "уродование") или "минификация" - программа, которая удалит все ненужные пробелы и максимально сожмет ваш файл, чтобы браузеру пришлось скачивать как можно меньший объем данных.

Точно так же Rails поступает и с Javascript-файлами - все они соединяются в один, уродуются (минифицируются), и в таком виде уже доступны для получения браузером. Гораздо лучше иметь один относительно большой файл, чем делать несколько полноценных HTTP-запросов.

### Manifest-файлы

Rails необходимо знать, какие файлы включать в этот огромный ком, и для этого он (фреймворк) использует так называемые файлы manifest. Вашим manifest-файлом для подключения javascript будет `app/assets/javascripts/application.js`. Его содержимое выглядит закомментированным, но строки, начинающиеся с `//=` сообщают Rails, какие файлы следует найти и подключить. Комментарии в файле довольно полезны - они говорят:

```language-javascript
// This is a manifest file that'll be compiled into application.js, which will include all the files
// listed below.
//
// Any JavaScript/Coffee file within this directory, lib/assets/javascripts, vendor/assets/javascripts,
// or vendor/assets/javascripts of plugins, if any, can be referenced here using a relative path.
//
// It's not advisable to add code directly here, but if you do, it'll appear at the bottom of the
// compiled file.
//
// Read Sprockets README (https://github.com/sstephenson/sprockets#sprockets-directives) for details
// about supported directives.
//
//= require jquery
//= require jquery_ujs
//= require turbolinks
//= require_tree .
```

Хелпер-метод require_tree` просто подключает все файлы, содержащиеся в текущей директории.

Ваш файл-манифест для стилей работает по такому же принципу - он доступен по адресу `app/assets/stylesheets/application.css.scss`:

```language-css
/*
 * This is a manifest file that'll be compiled into application.css, which will include all the files
 * listed below.
 *
 * Any CSS and SCSS file within this directory, lib/assets/stylesheets, vendor/assets/stylesheets,
 * or vendor/assets/stylesheets of plugins, if any, can be referenced here using a relative path.
 *
 * You're free to add application-wide styles to this file and they'll appear at the top of the
 * compiled file, but it's generally better to create a new file per style scope.
 *
 *= require_self
 *= require_tree .
 */
```

И здесь вы снова видите хелпер `require_tree`, которые подключает все файлы, расположенные в текущей директории.

Прочитав комментарии вы так же можете увидеть пару других директорий, которые подразумеваются как "локальные" и из которых так же непринужденно можно подключать файлы: это директории `lib/assets` и `vendor/assets`. Иногда, если вы начинаете использовать новый гем (например, гем для подключения Twitter Bootstrap), вам необходимо добавить файлы css и js, относящиеся к Bootstrap в файлы манифестов, чтобы быть уверенными, что приложение действительно подключит их.

### Результат

Каким будет финальный результат? Rails соберет все указанные файлы воедино и создаст один новый, название которого будет похоже на что-то вроде `application-1fc71ddbb281c144b2ee4af31cf0e308.js`. Этот бессмысленный набор символов позволяет различать файлы, если вы вносите любые изменения в css или js-код. Если бы они назывались как-то вроде `application.js`, то ваш браузер кэшировал бы их и так никогда и не узнал бы, что существует обновленный файл, потому что его название не меняется.

Но постойте, откуда браузер узнает, что нужно запрашивать файл `application-1fc71ddbb281c144b2ee4af31cf0e308.js`? Об этом мы говорили в предыдущем уроке. Теги для загрузки ассетов позволяют указать браузеру, что он должен запрашивать файл с конкретным названием. Когда вы пишете в макете приложения `<%= javascript_include_tag "application" %>`, Rails автоматически определяет, какой файл запросить, чтобы получить javascript-файл последней версии.

### Taking This Into Account in Your Code: Namespacing

Это звучит великолепно, прекрасно и ускоряет ваше приложение, но меняет ли это что-либо из того, что вы делаете? Зачастую вы можете просто забыть о файлах манифестов и продолжать писать код. В самом начале написания приложения вы можете держать все стили и js в одном файле, и ничего в итоге не изменится.

Это становится важно когда, например, у вас есть куча разных страниц и вы хотите использовать для них разные стили. Что, если вы хотите, чтобы класс `.container` на странице логина вел себя несколько иначе, чем на странице выполнения платежа? С assets pipeline Rails объединит файлы в один и вы не сможете быть уверены, какие свойства `.container` были перезаписаны другими.

Теоретически, вы можете перезаписывать стили из ваших файлов, размещенных в `app/assets/stylesheets` при помощи явных тегов `<style>` или просто в других файлах, но это лишь добавит беспорядка и полностью уничтожит смысл существования внешних стилей, ведь код уже не будет чистым.


Let's also assume that you really like user `.container` classes to keep your `<div>` elements neatly organized.  The solution is to use "Namespacing", which means that you basically nest your beneath some sort of variable or function name.  This is actually a principle that gets used a LOT, so it's important to understand it.  You'll see it with stylesheets, javascripts, modules of code and more.

The basic idea is to be able to say "all this code/css/whatever inside here only belongs to XYZ".  You sort of fence it off.  It's best explained with an example:

```language-ruby
    # app/views/users/show.html.erb
    <div class="user">
      <div class="container">
        <!-- a bunch of code for displaying the user -->
      </div>
    </div>
```

Now this container and all the code inside of it is also within the `.user` class.  So we can set up our stylesheet to specifically address the `.container` class that's inside a `.user` class:

```language-ruby
    # app/assets/stylesheets/user.css.scss
    # Note: I'm not going to use SCSS code because we haven't covered it yet
    .user .container{
      // style stuff
    }
```

This is good because we're now specifically targeting containers used by User pages.

The same principle applies to javascript, though I won't cover it here because that's material for a later course.

So any time you want to make only a portion of your stylesheets or javascript code available to a specific set of views, try namespacing it.

### Rails in Development

The asset pipeline functions a bit differently in development mode.  If you look at your Rails server output when you're working with a webpage in the local environment, it actually sends out a whole bunch of stylesheets and the like.  This is just to give you the ability to debug easier.

### Images

For images, the asset pipeline keeps them in the `/assets` directory unless you've made your own subdirectories.  Use `image_tag`'s to avoid confusion, e.g. `<%= image_tag "fuzzy_slippers.jpg" %>`.

### Preprocessors

Remember the preprocessors we talked about in the previous lesson on Views?  Filetypes like ERB and SASS and HAML and Coffeescript all get preprocessed as part of the pipeline.

## Un-Escaping HTML

Let's say you're building a blog and you want to be able to write posts that include HTML code.  If you just write something like `this is the <strong>BODY</strong> of my post` and then try to display it in a view later, the `<strong>`tags will just be regular text... they will literally say '\<strong\>'.  That's called "escaping" the characters.

To get your views to actually render HTML as HTML, you need to let Rails know that the code is safe to run.  Otherwise, it's easy for a malicious attacker to inject code like `<script>` tags that cause major issues when you try to render them.

To tell Rails a string is safe, just use the method `raw` in your view template, for example:

    <%= raw "<p>hello world!</p>" %>   <!-- this will create real <p> tags -->

If you don't want to rely on Rails' native behavior and would like to make absolutely sure the HTML does not get run, use the `CGI` class's `escapeHTML` method, e.g.

```language-ruby
    CGI::escapeHTML('usage: foo "bar" <baz>')
    # => "Usage: foo &quot;bar&quot; &lt;baz&gt;"
```

## Your Assignment

Some necessary and straightforward reading on the Asset Pipeline:

1. Read [Rails Guides on the Asset Pipeline](http://guides.rubyonrails.org/asset_pipeline.html) sections 1 to 3.


## Conclusion

The Asset Pipeline isn't something that you often think about, especially when just building little toy apps, but it becomes important to understand as soon as you want to deploy your application (because you'll need to take it into account, which we'll talk about in that lesson later) or work with anything but the vanilla asset structure.

## Additional Resources

*This section contains helpful links to other content. It isn't required, so consider it supplemental for if you need to dive deeper into something*


* [Ryan Bates' asset pipeline Railscast](http://railscasts.com/episodes/279-understanding-the-asset-pipeline?view=asciicast)
* [Stack Overflow on Escaping HTML in Rails](http://stackoverflow.com/questions/692921/rails-how-to-html-encode-escape-a-string-is-there-a-built-in)
