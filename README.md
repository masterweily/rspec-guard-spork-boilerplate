# RSpec-guard-spork Boilerplate

A boilerplate project template for Ruby to kickstart behaviour-driven development using RSpec.

I prefer guard to autotest/autospec.  It's file watcher is easily configured and very versatile.  Running spork in the background speeds up the testing process even more.

# Create a Project

You won't like to inherit this repository's revision history.  Here's how to checkout the plain project files only.

You need to clone this repository on your machine before you proceed.

## Copy via `git-checkout-index`

The following command will checkout the boilerplate to `/full/path/to/new/project/`.  **It'll overwrite existing files.**

    cd /path/to/rspec-guard-spork-boilerplate/
    git checkout-index -f -a --prefix=/full/path/to/new/project/ 
    #        the trailing slash is super important!  ----------^
    
This will copy all files from the boilerplate's index to the path specified for `--prefix=`.  The destination path **must end with a slash** or else unexpected things will happen.

## Archive and Extract Boilerplate Folder

You could also use `git-archive` and re-use the archive to kickstart projects:

    git archive -o archive.tar HEAD

Shorthand for archiving and extracting at a destination of your choice:

    git archive --format=tar --prefix=your-project-name/ HEAD | (cd your/projects/folder && tar xf -)


# Test-Driving your Project

Just install the bundles:

    bundle install

Simply type

    guard
    
and there you are.

# License

This code is in the Public Domain.  See [LICENSE](./LICENSE)
