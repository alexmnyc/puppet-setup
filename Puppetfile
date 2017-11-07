#!/usr/bin/env ruby
#^syntax detection

## Test with librarian-puppet if you have all dependencies listed
## Exclude modules you don't need
# librarian-puppet install --verbose --clean

## r10k also can install the modules from the Puppetfile,
## but does not resolve dependencies
# r10k puppetfile install

## don't pull from forge, I want all from git.
#forge "https://forgeapi.puppetlabs.com"
forge 'http://localhost'

mod 'puppetlabs-stdlib',
  :git => 'https://github.com/puppetlabs/puppetlabs-stdlib',
  :ref => 'master'

mod 'rnelson-hiera_resources',
  :git => 'https://github.com/rnelson0/puppet-hiera_resources.git',
  :ref => 'master'

## Owncloud
mod 'shoekstra/owncloud',
  :git => 'https://github.com/shoekstra/puppet-owncloud.git',
  :ref => 'master'

## owncloud dependencies:
## exclude conflicting and modules unnecessary on ubuntu
exclusion 'ckhall-remi'
exclusion 'stahnma-epel'

## alternative to nanliu-staging
exclusion 'nanliu-staging'
mod 'puppet-staging',
  :git => 'https://github.com/puppet-community/puppet-staging.git',
  :ref => 'master'
