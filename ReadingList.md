# Reading List

**NOTE: This is just a start! We need more suggestions! Please
Contribute!**

The list below is directly lifted
from
[Tamara](https://github.com/tamouse)'s
[Software as a Craft blog](https://swaac.tamouse.org)'s
[learning page](https://tamouse.github.io/swaac/pages/learning/). She's the
"I" below.

It has since been updated with various links shared on the Slack channel as of 7/16/2018. These descriptions where written by Kim Thompson.

Please follow [**our Instagram! <3**](https://www.instagram.com/gdimpls/)

## General Programming

* [**Think Like a Programmer: An Introduction to Creative Problem Solving**](https://www.goodreads.com/book/show/13590009-think-like-a-programmer)
  by V. Anton Spraul

  Spraul's purpose in this book is not to teach you how to write a
  program, but to begin to understand the problem-solving approach
  that is inherent in good programmers. Like so many skills,
  programming is driven by the desire and vision of the
  practitioner. A painter uses brushes, canvas, paints, other media to
  create a work of art, but it isn't the tools, it isn't the specific
  techniques, and it isn't even the particular skill the painter has
  that makes a good work of art; it is their composition, the melding
  of media and surface, the use of different techniques, and practice
  in developing the skills that come together to form the work of
  art. Spraul is going to take you deeper than just the syntax,
  semantics, and data structures of software to the heart of what
  makes a good programmer: the ability to creatively find and generate
  solutions to problems.

* [**Learn to Program**](https://www.goodreads.com/book/show/520.Learn_to_Program)
  by Chris Pine

  This book is nearly universally recommended to people new to programming. The
  original tutorial is available online for free as well:
  [https://pine.fm/LearnToProgram/](https://pine.fm/LearnToProgram/). _Learn
  to Program_
  was featured on the great webcomic
  [Unshelved](http://www.unshelved.com/2014-7-25).

* [**A Pattern Language: Towns, Buildings, Construction**](https://www.goodreads.com/book/show/79766.A_Pattern_Language)
  by Christopher Alexander

  You may be wondering why I've included a book on building
  construction. The answer is quite simple: the concepts in building
  towns and houses is nearly directly translatable to building
  software applications and systems. One part of being an excellent
  craftsperson is being able to apply abstract learning in different
  problem domains. If you are an expert in writing software, you are
  almost *never* going to be solving problems only for other software
  developers. (You can and should do so, but the client and users are
  generally non-programmers.) Thus you're most likely going to be
  working in someone else's domain of expertise. Alexander's views on
  architecture apply to software architecture as well.

* [**Beautiful Code**](http://shop.oreilly.com/product/9780596510046.do)
  by Andy Oram and Greg Wilson

  A book with a purpose, that isn't a how to code, so much as a how to
  think about coding. Source of the missive:

  1. Make it correct
  2. Make it pretty
  3. Make it fast

  In that order.

* [**System Design Heuristics**](https://leanpub.com/systemdesignheuristics)

  A pay what you want (within reason) book that is being revised on an ongoing basis. It covers a number of design principles.

## Object-Oriented Programming

* [**99 Bottles of OOP**](https://www.sandimetz.com/99bottles) by
  Sandi Metz and Katrina Owen.

  A recent book, representing the absolute best by two teachers of
  software engineering. Sandi has been teaching Object-oriented
  programming for decades, and Katrina brings in her expertise with
  refactoring, resulting in a deep book that stretches beyond the
  basics and deep into the structures and understanding of object
  systems and idioms. It brings up to date the actual concepts of
  refactoring, test-driven development, naming things, reducing code
  "smells" and making code more easily and economically maintainable
  and sustainable. They take all the buzzwords and unbuzzify them into
  practical, useful methodologies and techniques.

## JavaScript

* [**JavaScript: The Good Parts**](https://www.goodreads.com/book/show/2998152-javascript)
  by David Crockford.

  JavaScript is a vast, sprawling language and ecosystem, and has been
  maligned for much poor code on the web. Crockford extracts out the
  parts that are really useful, giving the reader a better
  grounding. This book is the progenitor of many of the JavaScript
  frameworks that have come up the past few years, including
  CoffeeScript, TypeScript and other *Script derivatives.

* [**You Don't Know JS series**](https://github.com/getify/You-Dont-Know-JS)
  by [Kyle Simpson](https://github.com/getify).

  A *tour de force* by one of the great teachers and evangelists of
  JavaScript, Kyle's "You Don't Know JS" series is a must-read
  collection of books. You can get the books in raw form on-line at
  the above address, and you can get the published e-books at your
  favourite vendor.

* [**Eloquent Javascript**](http://eloquentjavascript.net/)
  by Marijn Haverbeke.

  When I was more naive about JS, I wrote a bit of a negative review
  of this book. Subsequently, I've learned of it's true eloquence and
  meaning in giving a model of how to organize and implement modern
  JS. The subtitle "A modern introduction to programming" is still a
  bit misleading, perhaps, because you have to understand a fair bit
  of JavaScript *and* programming to get the message, I feel. But
  that's just a quibble at this point. Read this before you strike out
  on creating a client-based JS application; you won't regret it.

* [**Get Started with Debugging JavaScript in Chrome DevTools**](https://developers.google.com/web/tools/chrome-devtools/javascript/)
  by Kayce Basques

  This basic tutorial for debugging any JavaScript issue in DevTools is available as both an article and a video.

* [**JavaScript ES6+: var, let, or const?**](https://medium.com/javascript-scene/javascript-es6-var-let-or-const-ba58b8dcde75)
  by Eric Elliot

  A rundown of ES6's alternatives to `var`, `const` and `let`. `var` is now the weakest signal available. `const` denotes that the value will never be changed. `let`s may be reassigned, but can only be used in the block they were defined in.

* [**Increment/Decrement**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Arithmetic_Operators#Increment)

  Added clarification around how `++` and `--` work in JavaScript. Basically, if it is put after the variable (e.g. `x++`), the value will be returned before incrementing. If it is put after the variable (e.g. `++x`), the value will be returned after incrementing.

* [**Template Literals**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals)

  True bliss. No more do we need to do this:

  ```JavaScript
    console.log('Fifteen is ' + (a + b) + ' and\not ' + (2 * a + b) + '.');
  ```

  This (which uses backticks instead of quotes) is much more readable:

  ```JavaScript
    console.log(`Fifteen is ${a + b} and not ${2 * a + b}.`);
  ```

* [**JavaScript Style Guides and Beautifiers**](https://addyosmani.com/blog/javascript-style-guides-and-beautifiers/)
  by Addy Osmani

  Note from @tamouse:
  
  > The article was written in 2012 though, and if you've heard anything
  > about the JavaScript world, it's that the amount and frequency of change is
  > *huge*. The tools most often used now are `eslint` and `prettier`.
  > Teams use these a lot when working on code to achieve a common style (and
  > to find syntax errors before shipping code!) so no one has to argue about
  > the right style anymore.

  Idiomatic's still big, but Google and AirBnB have overtaken it in time ([read more](https://codeburst.io/5-javascript-style-guides-including-airbnb-github-google-88cbc6b2b7aa)).

### React

* [**React Developer Roadmap**](https://github.com/adam-golab/react-developer-roadmap)

  A chart that demonstrates the paths you can take and the libraries you might want to learn in order to become a React developer. It should help give you a rough idea of the landscape as it is currently, since it is frequently being updated.

## HTML and CSS

* [The New CSS Layout](https://abookapart.com/products/the-new-css-layout)
  by [Rachel Andrew](https://twitter.com/rachelandrew/)

  This new book by CSS3 Grid contributor Rachel Andrew is the current
  best explanation and introduction to the new layout systems in CSS3,
  Grid and Flexbox. A *must* read!

* [**HTML and CSS Design and Build Websites**](https://www.amazon.com/HTML-CSS-Design-Build-Websites/dp/1118008189?ie=UTF8&*Version*=1&*entries*=0)
  by Jon Duckett

  This book has been recommended by several people in the [GDI] courses
  I've been helping in. A very visual approach, using full-colour photographs
  to explain the two declarative languages.

### Sass

* [**Sass Color Variables That Don't Suck](https://davidwalsh.name/sass-color-variables-dont-suck)
  by Landon Schropp

  Have you ever tried naming colors based on where they were used and found that you ended up using "hamburger-background" in unrelated places? Have you ever simply named the variables after their colors and ended up with this mess:

  ```Sass
  $yellow-green: #b0eb00;
  $red: #b30015;
  $blue: #2a00b3;
  $other-blue: #0077b3;
  $cyan: #00b0b3;
  $transparent-cyan: #24fbff;
  $periwinkle: #8a7dff;
  $light-gray: #a6a6a6;
  $gray: #595959;
  $darkish-gray: #444;
  $dark-gray: #363636;
  $darker-gray: #303030;
  $darkest-gray: #292929;
  $darkester-gray: #111;
  ```

  This is the article for you.

## PHP

* [**Head-First PHP and MySQL**](http://shop.oreilly.com/product/9780596006303.do)

  Published by O'Reilly, their "Head-First" imprint is intended for
  people just starting out learning to program. *Head-First PHP and
  MySQL* is an entertaining and informative dive into one of the most
  popular server-side programming languages. After learning HTML, CSS,
  and some JavaScript, PHP is a great place to jump into writing
  dynamic web sites that interact with your own data. WordPress,
  running on 28% of the web (and still growing) is written in PHP.

### WordPress

* [**Intro to WordPress**](https://allyson-wehrs.github.io/GDI-WP-101/#/beginning-slide)
  by Allyson Wehrs

  Slides from one of our courses on Wordpress, explaining what it is, how it is used and how you can get started.

## Ruby

* [**Eloquent Ruby**](https://www.goodreads.com/book/show/9364729-eloquent-ruby)
  by Russ Olsen.

  Olsen's approach in this book is to go far beyond just learning a
  programming language, but a way to learning the idioms and the "Ruby
  Way". Even if your chosen language is something other than Ruby,
  reading this book will give you an appreciation for how to delve
  into a language and get the most out of it.

* [**Confident Ruby**](http://www.confidentruby.com/)
  by Avdi Grimm

  More than any other book I've read on Ruby, "Confident Ruby" has
  affected my coding habits more than any other. If Ruby is about
  making programmers happy, *Confident Ruby* is about making
  programming joyful, and not just in the immediate, but being able to
  look at code you've written in the future and recall the
  joy. *Confident Ruby* seeks to combat software rot from the get-go.

* [**Well-Grounded Rubyist**](http://www.amazon.com/The-Well-Grounded-Rubyist-David-Black/dp/1617291692)
  by David A. Black

  Also known as the "Black Book" (because of the author's name), WGR
  is the successor to _Ruby for Rails_ by Black that provided me with
  the much-needed introduction to how to write Ruby code, with the
  idea of using it in Ruby for Rails. This book is a fabulous primer
  on the Ruby idioms and expressions that help make one a good Ruby
  programmer.

* [**Practical Object-Oriented Design in Ruby**](http://www.poodr.com/)
  by Sandi Metz

  This book provides a deeply-needed introduction to object-oriented
  design, specifically targeted to the Ruby language. Ruby is one of
  the richest languages in which to express object-oriented patterns,
  but it is easy to fall of the OO wagon and start to get things
  messed up. Sandi provides the thinking tools necessary to decide how
  to structure your code for better maintainability, extensibility and
  testability. Comprehension and forward communication of the choices
  made during software design are crucial to programming, and Sandi is
  one of the very best at explaining things.

### Rails

* [**Rails 4 in Action**](http://www.manning.com/bigg2/) by Ryan Bigg,
  Yehuda Katz, Steve Klabnik, and Rebecca Skinner.

  A follow-on the highly successful Rails 3 in Action, R4iA has been
  completely rewritten, with new examples, case study, and all the
  great new features in Rails 4.

  A great book for beginning Rails developers to start with, and for
  intermediate developers to step up their game.

* [**Practicing Rails**](https://www.justinweiss.com/practicing-rails/)
   by [Justin Weiss](http://www.justinweiss.com).

  The first chapter alone (free!) is worth a download and very
  thorough read. Justin has provided one of the most effective
  strategies for learning just about *anything* skill based, and it's
  especially effective for learning software skills. The focus of the
  book and the examples and such are obviously Rails, but the first
  chapter is applicable to learning anything.

* [**RailsConf 2018: Actionable Tactics for Leveling Up Junior Devs by Sumeet Jain**](https://www.youtube.com/watch?v=K0vxOBIyhF0)
  by Sumeet Jain

  Ain't nobody got time to watch a half hour video, so I'll list the description:

  > We are told that junior developers are a secret weapon, but this alleged
  > "competitive advantage" is so elusive! Typical advice about evolving talent
  > can be broad, u-relatable, and impractical. Aren't there any specific and
  > actionable tactics that teams can employ for leveling up new devs? (Yes,
  > there are!)

## Git

* [**Resources to learn Git**](https://try.github.io/)

  A good intro, with options to to learn by reading or doing (or both!)

## Web Architecture

* [**Web Architecture 101**](https://engineering.videoblocks.com/web-architecture-101-a3224e126947)
  by Jonathan Fulton

  An article that walks you through how modern web apps tend to be hooked up. It explains what the following things do and how they work together:

  * Domain Name Servers (DNS)
  * Load Balancers
  * Web Application Servers
  * Database Servers
  * Caching Services
  * Job Queues & Servers
  * Services
  * Cloud Storage
  * Content Delivery Networks (CDN)

## Accessibility

* [**Designing for accessibility is not that hard**](https://uxdesign.cc/designing-for-accessibility-is-not-that-hard-c04cc4779d94)
  by Pablo Stanley

  This article describes seven easy-to-implement things you can do that will improve the accessibility of your site. It also talks a bit about the business case for accessibility, and how sites that are designed this way from the ground up tend to see more traffic, be faster and have neater code.

## Education

* [**Welcome to the T in STEM**](http://technologistalk.libsyn.com/welcome-to-the-t-in-stem)
  by Technologist Talk podcast with Charles Eaton

  A podcast episode that discusses a number of paths into a tech career and how parents can help.

* [**Abby Wambach's graduation speech is my new rally cry**](http://www.chicagotribune.com/lifestyles/stevens/ct-life-stevens-wednesday-abby-wambach-barnard-graduation-0523-story.html)
  by Heidi Stevens

  The full transcript of Abby's speech can be found [**here**](https://barnard.edu/commencement/archives/2018/abby-wambach-remarks).

* [**University of Minnesota Coding Boot Camp**](https://bootcamp.umn.edu/coding/)

  "Become a Web Development in 12 or 24 Weeks". This program would cover:

  * HTML5
  * CSS3
  * JavaScript
  * jQuery
  * Bootstrap
  * Express.js
  * React.js
  * Node.js
  * Database Theory
  * Bookshelf.js
  * MongoDB, MySQL
  * Command Line
  * Java
  * Git
  * and more

## Career Advice

* [**Becoming a 10x Developer]**(https://kateheddleston.com/blog/becoming-a-10x-developer)
  by Kate Heddleston

  Ten ways to be a better teammate: the kind of teammate that makes everyone around them 10x better, instead of just being 10x better than everyone else.

* [**88 ways to become better end to end software developer**](https://hackernoon.com/88-ways-to-become-better-end-to-end-software-developer-6e0ae2fdb652)
  by Leo Kyrpychenko

  Note from @tamouse:

  > i thought i'd bring this to folks' attention, not because I'm endorsing
  > this post, but because it lists a bunch of things that can help expand
  > one's desirability for hiring options. As most folk here are still at the
  > early stages of their career, this list is more of a "someday-maybe" sort.
  > If you aren't doing any of these, it's OKAY -- don't fret!
  >
  > Plus, piano players don't play all the keys either :)

* [**My Lessons from Interviewing 400+ Engineers Over Three Startups**](http://firstround.com/review/my-lessons-from-interviewing-400-engineers-over-three-startups/)

  What Marco Rogers actually looks for when hiring engineers at startups. Key takeaways: soft skills matter, startups don't often know what they're looking for in a candidate yet, interview in three person groups, bring future colleagues into the interview process.

* [**Add This To Your Resume After Deleting Your "Objective" Statement**](https://www.fastcompany.com/40531306/add-this-to-your-resume-after-deleting-your-objective-statement)
  by Martin Yate

  We know your objective is to get this job. Not only that, but frames the conversation on what you want from the company rather than what the company in question should want with you. Why not write a Performance Summary or Career Summary instead?

## Sexism in the Industry

* [**The Perverse Incentives That Help Incels Thrive in Tech**](https://www.wired.com/story/ellen-pao-the-perverse-incentives-that-help-incels-thrive-in-tech)
  by Ellen Pao

  The title says it all. Don't read if you're in a good mood. Or if you're in too bad of a mood, for that matter.

* [**Google diversity report: Black women make up only 1.2 percent of its U.S. workforce**](https://www.washingtonpost.com/news/the-switch/wp/2018/06/15/google-diversity-report-black-women-make-up-only-1-2-percent-of-its-u-s-workforce/?noredirect=on&utm_term=.ac9d4aa34af2&wpisrc=nl_most&wpmm=1)
  by Hamza Shaban

  A breakdown of Google's continued failure to hire a proportional number of women and minorities, particularly those who fall into both categories.

* [**Science Finds Men Understand Body Language, Ignore It**](http://www.notsorryfeminism.com/2018/01/science-finds-men-understand-body-language.html)
  by Lindsey Weedston

  She discusses Aziz, Louie, and why men are still getting away with the "I didn't realize she didn't want it" excuse long after it's been debunked (see also [**Mythcommunication: It's Not That They Don't Understand, They Just Don't Like the Answer**](https://yesmeansyesblog.wordpress.com/2011/03/21/mythcommunication-its-not-that-they-dont-understand-they-just-dont-like-the-answer/) from 2011 and [**Just Say No? The Use of Conversation Analysis in Developing a Feminist Perspective on Sexual Refusal**](http://journals.sagepub.com/doi/abs/10.1177/0957926599010003002) from 1999).

* [**Women are given a tougher time in interviews than men, scientists find**](https://www.telegraph.co.uk/news/2017/07/03/women-given-tougher-time-interviews-men-scientists-find/)
  by Harry Yorke

  "Women are given a tougher time during interviews and are interrupted more often than men . . . Men are also twice as likely to interject while speaking to a woman. And when they do cut-in during a man-on-man discussion, it is 'generally more positive and affirming'."

* [**Leading By Example To Close The Gender Pay Gap**](https://www.cbsnews.com/news/salesforce-ceo-marc-benioff-leading-by-example-to-close-the-gender-pay-gap/)
  by Lesley Stahl

  Note from @tamouse:

  > In case you missed 60 Minutes on Sunday night, an interesting look at
  > Salesforce and the gender wage gap. This goes beyond the pay gap and also
  > touches on the importance of gender diversity within leadership. I'm curious
  > to know something that isn't covered&mdash;the gaps within other diverse
  > areas, including race and LGBTQ, both with wage and leadership.

## Mentoring and Volunteering

* [**1 Million Women to Tech: Benefits of Becoming a Mentor**](https://memberportal.1millionwomentotech.com/mentor-optin)

  Related to the Summer of Code event. Instead of taking these courses over the summer, you could help others learn.

## Security and Surveillance

* [**How a Hacker Proved Cops Used a Secret Government Phone Tracker to Find Him**](https://www.politico.com/magazine/story/2018/06/03/cyrus-farivar-book-excerpt-stingray-218588)
  by Cyrus Farivar

  The story of how a hacker was caught by the police, and how he turned it around and figured out how they caught him. Now, thanks to his unlikely discovery, cops' use of Stingrays might finally require a warrant.

* [**Woman says her Amazon device recorded private conversation, sent it out to random contact**](https://www.kiro7.com/www.kiro7.com/news/local/woman-says-her-amazon-device-recorded-private-conversation-sent-it-out-to-random-contact/755507974)
  by Gary Horcher

  One of her husband's employees was sent all sorts of private conversations and was kind enough to call them and let them know what was going on. Amazon sent an investigator, but hasn't really opened up about why the program misinterpreted what was said in this way and how they're going to prevent this kind of thing in the future.