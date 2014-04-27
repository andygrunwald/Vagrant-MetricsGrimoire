Vagrant-MetricsGrimoire
=======================

Vagrant setup to play with the [MetricsGrimoire toolset](https://github.com/MetricsGrimoire).

This setup uses the [Chef provider](http://www.getchef.com/chef/) with the cookbooks for:

* [repositoryhandler](https://github.com/andygrunwald/chef-repositoryhandler)
* [cvsanaly](https://github.com/andygrunwald/chef-cvsanaly)

## Requirements

* Vagrant >= 1.5

## Usage

* Clone it (`git clone https://github.com/andygrunwald/Vagrant-MetricsGrimoire.git`)
* Switch to the directory (`cd Vagrant-MetricsGrimoire`)
* Get submodules (`git submodule init && git submodule update`)
* Start the machine (`vagrant up`)
* Login to the machine (`vagrant ssh`)
* Play around with
** CVSAnaly (`cvsanaly2 --help`)

## License

This project is released under the terms of the [MIT license](http://en.wikipedia.org/wiki/MIT_License).

## Contributing

* Fork and clone it (`git clone https://github.com/andygrunwald/Vagrant-MetricsGrimoire.git`)
* Create your feature branch (`git checkout -b my-new-feature`)
* Make your changes (hack hack hack)
* Commit your changes (`git commit -am 'Add some feature'`)
* Push to the branch (`git push origin my-new-feature`)
* Create new Pull Request
