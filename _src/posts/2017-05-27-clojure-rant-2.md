    Title: clojure rant, 2
    Date: 2017-05-27T04:23:28
    Tags: rant, clojure

Clojure is an ugly, sloppy hack on top of Java that should shame anyone who has
ever written a lisp interpreter in any language. The core code is sloppy and
unprofessional, the leaky abstraction of the stacktrace would get you failed in
any compiler course. I mean it. There are weekend hacks of scheme compilers
inside Java that do not expose the implementation so blatantly. It's one thing
to do so to push out something as fast as possible, but to almost a decade later
still not see that sloppiness as a problem is inexcusable. [Here's Peter
Norvig's implementation of Scheme in Java](http://norvig.com/jscheme.html).
Notice how he took pride in his work.

Clojure is lisp for people who literally do not know what a lisp is supposed to
be like. It's as much a failure as Arc, except that arc would have passed a
freshman CS course. Arc *still* shows better attention to implementation detail
than Clojure. 

Clojure: what a [Java person's idea of a lisp
is](https://pookleblinky.github.io/2017/05/Clojure-annoyances-1.html). 

Clojure is an abomination, and that is probably why it'll surpass all common
lisps combined. It's the php of lisps. If you're a teen, you should probably
learn Clojure for the same reason your parents learned php. And when you get
older, you'll be able to laugh and cringe at how much needlessly sloppy, krufty
bullshit you had thought was perfectly normal. Clojure: php for people who think
they're better than php programmers.

Now consider all the amazing lispy stuff being done in Clojure by
future Elixir devs. Because it's a lisp, even a shitty one, they are able to do
incredible things which absolutely *terrify* their counterparts who arrived in
Clojure from Java. That is a testament to lisp, that even in such a bad lisp
people can do incredibly productive, cool things. All of these people will
eventually leave Clojure and find a better lisp, and leave behind warehouses of
interesting, mindbending lispy code that half of clojurians will regard with
religious terror, like powerful magical artifacts. Those on the other end of the
spectrum will leave for a more boss-friendly language and dev environment like
Go. What will be left, the eternal core of Clojure, will be people who are
content with using a bad lisp. The goldilocks programmer, stuck in the middle,
who simply puts up with the glaring warts and unfinished, sharp edges. Who
shrugs while pounding a nail using a garden gnome instead of a hammer, but
accepts that it's better than whatever they'd be doing in Go or such. 

The goldilocks Clojure programmer is one for whom Clojure is their first
functional language, first serious use of lisp outside of a hobby since college,
and who has suffered through a boss-friendly language for a bit before arriving
in Clojure. This person doesn't know what normal functional languages or lisps
or like, but does know what the lack of Java is like. Unfortunately, they've
normalized Java enough that they don't notice how much squirts out of their
code. This person will stay, outlasting the lisp weenies who arrive in a shower
of happy parentheses and leave just as suddenly. This person will stay,
outlasting their colleagues who spent more time in cubicle hell than they did,
and who retreat to a more corporate language. This person will not have any
sufficient motivation to fix either the errors the lisp weenies see, or the
errors the Java people see.

Clojure is, almost by design, guaranteed to experience evaporative cooling from
both ends of the political spectrum of coding. It's an alt-center language, it's
that weird guy who claims to be both an anarchist and a Moldbugian. It's a
gloriously failed lisp that will almost certainly expose more people to lisp
than any other dialect has. Just like php exposed an entire generation to their
first, terrible, programming language.
