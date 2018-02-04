    Title: Lifescripts: Stochastic routines
    Date: 2018-02-04T04:36:58
    Tags: flipism, racket, coding, fitness
Since November I've been doing a form of intermittent fasting I
created based on coinflips, that I call coinfasting.

Every morning flip a coin. Heads, you eat, tails you fast.

The expected value of heads over 7 days is 3.5, so it's identical in
effect to a scheduled alternate day fast.

The introduction of randomness makes things interesting: you can't
just binge on heads days, because you may get a bunch in a row. And
you can't restrict too much on fast days, because you may get a bunch
of fast days in a row. This makes it easier to dial in on the right
amount of calories, and lets the meals be a bit less absurd than on a
normal ADF.

After doing this a while, I love it. It feels fun and sustainable, and
is easily modifiable. When I hit maintenance, I can such as switch
heads to TDEE+15%, tails to TDEE-15% easily. The only actual daily
habit that needs to be engrained is one cointoss.

I decided to embrace more flipism.

Each morning I do 20 minutes of cycling. On heads days I add another
30 minute afternoon cycling session. This gives a baseline of 140
minutes, which is the minimum recommended dose of cardio, and averages
over time to another 105 minutes for a total of 245 minutes a
week. Maximum: 350 minutes a week. This is a good amount of cardio, as
the maximum effective dose of cardio is about 450 minutes a week
(https://well.blogs.nytimes.com/2015/04/15/the-right-dose-of-exercise-for-a-longer-life/).

So that's both calories and LISS out of the way, with one coinflip.

I then based my kettlebell on dice. After flipping the coin, roll 2d6
and multiply by a number to get the number of swings that day. I chose
a multiplier of 10. On average, 70 swings a day, maximum 120. This is
because any more swings right now would bite into my deficit too
much. Later, I can toggle the amount based on the coinflip: heads 25,
tails 10. This'd bring me to a maximum of 300 swings a day, and an
average of 210.

So that's what I'd been doing for a while. Some days I'd physically
flip a coin and roll dice, other days I'd just ask my phone to do so.

I decided to automate this.

I created a git repo called Lifescripts, and began making small racket
programs to at first simply do what I'm already doing.

Now I can simultaneously flip and roll for the day with one command.

The git repo is here: https://github.com/pookleblinky/lifescripts

I then added a script to decide whether to engage in argument, a
script to decide whether to cuss. One to decide the music of the day,
one to decide which topic to boost for the day. A script to decide
whether to refactor or write new code. One to assign a random small
task like doing kettlebell swings or clean something.
