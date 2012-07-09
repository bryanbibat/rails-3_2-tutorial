# Installing Ruby on Rails

This section will cover how to install a Ruby on Rails development environment on Windows and Linux. For the sake of simplicity, we'll assume you're using Ubuntu 12.04 for the entire _Installing on Linux_ section.

## Installing on Windows

Download and use the latest **RailsInstaller** from [http://railsinstaller.org/](http://railsinstaller.org/). This installer already includes Ruby 1.9.3, Rails 3.2.6, SQLite 3 as well as Git and essential tools for building native extensions in Windows.

A smaller alternative would be **RailsFTW** from [http://railsftw.bryanbibat.net/](http://railsftw.bryanbibat.net/). This installer does not contain Git and build tools (you can download them separately from [http://git-scm.com/downloads](http://git-scm.com/downloads) and [http://rubyinstaller.org/downloads/](http://rubyinstaller.org/downloads/), respectively), but it's smaller and includes MySQL support.

Don't worry if these installers using slightly older versions of Rails; they will still work with the examples in this book.

## Installing on Linux

### Installing RVM

There are several ways of installing Ruby in Linux. Here we will be using **Ruby Version Manager** (RVM) which will handle the installation for us. RVM requires Git, curl and essential build tools, while Ruby, Rails, and SQLite have their own requirements. We install them all using:

    $ sudo apt-get install curl build-essential git-core bison openssl libreadline6 \
    libreadline6-dev zlib1g zlib1g-dev libssl-dev libyaml-dev libxml2-dev libxslt-dev \
    ncurses-dev autoconf automake libtool bison subversion libc6-dev libsqlite3-0 \
    libsqlite3-dev sqlite3 nodejs

Also, note the inclusion of the `nodejs` package which will be used by Rails later. You can remove that entry if you already have Node.js installed on your machine.

After installing the required packages, we install RVM using the following command:

    $ curl -L https://get.rvm.io | bash -s stable --ruby

_TODO: notes for older versions of Ubuntu_

### Installing Rails and SQLite

Installing Rails and SQLite is a matter of calling RubyGems, Ruby's package manager. Thanks to RVM, we do not need to have admin rights to install Rails. Open a new terminal window to startup RVM and run the following commands:

    $ gem install rails -v=3.2.6
    $ gem install sqlite3


