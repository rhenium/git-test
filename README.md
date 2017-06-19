git-test
========

git-test is a script for running tests on commits in a Git repository.
It is useful for those who care whether every commit in a topic branch passes
the test.

git-test uses git-worktree(1) and runs the test inside a linked working tree
so that the current working tree doesn't become polluted; you can make any
changes to the local tree while running git-test in background.

For a typical topic branch workflow it is simply:

    # First define the test commands for the project
    git config --add git-test.test 'rake compile'
    git config --add git-test.test 'rake test'

    # By default every commit in master..HEAD is tested
    git test

Usage
-----

TODO: This needs to be documented.

License
-------

git-test is licensed under the MIT license. See COPYING.
