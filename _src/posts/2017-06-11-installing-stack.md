    Title: Installing Stack
    Date: 2017-06-11T06:05:30
    Tags: yakshaving, dev-environment, haskell 

I'm running Crouton, which makes some things difficult and others
outright cartoonish. Here is what was involved in getting Stack to
work.

Round 1: I installed stack from gethaskellstack. My ppa ghc was 7.4,
which is cartoonishly outdated and which stack will yell at you about
if you try to use it as global ghc. So: stack setup and it'll install
ghc, right?

No. First, I found that stack kept repeatedly freezing while
downloading ghc 8.2, then starting over again. Sometimes the resource
would vanish. When it did manage to download entirely, it'd attempt to
unpack all 1.4gb into about half that amount of tmpfs. I knew that the
tmpfs thing was a known issue, so I cleverly set $TMPDIR=~/tmp. Then I
discovered that stack was not obeying this environment variable, and
persisted in attempting to jam 10 gallons of shit into a 5 gallon
bucket.

My tmpfs was half of total ram, and I my *free space* was about 1.5gb
anyway. I manually plopped the ghc-8.2 tarball into where stack
expected it, bypassing stack's dodgy download process, and then tried
to see if I could bypass stack in building it, taking advantage of an
actual tmp directory. No dice: just not enough actual space for that.

So I moved my chroot out of internal storage and into an sdcard with
50gb of free space. This move was one command, worked instantly, and I
haven't seen any performance hit whatsoever. My filesystem now had
plenty of space for updating from trusty to xenial (and ghc 7.4 to
7.10, which stack won't yell about).

So I upgraded to xenial. Everything went absolutely smoothly. The only
thing I had to tweak was that tmux's updated version collapsed several
mouse options into one, so I just had to replace them with that one
setting. 

I had plenty of space, a modern enough ghc, and the will to keep
fighting stack. 

Round 2. Xenial has haskell-stack in its repo. I installed it, and
began working on the tmpfs problem. I discovered that it wasn't
listening to fish; I had to switch to zsh in order to set $TMPDIR such
that it'd actually listen. This turned out to be a known issue
since 2015. Stack will yell at you if you attempt to use a version
below 1.4, so I had to upgrade it before I could install ghc 8.2.

I opened zsh in a pane, exported TMPDIR=~/tmp, and ran stack
upgrade. Switched to another pane, cd'd to tmp, and stuff was going
on! Things were happening! Compilation failed at 27/34 modules,
something about ZLib compression having set invalid code lengths. Hey,
at least it wasn't my fault. I ran it again, this time it said only 29
modules were needed. It compiled all of them, exited successfully, and
*the version was not changed.* The successful exit was a lie, it had
not actually upgraded to 1.4. In a rage I uninstalled it and wiped
~/.stack.

I knew now that manually plopping things where stack expects them
works, and that stack needs a non-fish shell interaction.

Round 3. I installed stack from gethaskellstack, so I would have 1.4
and wouldn't have to be distracted by upgrading it. I opened a zsh
pane, set TMPDIR=~/tmp, and then ran stack setup --git. It yelled that
there was no package index, tried to download it, and then gave up
saying the resource had vanished. I tried stack update --git. This caused
stack to scream that there was no package index, and then try to
download it, and then exit after the aws resource "vanished." I ran it
again with -v and discovered that the mirror it's pointing at, simply
doesn't respond. It turns out this is a known issue, as well. 

So: I needed to get that package index without relying on the
mirror. I google-fu'd and found the json it was trying to get, and
downloaded it into my frog static site. I redirected the url stack
update was trying to get to into a localhost frog server, and
voila. It installed the package index, and exited successfully. I then
ran stack setup --git -v, and it miraculously began downloading
ghc-8.2 *without any interruptions*. It downloaded the entire thing,
then froze on installing ghc for 48 minutes. Then, exited
successfully.

Right now it appears that stack is up and running, with a local ghc
that is sufficiently up to date that it should stop yelling at me. 
