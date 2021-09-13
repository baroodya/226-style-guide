This is likely the first time you have encountered import statements
in code. The point of an import statement is to tell your computer 
where to find the module that you are importing so that it can access 
it. In COS 126, this step was performed automatically by the IDE; now,
it is your responsibility to import modules for use in your code.

All import statements should go at the top of your file, only after
a header comment. There should be no code above the import statements 
to ensure that every module you need to use is imported by the time
that line of code is executed. Although it might seem more appropriate
to import a module right before you use it, many modules are used throughout
a file and scattering import statements throught code can make it difficult 
to read.

It is also important to only import those modules you need. In addition to 
saving space (your computer will only access the required modules instead of 
loading an entire package), it is more clear to a reader what you intend to do in
the rest of the code. for example, if I wanted the ability to use the built in 
`Java.awt.color` Module, I should make my import statement:

```
import Java.awt.color;
```

instead of 

```
import Java.awt.*;
```

Further, it is **Bad Style** to import the entire `algs4` package for every file.
Instead, you should only import the modules you need:

```
import edu.princeton.cs.algs4.*;
```

is bad style, while

```
import edu.princeton.cs.algs4.Picture;
import edu.princeton.cs.algs4.Queue;
import edu.princeton.cs.algs4.ST;
import edu.princeton.cs.algs4.StdIn;
import edu.princeton.cs.algs4.StdOut;
```