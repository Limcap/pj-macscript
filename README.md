# MacbookPro2015SleepFix

### 1 Should I use this script?

This tool is for people who bought the Macbook Pro 2015 retina with force touch
and are having issues with the sleep feature. The computer will keep waking up
frequently for reasons such as "ART", "Network". You can check if you have that
issue by typing 
$ syslog | grep -i "Wake reason"
in terminal and checking the log that is shown.

I had that problem and my notebook kept waking up literaly every minute,
draining the battery a lot faster than it should. Some of the times, if
the notebook was asleep for too many hours (i.e.: during the night) it
would heat up a lot and eventually shut down completely (it was necessary to
press the power button for 15 seconds for the computer to turn on again)

Even ater the OSx upgrade for the El Captain version this problem is still
present. I found out that the best workaround is to turn the Airport off
before putting the mackbook pro to sleep. Therefore I created this script
that will automate this process.

If you have been experiencing similar issues, this tool will probably
help you with it.


### 2 How does it works?

It will automatically turn off the airport from your notebook as soon as you
put the computer to sleep, and will turn it on again when you wake it up,
effectively solving the problem.

This tool installs SleepWatcher v2.2 (local user) from tool
[http://www.bernhard-baehr.de/](http://www.bernhard-baehr.de/)
and a personalized script fo the wakescript and sleepscript that actually does
the fix.

**If you already have this tools installed in you macbook pro, this script
will overwrite the files you already care. Be warned.** 

### 3 Installation and Removal

To install it, open the terminal, go to the folder of the script and type:
```bash
$ sh sleepfix-install.sh
```

To remove it, type:
```bash
$ sleepfix sh-install.sh remove
```