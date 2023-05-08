Download Link: https://assignmentchef.com/product/solved-scrambler
<br>
<a href="https://www.youtube.com/playlist?list=PLhOuww6rJJNPcLby3JXlKSo6duCIjh93S" rel="nofollow">https://www.youtube.com/playlist?list=PLhOuww6rJJNPcLby3JXlKSo6duCIjh93S</a>

Write a program that will randomly scramble the middle parts of words of 3 letters or more in a given text which may come from the command line:

<pre><code>$ ./scrambler.py 'The quick brown fox jumps over the lazy dog.'The qiuck bwron fox jmpus over the lzay dog.</code></pre>

Or from an input file:

<pre><code>$ ./scrambler.py ../inputs/fox.txtThe qucik borwn fox jpmus over the lazy dog.</code></pre>

The program should accept a <code>-s</code> or <code>--seed</code> value for the random seed to ensure reproducibility:

<pre><code>$ ./scrambler.py -s 1 ../inputs/fox.txtThe qicuk bwron fox jupms over the lazy dog.</code></pre>

It should print a usage if provided no arguments:

<pre><code>$ ./scrambler.pyusage: scrambler.py [-h] [-s int] strscrambler.py: error: the following arguments are required: str</code></pre>

And a longer usage for <code>-h</code> or <code>--help</code>:

<pre><code>$ ./scrambler.py -husage: scrambler.py [-h] [-s int] strScramble the letters of wordspositional arguments:  str                 Input text or fileoptional arguments:  -h, --help          show this help message and exit  -s int, --seed int  Random seed (default: None)</code></pre>

Run the test suite to ensure your program is working correctly:

<pre><code>$ make testpytest -xv test.py============================= test session starts ==============================...collected 7 itemstest.py::test_exists PASSED                                              [ 14%]test.py::test_usage PASSED                                               [ 28%]test.py::test_text1 PASSED                                               [ 42%]test.py::test_text2 PASSED                                               [ 57%]test.py::test_file_bustle PASSED                                         [ 71%]test.py::test_file_fox PASSED                                            [ 85%]test.py::test_file_spiders PASSED                                        [100%]============================== 7 passed in 0.72s ===============================</code></pre>