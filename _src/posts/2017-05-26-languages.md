    Title: languages
    Date: 2017-05-26T03:04:55
    Tags: languages, dev environment, workflow, learning

I tend to get flustered when learning languages. I bounce from one to another,
trying the same thing in each. "oh cool how would I do this in foo? Ah, gotta
yakshave my emacs for bar" 

Little ends up getting done, and I end up working at a cartoonishly slow pace as
I bounce around playing with everything. 

Right now, I'm focusing on Racket, Elixir, Clojure, and Common Lisp. oCaml, LFE,
and Haskell as background noise, not the main focus.

That's a lot of opportunity to get distracted on several levels, from other
languages to yakshaving dev environments and workflows for them. 

For instance, my normal workflow involves vim-slime and tmux. Vim-slime sends
text to a specified tmux pane, it doesn't know or care what repl is on the other
end. It doesn't know or care about nrepl or swank or any of that. Just where to
dump the text. I prefer this over magic. Well, in LFE slurping a file into the
repl dumps all previously slurped macros and defs. The repl is more stateful
than most, so the workflow is a little awkward. I was pondering how to tweak
vim-slime to have an LFE mode that would on C-c C-c first save, then send over
the text (c "@%"), or something. I could yakshave on this happily, but it's a
distraction.

My attempted solution is simple. For focus, I'm using exercism. Each language is
on a different track, each has defined tasks to accomplish and progress is
tracked. Most tracks have similar tasks, which nicely satisfies my "oh man I
wonder how I'd do this in foo" impulse, but in a structured and focused way.
Yakshaving is kept to a minimum: while working in racket, I can pop over to
another pane, type "langjournal," and note a todo about yakshaving vim to work
better with it. Later, I can yakshave, but I can keep focused on what I was
doing instead of falling down the rabbit hole. 

While doing the erlang track, I saw that rebar.config hardcoded rebar3. I did
the task, gsubbed rebar3 to rebar (v2 is what I had), and ran the tests. They
passed, I made a note. Went on #erlang, asked about rebar3, and decided to
upgrade. I bootstrapped it in less than a minute, reverted rebar.config, and it
worked as intended. Minimal yakshaving.

I figure as long as I keep things structured, push yakshaving out of the way
into its own activity ("today I'm gonna get vim to work better with lfe"), and
avoid temptation, I'll have a much nicer time than my usual habits provide.

This blog is going to be part of my workflow, forcing me to maintain a coherency
which is usually lost reinventing a local PLEAC.
