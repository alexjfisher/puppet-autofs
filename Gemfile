source "https://rubygems.org"

group :test do
  gem "rake"
  if puppet_gem_version = ENV['PUPPET_GEM_VERSION']
    gem "puppet", ENV['PUPPET_GEM_VERSION']
  elsif puppet_git_url = ENV['PUPPET_GIT_URL']
    gem "puppet", :git => "#{puppet_git_url}"
  else
    gem "puppet", ENV['PUPPET_GEM_VERSION']
  end
  gem 'puppet-strings'
  gem 'yard'
  gem 'redcarpet'
  gem 'github-markup'
  gem "puppet-lint"
  gem "puppet-lint-unquoted_string-check"
  gem "rspec-puppet"
  gem "puppet-syntax"
  gem "puppetlabs_spec_helper"
  gem "metadata-json-lint"
  gem "rspec"
  gem "rspec-retry"
  gem "simplecov", :require => false
  gem "codeclimate-test-reporter", :require => false
end

group :system_tests do
  gem "beaker-puppet_install_helper", :require => false
  gem "specinfra", "~> 2"
  gem "beaker-rspec"
  gem "beaker", "~> 2"
end

group :development do
  gem "travis"
  gem "travis-lint"
  gem "puppet-blacksmith"
  gem "guard-rake"
  gem "pry"
  gem 'parallel_tests' # requires at least Ruby 1.9.3
  gem 'rubocop', :require => false # requires at least Ruby 1.9.2
end
