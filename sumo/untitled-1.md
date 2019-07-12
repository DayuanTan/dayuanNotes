# SUMO: error: typemap file "/usr/share/sumo/data/typemap/osmPolyconvert.typ.xml" not found

When you are learning **SUMO** using **Tutorials/OSMWebWizard** \([http://sumo.sourceforge.net/userdoc/Tutorials/OSMWebWizard.html](http://sumo.sourceforge.net/userdoc/Tutorials/OSMWebWizard.html)\).

You followed instructions from the **tutorial** and went into the directory /usr/share/sumo/tools.

After you clicked "Generate Scenario" and you waited for a long time. Then you checked your terminal you found an error:

```text
osmWebWizard.py: error: typemap file "/usr/share/sumo/data/typemap/osmPolyconvert.typ.xml" not found
Traceback (most recent call last):
  File "osmWebWizard.py", line 379, in build
    builder.build()
  File "osmWebWizard.py", line 187, in build
    osmBuild.build(options)
  File "/usr/share/sumo/tools/osmBuild.py", line 68, in build
    optParser.error('typemap file "%s" not found' % options.typemap)
  File "/home/tan/anaconda3/lib/python3.6/optparse.py", line 1569, in error
    self.exit(2, "%s: error: %s\n" % (self.get_prog_name(), msg))
  File "/home/tan/anaconda3/lib/python3.6/optparse.py", line 1559, in exit
    sys.exit(status)
```

I didn't find a good solution to this problem. The official community website didn't answer this question very well \([https://www.mail-archive.com/search?l=debian-bugs-dist@lists.debian.org&q=subject:%22Bug%23899345%5C%3A+sumo%5C%3A+Should+include+data+directory+in+package%22&o=newest&f=1](https://www.mail-archive.com/search?l=debian-bugs-dist@lists.debian.org&q=subject:%22Bug%23899345%5C%3A+sumo%5C%3A+Should+include+data+directory+in+package%22&o=newest&f=1)\)

### Solution:

All you need to do is just go to [SUMO github website](https://github.com/eclipse/sumo) and download their all files and copy 'data' directory into /user/share/sumo. 





