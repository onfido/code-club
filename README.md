# Code Club

Resources for our ongoing Code Club (engineering for non-engineers) sessions

## Lessons

1. [Race through Ruby](content/01_ruby.md)
2. [Cloning, pulling, pushing](content/02_version_control.md)
3. [The web and rails](content/03_rails.md)
4. [A home for our data](content/04_persistence.md)
5. ???

## The project

[insert game here] ladder & challenge app [todo: requirements]

## Getting started

First up, install the following tools:

1. [Git](http://git-scm.com/) (on Windows, you'll also need to add to your [path](http://blog.countableset.ch/2012/06/07/adding-git-to-windows-7-path/))
2. [VirtualBox](https://www.virtualbox.org/)
3. [Vagrant](https://www.vagrantup.com/)
4. Text editor of your choice (most of us use [Sublime Text](http://www.sublimetext.com/); you could also try Notepad++ or Atom)
5. (Optional) [Sourcetree](http://www.sourcetreeapp.com/)

Git is a *version control tool*: these tools are used to manage changes, share and track the history of a codebase.  Vagrant is a tool for quickly provisioning virtual machines (VMs).  We'll use this to launch pre-configured machines that are ready for development and consistent regardless of host OS (Mac, Linux, Windows...)

Once you've got everything installed, please try and get a basic Vagrant instance up and running:

  1. Open a terminal window (`Terminal` on a Mac, `Powershell` or `cmd` on Windows)
  2. Create a new directory and cd there (cd means "change directory)
  3. Run `vagrant init hashicorp/precise32`
  4. Run `vagrant up`
  5. Once the machine is up and running, try and run `vagrant ssh` (ssh stands for [Secure Shell](http://en.wikipedia.org/wiki/Secure_Shell))
  6. All going well, you should now be logged into a virtual machine running Ubuntu.
  6. If you're happy, type `exit`, and then `vagrant halt` or `vagrant destroy`

Right. Let's get developing.

  1. Open a terminal window again
  2. Clone this repository to your computer (type the following in your terminal `git clone https://github.com/onfido/code-club.git`).  We'll talk about what this means in our 2nd lesson
  3. Run `cd code-club/box`
  4. Run `vagrant up`
  5. When that's complete, run `vagrant ssh`
  6. Run `cd ../../vagrant`.  This directory is shared with your host machine
  7. Run `rails new test-app`.  This will create a new rails application.  Run `cd test-app`.
  8. Run `rails server -b 0.0.0.0`.  This starts a new server running `test-app`
  9. From your host computer, navigate to localhost:3030.  All going well, this should show your new Rails app!

## Useful resources

+ https://www.codeschool.com/courses/rails-for-zombies-redux
+ https://www.codeschool.com/courses/try-git
+ http://mislav.uniqpath.com/poignant-guide/
+ http://learnrubythehardway.org/book/
+ http://tryruby.org/levels/1/challenges/0
+ https://rubymonk.com/
+ https://github.com/RailsApps/rails-composer
