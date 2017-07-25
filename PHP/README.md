# PHP - Intro to PHP class

## First Offering

* Instructor: [Stacy Davis](https://gdimpls.slack.com/messages/@hurrendor)
* July 10, 17, 24 2017
* TA's:

  - [Jeanne]()
  - [Clare]()
  - [Stephanie O]()
  - [Tamara](https://gdimpls.slack.com/messages/@tamouse)

## Class Materials

The class materials can be found
at <https://github.com/hurrendor/gdi-featured-php-mysql/>.

* Day 1
  * Slides: <http://hurrendor.com/gdi-php-mysql/class1.html>

* Day 2
  * Slides: <https://hurrendor.github.io/gdi-featured-php-mysql/class2.html>
  * Project files: <https://github.com/hurrendor/gdi-featured-php-mysql/blob/gh-pages/class2-codesample.zip>

* Day 3
  * Slides: <https://hurrendor.github.io/gdi-featured-php-mysql/class3.html>
  * Project files:
    * Excerises: <https://github.com/hurrendor/gdi-featured-php-mysql/blob/gh-pages/class3-exercises.zip>
    * Completed: <https://github.com/hurrendor/gdi-featured-php-mysql/blob/gh-pages/class3-complete.zip>


## Links and Notes

### Use the mysqli library

PHP has two MySQL libraries:

- `mysql` is an old, outdated, and vulnerable interface. **DO NOT USE
  IT**
- `mysqli` is "MySql, Improved" and is by far the preferred
  interface. **Make sure all your database methods use mysqli**.

(Sometimes, depending on which editor you use, you may get the old,
non-improved, methods offered up to you. Be careful when you select a
method.)

In the PHP documentation, the `mysqli` library shows two forms: the
Object form and the Procedural form. In class, we were using the
Procedural form. The documentation can sometimes get confusing as the
Object form seems to be preferred by most people. It is perfectly okay
to keep using the Procedural form.


### Turn on all php error reporting

When learning, and during development, put `error_reporting(-1);` at
the very beginning of the file, the first thing following the
opening `<?php` tag. The start of each PHP file should look like
this:

```php
<?php error_reporting(-1);

// rest of code follows
```

To learn more about error_reporting,
see <http://php.net/manual/en/function.error-reporting.php>.

### Make sure you set the right credentials for using the database

If you're using MAMP on macOS, the credentials for connecting to the
database system are:

* host: "localhost"
* user: "root"
* password: "root"

On XAMPP for either Windows or macOS, the credentials are:

* host: "localhost"
* user: "root"
* password: "" (it's blank)

The class exercises left the password setting in `db.inc.php` blank,
so if you're running on macOS, you have to edit that file before
things will work.

### Making strings "safe"

In the exercises, we used 2 separate functions to make data safe:

1. For taking input from users and making it safe to store in the
   database, we used `mysqli_real_escape_string`.

   `$company = mysqli_real_escape_string($link, $_GET['company']);`

   This converts the
   various parts from the form input into a string that can be safely
   inserted and extracted from the
   database. See
   <http://php.net/manual/en/mysqli.real-escape-string.php> for more
   information about what this is doing (and why).

2. For taking information from the database (or from the user,
   depending) and displaying it on a web page, we used
   `htmlspecialchars`:

   `$companyID = htmlspecialchars($recording['companyID'], ENT_QUOTES, 'UTF-8');`

   This converts a string into safely displayable
   output, converting certain special charactres into their HTML
   entity codes. It doesn't convert all such characters, only the most
   likely to cause problems if let through.

   The documentation page
   at <http://php.net/manual/en/function.htmlspecialchars.php> shows
   which characters are changed. There's a lot of information there,
   not all of which will make sense yet.

   In class, we added the flag `ENT_QUOTES` which converts both double
   quotes and single quotes to HTML entities. The table for the `flag`
   paramter lists more.

   The last parameter we used was 'UTF-8'. This is a character set
   representation. You'll almost always want to use that, along with
   setting your web pages to display in UTF-8 using the `meta` tag in
   the HTML head.


So, to recap:

* `mysqli_real_escape_string` when getting data ready to
  add to the database.

* `htmlspecialchars` when getting data ready to display on the web
  page.

### PHP Closing tags

If there will be no HTML after you're PHP code, it's best to leave off
the PHP closing tag `?>`. If you have a closing tag on your
PHP file, and somehow add empty lines after the closing tag, PHP will
send those to the output (which is what is getting sent to the
browser). This can result in issues that end up being rather hard to
debug.

### Blank page syndrome

When you run a PHP script from your browser and get back a completely
blank page, it's frustrating and disconcerting. There are two likely
causes.

1. THere was an error during PHP execution. Check to make sure you've
   got error reporting turned on. (See above.)

2. There was a syntax error, before PHP could execute. This is harder
   because PHP never even got to the point of turning on error
   reporting.

   To figure these problems out, you have to find and follow the PHP
   error log.

### Following the PHP Error log

Although this was not covered in class, it came up for a few
students. It's just generally a good idea to do this.

On MAMP and XAMPP, in the installation directory, you'll find a
subdirectory called `log` or `logs`. Inside that subdirectory is
usually the file `php_error.log`. This is what you want to look at.

On macOS, you can open the log file in it's default application,
Console.app, and it will keep track of what's getting added to the
error log.

**HELP WANTED HERE: How does this work on Windows?**

Not sure where the error log is on Windows, or what application you'd
use to follow it. In Git-Bash on windows, you can try the following:

```bash
cd /c/xampp/logs/
tail -f php_error.log
```

(The '-f' option on `tail` says to keep following the file.)


### POST method vs GET.

**Always** use POST for sending sensitive information from the user to
the server. See <https://www.w3schools.com/tags/ref_httpmethods.asp>
for more explanation.

A classic example, if you ask a user for their password using a
special form field for passwords, but then send the form data with the
`GET` method, their password will show up in the address bar in clear
text format.

The general rule of thumb is:

- use `GET` to *request* information
- use `POST` to *send* information

### Relating tables together

In class 3, we built 2 tables in the database, `product` and
`company`, and related them together with a **foreign key**. This let
us give just the ID of the company in a row of the product table
without needing to repeat the name of the company in each row.
(The big name for this is *"database normalization"*.)

This creates a one-to-many relationship: one company can have many
products. Another way these are referred to are 'has many' and
'belongs to'.

* a company *has many* products
* a product *belongs to* a company

![Diagram of foreign key concept](http://guides.rubyonrails.org/images/belongs_to.png "Diagram of Foreign Key Usage")

*(This is from Rails, but the concept is identical. Just think of
'books' as 'products' and 'authors' as 'companies'.)*

There are lots of other kinds of relationships, but this is the most
common use.

Setting up the foreign key means adding the foreign key field to the
referencing table (the one belonging to, or the one on the 'many' side
of one-to-many).

It should be the same type as the ID field on the parent table (the
one having many, the one on the 'one' side of one-to-many).

When we created the foreign key index, we also told it to
"CASCADE". This means that if the Company row is deleted, all product
rows referring to that company will also be deleted. This is important
so there aren't any product entries that point to a non-existent
company. (The big name for this is *"referential integrity"*.)

There is *so* much to learn about relational tables, but you've got
the basics for now. You might
find <https://www.w3schools.com/sql/sql_foreignkey.asp> helpful.

## Local PHP Development Environment(s)

### macOS

* MAMP (Mac - Apache - MySQL - PHP): <https://www.mamp.info/en/downloads/>

  Default MySQL credentials:
  * user: "root"
  * password: "root"

* XAMPP (x - Apache - MySQL - PHP - Python): <https://www.apachefriends.org/index.html>

  Default MySQL credentials:
  - user: "root"
  - password: '' (empty, blank string)


### Windows

* XAMPP (x - Apache - MySQL - PHP - Python): <https://www.apachefriends.org/index.html>

  Default MySQL credentials:
  - user: "root"
  - password: '' (empty, blank string)

* WAMP (Windows - Apache - MySQL -
  PHP): <http://www.wampserver.com/en/#download-wrapper>
  * several people, include your instructors, had some problems
    getting WAMP installed and running, so we think XAMPP is the
    better way to go on Windows.

  * **HELP WANTED!** having never successfully installed this, I don't
    know what the default MySQL credentials are

## PHP Documentation

The main website for php, <https://www.php.net>, is one of the better
documented systems, because it contains **lots** of extra commentary
from decades of PHP developers' experience. While the language syntax
is fairly small, the libraries that come with PHP are huge. Keep the
site bookmarked and in a browser window while you're developing.

## Books

* [Head-First PHP & MySQL](http://shop.oreilly.com/product/9780596006303.do)
  a very accessible book for learning PHP and MySQL from O'Reilly's
  Head First imprint.

## Web Sites

* [CodeAcademy PHP Track](http://www.codecademy.com/tracks/php)
* [w3schools PHP Tutorial](https://www.w3schools.com/php/default.asp)
* [w3schools SQL Tutorial](https://www.w3schools.com/sql/default.asp)
* [Learn PHP the Hard Way](https://phpthehardway.wordpress.com/)


## MORE HELP WANTED!!

Please submit [issues, questions, comments, etc.](https://github.com/gdiminneapolis/LinksInfoNotes/issues) !!

For extra credit, submit [changes, pull request](https://github.com/gdiminneapolis/LinksInfoNotes/pulls).

Talk in the [#php-classes Slack channel](https://gdimpls.slack.com/messages/C67F0RL8N).
