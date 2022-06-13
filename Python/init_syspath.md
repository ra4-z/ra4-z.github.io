# What is proble
We need to provide a package as a whole some time, like to make it a black box for others to use. We may do all the stuff inside the directory, but what we want is to import it from outside. 
So, here are some great tips.

```python
# e.g.
.
├──procedure.py
├──mypackage
    ├── subpackage_1
    │   ├── test11.py
    │   └── test12.py
    ├── subpackage_2
        ├── test21.py
        └── test22.py

```

# Solution 1: Adding a system path to the very beginning
```python
# In the file procedure.py
import sys
sys.path.append('./mypackage/')
```
In this way, everything will be taken care of like the file is in the directory `mypackage`.

This move is really simple, but it's noticed that some names can be multi-imported.



# References
[Python __init__.py 作用详解](https://www.jianshu.com/p/73f7fbf75183)