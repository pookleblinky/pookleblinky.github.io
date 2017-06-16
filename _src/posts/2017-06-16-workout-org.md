    Title: workout.org
    Date: 2017-06-16T06:35:00
    Tags: org-mode, fitness

I believe that org-mode will drive you mad if you try to use more than
the bare minimum of features necessary for what you need to do.

Here's how I'm using it to track workouts.

I have a workout.org file, which is in ```org-agenda-list```

Workout.org has a local status header:

    #+TODO TODO STARTED | DONE

The STARTED status is just handy to have, even if I don't use it much.

workout.org contains the following structure:

    Datetree
    Schedule
    Regimen
    Stats

I have the template 

    ("w" "Log Workout" entry (file+datetree+prompt
         "~/org/workout.org") "* %? %U" :empty-lines 1)

in my org.el which lets me create a new entry in the datetree. This
entry is only to log details of the workout: weights, level of
perceived effort, etc. The workout tasks are outside the datetree, in
the schedule node. The schedule node contains subheaders of repeating
scheduled todos:

    ** TODO Daily: 300 KB swings
    DEADLINE: <2017-06-15 Thu +1d>
    ** TODO Monday: Squat/row
    DEADLINE: <2017-06-19 Mon +1w>

etc. I can clock in, mark done to clock out, and then log the details
in the datetree. Keeping the todo separate from the details seems like
a good idea, as I don't have to go hunting around: every workout todo
is in a single spot. Each workout task has a link to a description in
the regimen node: giant set blah, use these accessory movements blah,
etc.

Note that these tasks are deadlines, not scheduled. org-mode considers
a scheduled task to be when the task is to be started. A deadline task
will appear as DEADLINE on the designated day, and org-agenda will
show the number of days til a deadline.

The regimen node just contains such as giant set templates, notes on
progressive increments, etc. Eventually I may use org-babel to add a
such as a 531 calculator and template generator.

Stats contains my bodyweight, BF%, not in a datetree but just time
stamped.

This is the simplest setup that does what I want. I could get fancier:
adding tags, tweaking a report function that'll show a plot of weights
used for a specific lift over time, setting org-habit properties,
writing a function to slurp the data right out of my phone's FitNotes
.csv into the appropriate places, etc.

None of that's really necessary. FitNotes tracks and graphs specific
movements and muscle groups and weights much more nicely than I would
do myself. Org-habit, while useful for some things, doesn't really
make sense in this context. And directly integrating FitNotes data
seems redundant. What workout.org does allow that fitnotes doesn't, is
the ability to track and schedule things in plaintext, portably.

The one justifiable increase in complexity is the abovementioned
desire to incorporate a workout calculator and generator directly into
the file via org-babel. For instance, being able to generate a
datetree pre-filled with 531 workouts for a specified number of
mesocycles. However, I'm not doing 531 although I am inspired by
it. If I do switch over, I'll probably get around to it.

That's workout.org. It uses barely any of org-mode's features, does
what I need it to do, and can be endlessly refined into one of those
org setups where the user seems to be attempting to use every feature
of org-mode to weave an elaborate robot web around their lives. 

The prime rule in emacs is to start from scratch. The absolute worst
thing you can do is plop someone else's stuff into your setup and
expect it to work for you. In org-mode especially, this is
vital. Every one of those absurdly-polished gems of org mode
configurations you see, where the blogger seems to have automated
themselves away, is the result of years of tweaks and personal
itch-scratches built up over time in the way that only lisp
allows. Few will want to show you how they did things the lazy way,
only the final result guaranteed to utterly annoy anyone who plops it
into their config and tries to use it. In org mode especially, that
lazy way that doesn't show off any of the really nifty features is
probably good enough for 80% of the time, and can easily be used as
a guide by a newbie. If they're foolish enough to steal it for
themselves, at least it'll be simple enough they will be able to
understand it and find out how to tweak it. Either way, it's much more
useful than showing the fully chromed-out inscrutable code that the
config inevitably becomes as emacs is tweaked into conforming to them.


