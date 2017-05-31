    Title: org mode and language study
    Date: 2017-05-31T05:39:05
    Tags: orgmode, emacs, workflow
I made a shell script that plops out a random programming language
from the list of ones I'm playing with. I called it
language-of-the-day.

In the morning, I add an entry to orgfile.org that drops the output of
that script into today's node and evals it. I then know what language
to focus on that day.

I then C-c c and start adding todos for that language. Do foo, look up
bar, try out baz, study source of quux, etc. C-c a t lets me see all
these todos, and I can start working on them.

I can divide a todo into separate todo steps, set a time estimate
for each, and see how long I expect the task to take. It's possible to
then compare the estimate with the reality, and see how laughable the
former is. It's possible to then look into the subtasks and see which
ones were the most inaccurate. I can set a todo note to study whatever
was causing that step to take so long.

Today's language is Racket. I only have 3 todos: some exercism
problems, studying the Racket style guide, and writing
yasnippet/ultisnip templates specifically for Racket. The latter is
gonna take a while, as I don't feel at all like writing a snippet I
will never use. I'd rather write code, note (C-c c n) when a snippet
would come in handy, and keep working on it. Later, I can look at
those notes and see which snippets would actually come in handy. I can
also, without interrupting what I'm doing, make a note about
inefficient editing habits. "find a better way to do blah" etc.

This workflow helps keep me from bouncing around too much, playing
with trying the same thing in another language or editor or falling
down the rabbit hole of yakshaving. I'm focusing on foolang, doing bar
and quux, and can tell you exactly how long it took me to figure out
how to frobulate the wibble. Afterward I can look the notes, spin them
off into separate projects, remind myself that I really wanted to try
out x in another language, etc. 

It's not a polished, highly automated set up for 2 reasons: I don't
like magic, and that way lays endless yakshaving. This way has enough
rough edges that resisting the urge to yakshave them away is a good
form of exposure therapy. 
