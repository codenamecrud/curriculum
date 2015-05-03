# Проект: HTML/CSS
<!-- *Estimated Time: 4-8 hrs* -->

Для этого мини-проекта вы разберете существующую веб-страницу и воссоздадите её снова. Не беспокойтесь, если ссылки не будут никуда вести и поисковая форма не будет работать, когда вы её отправите. Цель в том, чтобы начать думать о том, как элементы размещаются на странице, как они выравниваются и стилизуются. Для некоторых из вас это может быть первым разом, когда вы непосредственно попробуете создать что-то при помощи HTML (очень волнительно!).

Используйте инструменты разработчика из вашего браузера (правый клик на любом месте страницы и клик по пункту "исследовать элемент"), они станут вашими лучшими друзьями. Создайте страницу в текстовом файле с расширением .html и откройте её в своем браузере, чтобы увидеть, как она выглядит (или попробуйте использовать [CodePen](http://codepen.io/pen/) или [jsfiddle.net](http://www.jsfiddle.net)).

## Попробуйте это, прежде чем начинать

These skills will be helpful for you when you start building.  Either try them yourself or at least make sure you know how to do it:

1. Two ways to move a div around on the page
1. Stick a div onto the bottom or top of the page
1. Identify the background color of an existing webpage
1. Grab the URL for an image from an existing webpage
1. Center an element horizontally
1. Identify three ways you can include your CSS styles in a page
1. Understand how to use classes and ids to target CSS at specific elements on the page
1. Build a very basic form (even if it doesn't "go" anywhere)

## Setting Up Your Project's Github Repository (optional)

You'll want to organize all your projects as you go through the course, and the best way to do so is using Github.  It's like a file storage system for code that lives in the cloud and that can be seen by others. You already set up your Github account in the [Installations Project](/web-development-101/installations), so here we're going to put it to use.

These instructions will be the same for every project we do.  They may seem strange or odd at first (especially if you haven't officially learned about Git yet, which we do later), but don't worry -- you'll get it because you'll do it dozens of times.  If you're really frustrated, skip it the first time -- building is more important than Git right now!

1. If you haven't already, create a folder on your computer called `the_odin_project` which will house all your projects .
2. Go to your Github.com account and log in.
3. Create a new repo for this project on Github.com [by following the instructions on Github.](https://help.github.com/articles/create-a-repo) and call it `google-homepage` (instead of `Hello-World`).  Make your repository "Public" instead of "Private".
4. Go to your new repository on Github (`http://github.com/YOUR_USERNAME/google-homepage`) and take a look at it.  If you scroll down, you'll see that the `README` file you just created is what is displayed by default.
5. Download your repository to your local computer by using the `$ git clone` command.  [This should be a helpful article](http://git-scm.com/book/en/Git-Basics-Getting-a-Git-Repository)(see the second section). Basically, you'll need to get the URL for your repository (it will end with `.git`) so the `clone` knows where to grab that repo from.  You can find your repo's clone URL by checking on the right-hand column (called "HTTPS clone URL") on the repo's main page on Github.  The full command would look something like `$ git clone https://github.com/theodinproject/curriculum.git`.  It pulls your repo from your Github account down onto your local computer.
6. `cd` into your project directory on your local computer and open the `README` file in your text editor.  Change its text to include the title of the project and a link to this project on theodinproject.com.
6. Commit the updated `README` to your Github repository using the commands below on your command prompt:

    ```language-bash
    # adds all files that are in your current directory and which you've
    # recently changed to the "staging area" (ie. they're "ready to commit")
    $ git add -A

    # commits all the "staged" files into your local repository
    $ git commit -m "update README"

    # pushes your local repository up to your remote one on Github
    $ git push origin master
    ```

*When you're building your project, you will probably end up doing several `git add` + `git commit` cycles before being ready to push it up to Github with `git push`.*

You should be able to see the changes to your README on Github if you refresh the page.

*If you're not comfortable yet with using Git from the command line, you can actually just click into the README file on Github's web interface and then click the Edit button at the top to edit directly on the website.  This is covered in the second part of [the above-mentioned article](https://help.github.com/articles/create-a-repo) on creating a repo*

Note: All Git commands need to be run from inside your project's folder (the one where you typed `$ git init`) or you'll get an error!

Okay, that's enough Git for the moment -- time to actually build stuff!

## Easy Version: Build the [Google.com](http://www.google.com) homepage
(the simple one with just a search box).


Inside your project folder, create your index.html file

  1. Tips:
      * DONT BE A PERFECTIONIST!  You're just trying to make it *look* like google.com, not actually function like it and it doesn't have to be spaced exactly the same way to the pixel.  Any dropdown menus or form submissions or hover-highlighting should be ignored.
      * USE GOOGLE! You'll probably run into roadblocks where you can't figure out how to do something so do what all good devs do... Google it!
      * If you're frustrated with trying to get buttons or inputs to style the way you want (for instance, they seem to just not respond to any styles), look into the css property `-webkit-appearance: none;` or `-moz-appearance` if you're using Firefox.
  2. Start with just putting the main elements on the page (the logo image and search form), then get them placed horizontally.  You can either download the Google logo or link directly to its URL on the web in your `<img>` tag.
  3. Next do the navbar across the top, first building the content and then trying to position it.  Check out [how to build a horizontal CSS navbar](http://www.w3schools.com/css/css_navbar.asp) if you're lost.
  4. Finally, put in the footer, which should be very similar to the top navbar.
  5. In general, do as much on your own as you can before relying on the developer tools (or viewing the page's source code) to help you along.
  6. Push your project to Github using the instructions above!

## Difficult Version (optional): Build the [Google.com search results page](https://www.google.com/search?q=build+this+webpage)

You should be able to reuse much of your code from before if you started with that project.  Again, don't worry about links to nowhere and forms that won't submit and hard coding the search results (which you'll have to do of course), just focus on placement and order of items on the page.

Note: All the classes and id's and names of elements that you inspect on Google's home page are nonsensical strings (like `<div class='srg'>`).  This is because the code was **Minified** ([see the Wikipedia entry here](http://en.wikipedia.org/wiki/Minification_(programming))), which removes or shortens unnecessary characters and names to help the page load faster.  The HTML (or Javascript or CSS) file will be smaller but the browser can still read it just fine.

## Student Solutions

*Submit a link below to the github repo with your files in it by using a pull request.  See the section on [Contributing](http://github.com/TheOdinProject/curriculum/blob/master/contributing.md) for how.  Please include your partner's github handle somewhere in the description if you had one and they would like attribution.*




## Additional Resources


*This section contains helpful links to other content. It isn't required, so consider it supplemental for if you need to dive deeper into something*

If you still feel shaky on your understanding of HTML and CSS, that's okay! You don't need to be an expert by any means yet. These resources should help if you want to shore up your understanding of things:

* Watch all the [free HTML videos](http://teamtreehouse.com/library/websites/html/introduction) from Treehouse and take the quiz.
* Check out the [quickie CSS introduction](http://teamtreehouse.com/library/websites/build-a-simple-website/website-basics/introduction-to-css) from the same people as well.
* If you want to see the art of CSS, check out the [CSS Zen Garden](http://www.csszengarden.com/), which collects submissions that use identical HTML and modify only the CSS but turn out wildly different (and beautiful).
* Read through [Shay Howe's HTML&CSS Tutorial](http://learn.shayhowe.com/html-css/terminology-syntax-intro).  Lesson 1 gives a solid overview and you can do the whole thing for a more in-depth understanding.
* Learn more about github using this tutorial: https://try.github.io or read more in this article: http://readwrite.com/2013/09/30/understanding-github-a-journey-for-beginners-part-1
