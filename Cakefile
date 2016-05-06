require 'shortcake'

use 'cake-test'
use 'cake-version'
use 'cake-publish'

option '-b', '--browser [browser]', 'browser to use for tests'
option '-g', '--grep [filter]',     'test filter'
option '-t', '--test [test]',       'specify test to run'
option '-v', '--verbose',           'enable verbose test logging'

task 'clean', 'clean project', ->
  exec 'rm -rf lib'

task 'build', 'build project', ->
  exec 'coffee -bcm -o lib/ src/'

task 'build:min', 'build project', ['build'], ->

task 'watch', 'watch for changes and recompile project', ->
  exec 'coffee -bcmw -o lib/ src/'
