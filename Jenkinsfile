node {
  deleteDir()
  checkout scm
  echo 'beginnning workflow...'

  stage 'prepare gems'
  sh '''#!/bin/bash
<<<<<<< HEAD
  source /usr/local/rvm/scripts/rvm
=======
  source usr/local/rvm/scripts/rvm
>>>>>>> master
  bundle install --path=.bundle/gems/
  '''

  stage 'syntax testing'
  sh '''#!/bin/bash
<<<<<<< HEAD
  source /usr/local/rvm/scripts/rvm
=======
  source usr/local/rvm/scripts/rvm
>>>>>>> master
  bundle exec puppet parser validate manifests/
  '''

  stage 'lint testing'
  sh '''#!/bin/bash
<<<<<<< HEAD
  source /usr/local/rvm/scripts/rvm
  bundle exec puppet-lint --no-autoloader_layout-check manifests/*.pp
=======
  source usr/local/rvm/scripts/rvm
  bundle exec bundle exec puppet-lint --no-autoloader_layout-check manifests/*.pp
>>>>>>> master
  '''

  stage 'rspec testing'
  sh '''#!/bin/bash
<<<<<<< HEAD
  source /usr/local/rvm/scripts/rvm
=======
  source usr/local/rvm/scripts/rvm
>>>>>>> master
  bundle exec rake spec
  '''

  stage 'smoke testing'
  sh '''#!/bin/bash
<<<<<<< HEAD
  source /usr/local/rvm/scripts/rvm
=======
  source usr/local/rvm/scripts/rvm
>>>>>>> master
  bundle exec rake spec_prep
  puppet apply tests/init.pp --noop --modulepath=spec/fixtures/modules
  '''

  stage 'deploy'
<<<<<<< HEAD
  echo 'deploy to test branch'
=======
  echo 'deploy to puppet masters'
>>>>>>> master
}
