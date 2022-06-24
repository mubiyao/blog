---
layout: post
title: "learning ruby so far"
date: 2022-06-24 16:03:00 +0500
categories: programming/tech
---
> “Perfection is achieved not when there is nothing more to add, but rather when there is nothing more to take away.” – Antoine de Saint-Exupery

A few weeks before setting up this blog, I decided to start learning the Ruby programming language. I've always been infatuated with scripting languages and how versatile and useful they are, and wanted something more object-oriented than Python. I started off using the **"IRb"** or the *I*nteractive *R*u*b*y Session and playing around with a Linux-Shell like environment, which I was more familiar with.

After using the Ineractive Enviroment for a bit, I decided to start writing by first program.

```ruby
#!/usr/bin/ruby 

puts "Hello, World"; 
```

A simple Hello World didn't show much, but after coding trial programs for awhile, I could see a slight similarity to the syntax of C++ and Perl. It took some time getting used to working with another OO Language 2-3 years after learning Java, but it was easy since EVERYTHING is an object in Ruby. Coming from Python, I found accessor & setter Methods to be easy to replicate some of the programs I coded in Python before.

```ruby
#!/usr/bin/ruby 

# outputs a random width and height of a box

class Box
   def initialize(w,h)
      @width, @height = w, h
   end

   def getWidth
      @width
   end
   def getHeight
      @height
   end

   def setWidth=(value)
      @width = value
   end
   def setHeight=(value)
      @height = value
   end
end

box = Box.new(10, 20)

box.setWidth = rand(1..110)
box.setHeight = rand(1..95)

x = box.getWidth()
y = box.getHeight()

puts "Width of the box is : #{x}"
puts "Height of the box is : #{y}"
```

I don't really know how to end off this post, but I'll continue to update this blog with my progress of learning Ruby and some code snippets along the way.

Best,
Vik