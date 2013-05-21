HubFlow
=======

Adds the 'git hf' Git extension to provide high-level repository operations
for [DataSift's HubFlow branching model](http://datasift.github.com/gitflow/), which is based on [Vincent Driessen’s original blog post](http://nvie.com/posts/a-successful-git-branching-model/).

![](http://nvie.com/img/2009/12/Screen-shot-2009-12-24-at-11.32.03.png)

Installation
------------

1. `git clone git@github.com:socialpoint/gitflow.git`
2. `cd gitflow`
3. `sudo ./install.sh`

Windows users will need something like Cygwin in order to use this extension.

Upgrading To The Latest Version
-------------------------------

Upgrading to the latest version of the HubFlow tools is very easy:

1. `sudo git hf upgrade`

Getting Started
---------------

Run `git hf init` on your repository folder

If you want to work with fork support in your repository you have two options:
1. Answer Y when the script asks if you want to use forks and specifying user name
2. Run init specifying the fork user name directly on init script parameters `git hf init --fork=patterComunitatis`

Now, your HubFlow is ready to fetch and pull from the origin, but to push changes to your fork remote.

An example of the git repo config file (.git/config):

    [hubflow]
            featureOrigin = fork
    [hubflow "branch"]
            master = master
            develop = develop
    [hubflow "prefix"]
            feature = feature/
            release = release/
            hotfix = hotfix/
            support = support/
            versiontag =
    [remote "fork"]
            url = git@github.com:smoya/sp-platform-basev2.git
            fetch = +refs/heads/*:refs/remotes/fork/*

See our tutorial website to learn more about the [GitFlow](http://datasift.github.com/gitflow/IntroducingGitFlow.html) branching model and [how to use the HubFlow tools](http://datasift.github.com/gitflow/GitFlowForGitHub.html).

Changelog
---------

To see what's new in each release, see our [Changelog](http://datasift.github.com/gitflow/ChangeLog.html).

License Terms
-------------
HubFlow is published under the liberal terms of the BSD License, see the
[LICENSE](LICENSE) file. Although the BSD License does not require you to share
any modifications you make to the source code, you are very much encouraged and
invited to contribute back your modifications to the community, preferably
in a Github fork, of course.