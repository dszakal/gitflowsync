# Gitflowsync

Installation:

Go to the folder in your terminal where you checked out the repo, there type

    sudo cp gitflowsync /usr/bin/gitflowsync
    sudo chmod o+x /usr/bin/gitflowsync

Updating to latest version:

Are you up to date?

    diff ./gitflowsync /usr/bin/gitflowsync && echo 'up to date' || echo 'not up to date'

If not, repeat the steps stated in installation. You need to do it manually after "git pull".

Usage:

You need to be in your git project's folder, and you need to have existing git flow master and develop branches (in your local and on origin).

Pull current (if it is not master or develop), master and develop branches:

    $ gitflowsync pullonly

Pull and then push current (if it is not master or develop), master and develop branches, and push tags:

    $ gitflowsync push

The script will stop with exit code 1, where git pull or git push fails (because of conflicts, non existing branch (pullonly), or other git error).

