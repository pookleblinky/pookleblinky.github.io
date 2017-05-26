    Title: clojure annoyances, 1
    Date: 2017-05-26T09:53:03
    Tags: clojure, rant

I use Crouton on a chromebook. Clojure is a pain in the ass on low-end devices.
Just annoying as hell, easily hogs all cycles. Lein spins up its own jvm, which
adds to the startup time. On a low-end device, you're gonna spin it down in
order to such as watch a youtube video, so you really will not have long enough
lein sessions to justify such a slow startup. On a heftier box, you don't have
to juggle things like that. 

The stacktraces, holy shit. I hate Java. Every time I see 100+ lines of java
vomitspit I see clojure telling me that it is not a real lisp, that it
fundamentally will never understand concurrency, and that it does not intend to
follow the Lisp Main Sequence.

The Lisp Main Sequence: All lisps inevitably try to consume their own stack. The
normal evolution of a lisp is to ruthlessly divorce itself from its
implementation, and become pure lisp. Lisps are like facehuggers.  Every normal
lisp wants to be lisp all the way down. This isn't a technical thing, it's
social. Lisp hackers want to be able to hack lisp all the way down to the
silicon. It's engrained into the mindset. Lisp is meant to take over all that it
sees, drive its enemies before them, etc. Deep down, even the smallest lisp
wants to grow up to be a Genera lisp machine.

The mindset of clojure devs, meanwhile, is not the normal lisp mindset. After
almost a decade, they have not taken over the stack. In any normal lisp, a year
is sufficient. Clojure devs do not think like normal lispers; something is
missing in their personalities. It's downright unsettling to think that for
almost a decade clojure hackers have dealt with java regurgitating at them in
every stacktrace and *put up with it* instead of fixing it by replacing it with
more clojure. It's disturbing to think of the sheer volume of java vomitspit
they have dealt with over the years as something that is perfectly normal in a
lisp. It points to a fundamental defect, an inability to really grok lisp. It's
lisp for pointy-haired bosses. It's lisp for people who wear ties. Horrifying.

Clojure seems to be at odds with its users. Half are from java, and don't see
anything wrong with java being spat at them. Half are from lisps, and
[inevitably try to hack their own mutually incompatible
solution](http://winestockwebdesign.com/Essays/Lisp_Curse.html). The result is
that there will never be a single, united front behind which the pre-gamed
lispers can rally persuasively enough to get its benevolent dictator for life to
adopt. The result is an incredible inertia compared to most other lisps. The
userbase may grow, the number of libraries written in clojure may grow, but
fundamentally it will not embrace the main sequence of lisp evolution. 

Parodoxically, the inherent expressiveness of clojure (it is still a lisp after
all), guarantees that a fuckload of effort will go toward scratching personal
itches. New libraries and build tools will appear overnight, because in lisps
they can appear overnight. But each must beat not only the java, but the other
lisp itch-scratching. This will result in dissatisfied lispers bleeding out of
the community in search of a lispier lisp. Before they leave, however, they'll
have produced so much sheer output in attempting to scratch their itches that
the vast space of options will terrify the java faction. The java faction will
similarly bleed off, in search of a more ordered and boss-friendly language.

Who remains? Those who are comfortable with java spewing shit at them, and who
are not sufficiently lispy to attempt to hack up a solution in a weekend. Those
who for whatever reason are at the borderline between the two mutually-exclusive
poles of clojure's community. In [Yegge's political spectrum of programming
languages](https://plus.google.com/110981030061712822816/posts/KaSKeg4vQtz),
clojure is that weird dude who appeals to both anarchists and the alt-right. 

I see clojure increasing in popularity, but I don't see it changing its
fundamentally divided nature. It'll have upswings in popularity, but it'll be
continually bleeding from both ends. This hemorrhaging may not kill it, but it
guarantees inertia. The java people will bleed off into Go or something, the
lisp freaks will bleed off into Elixir or something, and the core clojure
community will remain just as eventually dissatisfying to both. 

Note: I am still interested in clojure, despite these annoyances.
