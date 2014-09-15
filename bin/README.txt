So what is diffview,

    $ diffview without args do a: lsdiff --number

    $ diffview with args (for example "-F2-") do a filterdiff $* (all args), so defaults --number

after I have two scripts each, for working with git or svn ,

for svn I got: svndiff and viewdiff (as short name of svnviewdiff)

    $ svndiff (without args) will give the list of files modified

    $ svndiff -F1 (with args) will show the patch of file #1

    $ viewdiff (without args) pipe all patch with filerdiff to vim - -R (in ready only mode, easy to quit) , I see colored and complete patch,

    $viewdiff -F1 (with args) , it will pipe patch of file #1 to vim - -R

for git I have samething: gitdiff and gitviewdiff

and finally we can do scripts in one line, for example like this one, that I call it difftotrunk.sh:

    diff ~/prodution/svn . -ru -x .svn -x local.defs | diffview $*

to view differences of to directories and ./difftotrunk.sh (with args) will give the list of files that I change in devel

    $ ./difftotrunk.sh -F1 , will show the patch of file #1.


