---
layout: post
title: "the struggles of setting up"
date: 2022-06-23 18:50:00 +0500
categories: misc
---
By no means do I mean to be my "first" blog post, so I guess this could be considered post number zero c:

> “In a time of deceit telling the truth is a revolutionary act.” - Orwell, *1984*

Jekyll is fairly easy to setup, but for someone using it for the first time (like me ^-^) it might be pretty hard to get through. From about 11 in the morning to 7 in the evening I was working on getting the blog setup. The first time it worked great, but I went smooth brain and then forgot to save everything. This would be when my problems started

I was origanally following the [documentation](https://jekyllrb.com/docs/) but then realized I was wasting my time doing all the extra bits that I didn't need for my corner of the internet, so I decided to take a break for lunch and start again following Geoffrey Mungai's [guide](https://www.section.io/engineering-education/build-a-jekyll-site/). Going through all the initialization steps and launching the site went okay the first time around, but then I decided to restart my laptop (without saving, ofcourse :eyesrolled:). This voided all my progress that I was making on my ACTUAL first post and sparked a bunch of problems.

The first issue I faced was the 'jekyll' command returning this error:
{% highlight bash %}
➜  ~ jekyll         
/usr/lib/ruby/3.0.0/rubygems.rb:265:in 'find_spec_for_exe': can't find gem jekyll (>= 0.a) with executable jekyll (Gem::GemNotFoundException)
        from /usr/lib/ruby/3.0.0/rubygems.rb:284:in 'activate_bin_path'
        from /home/vik/.local/share/gem/ruby/3.0.0/bin/jekyll:25:in '<main>'
{% endhighlight %}

Solving this took quite a bit of time searching on google and finding solutions that fixed my exact problem. I tried many iterations of the `gem install` and the `gem update` commands that come alongside ruby, 
but the solution I found for this was reinstalling Ruby/Gem/Jekyll completely. There might be a quicker fix for this but at that point none of the solutions on the Almighty Google were fixing my problems. 

After fixing that, the gem bundler decided to mess itself up:
```bash
➜  ~ bundle install                                                        
/usr/lib/ruby/3.0.0/rubygems.rb:265:in `find_spec_for_exe': can't find gem bundler (>= 0.a) with executable bundle (Gem::GemNotFoundException)
        from /usr/lib/ruby/3.0.0/rubygems.rb:284:in `activate_bin_path'
        from /home/vik/.local/share/gem/ruby/3.0.0/bin/bundle:25:in `<main>'
➜  ~ jekyll         
/usr/lib/ruby/3.0.0/rubygems.rb:265:in `find_spec_for_exe': can't find gem jekyll (>= 0.a) with executable jekyll (Gem::GemNotFoundException)
        from /usr/lib/ruby/3.0.0/rubygems.rb:284:in `activate_bin_path'
        from /home/vik/.local/share/gem/ruby/3.0.0/bin/jekyll:25:in `<main>'
```

This ended up being an issue with my PATH and ~/.zshrc being messed up, so this probably meant I made a mistake along the way. Other issues I had were easily sovable by the first result on StackOverflow or Google.

Aftter fixing all of this, I set out and started writing this post, and as I end up today's article, I hope this helped or educated you in some way or the other! Thanks for reading

<3,
Vik
