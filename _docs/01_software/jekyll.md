---
title: Install Jekyll
stub: jekyll
section: software
section_order: 4
---

{:.py-4 .mt-4 #jekyll}
***

## 4. Install Jekyll

Finally, we get to [Jekyll](https://jekyllrb.com/){:target="_blank" rel="noopener"}!
Jekyll is a static site generator that uses templates and data to build out websites. 
It is a very popular tool used by tiny and giant web site projects. 

Jekyll is a Gem, a software package installed via Ruby's management system called RubyGems (similar to Python's Pip). 
Gem is a command line application, so again we will open a terminal to give it commands.
Once you have a terminal open, type in the command:

`gem install jekyll bundler`

{% include bootstrap/alert.md text="This will take awhile as the Gem installs all the dependencies and builds extensions (on Windows it may appear as if nothing is happening, be patient!)." color="warning" %}

{% include bootstrap/alert.md color="danger" text="**Debugging Note:** if you have **Ruby version 3.0+** and **Jekyll version 4.2.0** (or less), when using Jekyll you will encounter an error in your terminal including 'cannot load such file -- webrick (LoadError)'.
Please try installing webrick globally using `gem install webrick` *or* adding it to your project Gemfile using `bundle add webrick` in the project directory.
This issue will be resolved in future Jekyll versions." %}

Your dev environment is ready! Give yourself a hand!
