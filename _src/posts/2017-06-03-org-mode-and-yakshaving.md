    Title: org mode and yakshaving
    Date: 2017-06-03T19:56:51
	Tags: orgmode, workflow, emacs

I tweaked my language-of-the day script. There is now a major language
of the day (racket, elixir, haskell) and a minor language of the day
(cl, chicken, clojure, erlang, ocaml). Each day gets a major language
and a minor language; the major gets more emphasis.

How much more can vary depending on mood, but this way not only does
something get done in each language each day, but the three I am most
interested in get more emphasis each day. 

It seems like a nice setup. I'll have to play around with it more to
see where the annoyances are. The other day, for instance, was a
haskell day but I got damned little accomplished due to trying to get
stack to work properly. 

The yakshave in question: no matter how I changed $TMPDIR and
$STACK_ROOT and such, stack kept trying to download its local ghc into
~/.stack on my internal drive then cartoonishly fail at attempting to
stuff it into my limited (I'm on crouton) tmpfs instead of using a tmp
folder on an external drive with 2TB of space. Symlinks, according to
github issues tracking, apparently work fine *after* stack setup has
done its thing, but that wasn't the problem I was having. I eventually
concluded that it'd require serious yakshaving with executability of
external drives and such, and gave up for now. In the end, I got
little actual haskell done due to spending so much time trying to get
its environment working.

Here's my global org todo keywords:

	(setq org-todo-keywords
		'((sequence "TODO(t)" "STARTED(s)"
			"DEFERRED(p)" "NEXT(n)"
			"YAKSHAVE(y)"
			"|" "DONE(d)" "CANCELLED(c)")))

I have a YAKSHAVE org status that I can apply to tasks. I can C-c c a
yakshave note ("figure out how to get stack to actually use $TMPDIR"
etc) and keep doing what I was doing. I can clock in and out of it as
I work on something, and see how much time was spent actually doing a
task versus getting things to work. At some point I'll log this ratio
of task to yakshave by language, over time, etc.

Deferred/Next refer to tasks for a specific language that I'll pick up
again the next time its language-of-the-day rolls around. 

What I'm doing is banging out a bunch of todos after
language-of-the-day. C-c a t 1 r and I can see all of them. I can
start one, C-c C-t it to started, and then make subtasks for it.

	;; Enforce dependencies
	(setq org-enforce-todo-dependencies t)

This makes a todo depend on sub-tasks. You can't switch a task to
DONE until every TODO in it is done. Yakshaves aren't subtasks, and
thus survive after the task is done as a reminder. Afterwards, I can
switch the yakshave to a TODO, clock in, and start messing with it. 

While writing this I popped out a yakshave task to see how to convert
org source blocks to scribble code blocks. Github pages renders org
and md, but I don't know if I can tell it "this is a markdown file
with org syntax you should also follow." Hm, I wonder if frog can be
made to deal with org files. In keeping with my goal of minimizing
yakshaving, I decided to just indent the above code snippets into
generic markdown blocks and play with it later. 

I then made a note to figure out how to display clock minutes as
pomodoro units just by dividing them by 25. I don't really use
pomodoro (I prefer to measure effort in cigarettes. A full gentoo
stage one install is 1 pack. Getting Frog up and running: 3
cigarettes.) But, seeing things as 25 minute chunks is just more
useful than seeing the raw amount of time spent. Doing the same thing
later and seeing the effort drop is more impressive when you can see
whole pomodoro units drop off rather than "oh it took 20 minutes less
on each of these parts."
