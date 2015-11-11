# Porres's Puredata tutorial (Developer Guidelines)

Porres made the original work. Lunhani make a "translation", in sense that PureData patchs can be executed in [WebPD]({{ webpd.website }}) environment (or at least, the available [things](https://github.com/sebpiq/WebPd/#list-of-implemented-objects-and-other-limitations)).

This guide line was made to help other PD fans contribute to this book. So we describe some topics to improve:

## Work

Many people can help. If you have an ability, like language, you can help translate. If you know javascript, you can help adding some chunks of code. If you know PD, you can help convert PureData patches. But, above of all, you will need to know GIT (see more about them in GLORSSARY)

- Git installed. 
- A Github  account;
- Read some content from Gitbook help page
- If you know javascript, read some content about Node.js and Npm

## Download

To download this project, and knowing git, you will go to terminal, and type:

    $ git clone https://www.github.com/jahpd/porres_tutorialpd.git

Install dependencies. You will need `gitbook` installed globally:

    $ npm install gitbook -g

Go to tutorial folder and install them:

    $ gitbook install

## Running in local machine

To run locally, you do this:

    $ gitbook serve

Or

    $ gitbook build
    $ cd _book
    $ python -m SimpleHTTPServer

[Here](01.Introduction/1.Presentation/Hi.md), you can see some results.

## TODOS

{% for todo in book.todos.en %}
  - {{ todo.name }}: {{ todo.description }}
{% endfor %}

## Changelog

{% for log in book.changelog %}
  - {{ log.version }}: {{ log.description }}
{% endfor %}

## Authors

{% for author in book.authors %}
  - [{{ author.name }}]({{ author.website }})
{% endfor %}