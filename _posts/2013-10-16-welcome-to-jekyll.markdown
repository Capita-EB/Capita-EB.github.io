---
layout: post
title:  "Testing"
date:   2013-10-16 08:21:30
category: testing
---
 One of the challenges testing a system with a large domain and a complex data model is setting up fixtures to test against.

 Once we move beyond unit tests and want to create real objects with real data – either as part of the setup stage of an automated test or for manually testing – then things become more challenging:

 -The data items we care about for the test may not all live on the object; our test might be interested in the payroll cut-off date for an employee for instance, but concerning ourselves with the details of where that data goes and the object graph needed to correctly set it all up is error prone and time consuming
 -Extra code in our tests concerned with fixture details just adds noise to the test: it makes it harder to understand and adds to the maintenance burden.
 -False-negatives: To get valid fixtures we might well have to set up other bits of data and other objects that our test just doesn’t care about, otherwise our tests fail for reasons unrelated to our test scenario
 -False-positives: Tests might unwittingly pass because we’ve left fields empty that we don’t (think we) care about for the purposes of our test e.g. our test only works properly because something is null or false etc.

You'll find this post in your `_posts` directory - edit this post and re-build (or run with the `-w` switch) to see your changes!
To add new posts, simply add a file in the `_posts` directory that follows the convention: YYYY-MM-DD-name-of-post.ext.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll's GitHub repo][jekyll-gh].

[jekyll-gh]: https://github.com/mojombo/jekyll
[jekyll]:    http://jekyllrb.com
