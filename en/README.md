# Porres's Puredata tutorial (Developer Guidelines)

Porres made the original work. Lunhani make a "translation", in sense that PD patchs can be executed in [WebPD]({{ webpd.website }}) environment (or at least, the available [things](https://github.com/sebpiq/WebPd/#list-of-implemented-objects-and-other-limitations)).

This guide line was made to help other PD fans contribute to this book. So we describe some topics to improve:

## Work

Many people can help. If you have an ability, like language, you can help translate. If you know javascript, you can help adding some chunks of code. If you know PD, you can help convert PureData patches. But, above of all, you will need to know:

* Git:

	* The [Git](http://git-scm.com/)'s webpage says: "Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency". This [guide](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) will help you. But, for eletronic musicians, what the fucking hell is this?

	* Imagine you made some funny patches. But today is working, and tomorrow not. And them change the code. Now is working. Then you share the code with a friend. But the patch won't work in his or her computer. Maybe you write with a library that exist in a Unix system, but not in Windows system.

	* If these three versions codes have been versioned, you could investigate and customize each version, and help other peoples to improve a default version. The patch will no longer be mine. But our. It's a very scientific way to improve texts and softwares.

* A Github  account. Is very popular among programmers.It is the ("git entity")[https://www.github.com], like a friend of mine says...

* Read some content from [Gitbook help page](https://help.gitbook.com/). Gitbook is, in summary way, a methodology to write multimidiatic books. You can see in a webpage, or download in a printable format.

* A javascript runtime environment. More information [here](https://nodejs.org/en/)

* If you know javascript, read some content about Node.js and Npm

## Download

To download this project, and knowing git, you will go to terminal, and type:

    $ git clone https://www.github.com/jahpd/porres_tutorialpd.git
	
	
### Node.js and NVM

So, you will need node.js. So creationix proposed use [nvm](https://github.com/creationix/nvm). Read NVM's README and you will be fine in UNIX systems (linux and OSX). This will install `node` and `npm` commands. But first, ensures the node's version. This gitbook is using node version `4.2.2`, so:

    $ nvm use 4.2.2
	

## Returning to download

Install dependencies. You will need `gitbook` installed globally. Go to tutorial folder and install them:

	$ cd porres_tutorialpd/
    $ npm install gitbook -g
    $ gitbook install
	

## Running in local machine

To run locally, you do this:

    $ gitbook serve


Or

    $ gitbook build
    $ cd _book
    $ python -m SimpleHTTPServer


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

## Testing

This is (or i hope so) the Hi.pd file from original example in _01.Introduction/1.Presentation/Hi.pd_ . Uses a `print` object to print a Hello world message:

{% patch %}Hi_1.pd{% endpatch %}

You can invoke a PD patch like the below:

    {% patch %}Hi_1.pd{% endpatch %}

This patch:

{% patch %}Hi_2.pd{% endpatch %}

Is invoked as:

    {% patch %}Hi_2.pd{% endpatch %}

And so on... (this where we realy need pd developers)

To assign a patch, you need to modify them [here](https://www.github.com/jahpd/gitbook-plugins-webpd_porres_examples), and update `index.js` that assign where patches are located.

    


