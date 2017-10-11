# DRSH

I'm a long time user of [Drash](http://dra.sh/), an iPhone app that quickly
looks up if it's going to rain or not. I've asked @inferis about a Mac version
but sadly he doesn't have the time at the moment. So to scratch my own personal
itch, and learn more about the exciting world of shell scripting:

      DRSH - Drash for the command line

# What does it do?

     drsh Achel
     => ▁▁▆▇▇▇██▇▆▆▇▇▆▁▁▁▆▆▁▁▁▁▁▁ (3930 Achel, Belgium)

# How do I install it?

`drsh` is a simple shell script, so drop it anywhere in your `$PATH` and you should
be ready to go. It does have two dependencies [jq](http://stedolan.github.io/jq/) and
[spark](https://github.com/holman/spark), but those are simple to install.

(Homebrew has them both, so `brew install jq && brew install spark`).

(Here's to the lazy ones. The unfits. The rebels. The troublemakers. The round pegs in
the square holes:

     brew install https://gist.githubusercontent.com/pjaspers/6577968/raw/fb5ef7ceaa8dd661905468d588aaa1738037524d/drsh.rb
)

Or you could do: `curl -O https://raw.github.com/pjaspers/drsh/master/drsh` to a place
in your `$PATH`.

# What's missing?

1. At this point in time the bars don't actually reflect the amount of rain that will
fall, I just pass the data on to [spark](https://github.com/holman/spark) and it
assumes that the highest number I pass in is the maximum (but max is actually 255).

2. International support? But since I'm probably not going to need this, send me a
patch if you need it.

3. Less dependencies. I'll admit I mainly used `jq` to mess around with it, I'm pretty
sure we could ditch it and do some fancy `grep`, `awk`,`sed` and get the same results
without the dependency. Likewise for `spark`, it would be better to just show the chance
of rain if `spark` wasn't found.

4. More cowbell
