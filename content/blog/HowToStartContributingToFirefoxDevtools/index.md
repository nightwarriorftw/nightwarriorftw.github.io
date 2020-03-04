---

title: How to Start Contributing to Firefox Devtools ?
date: "2020-03-04T17:12:33.962Z"
---

Firefox Devtools is a complex app. However, if you have a good knowledge of HTML,CSS and Javascript you can easily start contributing. In order to start contributing to Firefox Devtools you first need to setup codebase and follow few steps.

### Getting a Bugzilla Account
Mozilla's Bug tracker is Bugzilla. You first need to setup an Bugzilla account [here](https://bugzilla.mozilla.org/)

### Getting and Building the Code
There are few steps we have to follow in order to get and build the code.

    - Install Mercurial

Install mercurial, if you haven't.

```
apt-get install mercurial
```

    - Get the code
The `mozilla-central` is a very big repository with size >= 2GB, so it might take time to pull changes. Moreover you need to be patient and have 40GB free disk space.

```
hg clone https://hg.mozilla.org/mozilla-central
```

If your internet connection is slow, or you face errors while pulling the codebase, you can go through [this](https://developer.mozilla.org/en-US/docs/Mozilla/Developer_guide/Source_Code/Mercurial/Bundles)

Remember there are other ways to, like writing a script and pulling the codebase in chunks.


    - Building and running locally
Try building Firefox and downloading dependencies by running this command

```
./mach bootstrap
```
After this command finishes you might be asked to make a file called `mozconfig` and write few lines to it.

```
# Automatically download and use compiled C++ components:
ac_add_options --enable-artifact-builds
```

Make sure to add the above lines to the respective file mentioned above as this is an addons step not to build Mozilla Nightly from scratch. In Layman's language it is bascially using `Artifacts Mode` to build Mozilla Nighty. 

Then run this:

```
./mach configure
./mach build
```

    - To run the Firefox you just compiled:

```
./mach run
```

    - To rebuild use

```
./mach build faster
```


### Pick a bug and start work
Next step is to pick a bug and start working on it. You can pick bugs either from [here](https://bugs.firefox-dev.tools/?easy&tool=all) or from [Bugzilla itself](https://codetribute.mozilla.org/projects/devtools?project%3DAll%26assignee%3DAny)

### Push and get reviewed
Push the code to the Phabricator and get your patch reviewed from the mentor. Remember you first need to setup an [Phabricator account](https://moz-conduit.readthedocs.io/en/latest/phabricator-user.html#creating-an-account). Also you should once go through [this](https://docs.firefox-dev.tools/contributing/code-reviews-setup.html), inorder to get more clear.

In order to push your commit to Phabricator, you need to install [moz-phab](https://moz-conduit.readthedocs.io/en/latest/phabricator-user.html#using-moz-phab).

Make changes to the file and run this

```
hg add /path/to/file/changed
hg commit -m "Bug 1112233 - Implement something. r=name,.."
```
The above commit command has a specific format of writing a commit message which goes like this

```
Bug 1112233 // Bug number
Implement something // commit message
r=name // name to the reviewer.
```

There are also some steps that you need to take care of like running test before pushing such that you don't break anything.

This is just a basic starting document for more detailed description you can refer [this](https://docs.firefox-dev.tools/contributing/code-reviews-setup.html)
