source 'https://rubygems.org'

if RUBY_VERSION =~ /^1\.8/
  rakeversion = "< 11"
  parallel_testsversion = "< 1.1.0"
else
  rakeversion = ">= 10.1.1"
  parallel_testsversion = ">= 1.1.0"
end

gem 'rake', rakeversion
gem 'rspec-its'
gem 'puppet-lint', '>= 0.3.2'
gem 'rspec-puppet', '~> 2.1.0'
gem 'puppetlabs_spec_helper',   :require => false
gem 'puppet-syntax', '>= 1.1.0'
gem 'json'
gem 'puppet', ENV['PUPPET_VERSION'] || '~> 3.5'
gem 'metadata-json-lint'
gem 'retries', '~> 0.0.5'
gem 'travis', '~> 1.8'
gem 'parallel_tests', parallel_testsversion
gem 'rubocop', '~> 0.39'

group :development do
  gem 'simplecov'
  gem 'ci_reporter'
  gem 'debugger', :platform => :mri_19
  gem 'debugger-pry', :platform => :mri_19
  gem 'byebug', :platform => [:mri_20, :mri_21]
  gem 'pry'
  gem 'pry-byebug'
end

group :system_tests do
  gem 'beaker-rspec',  :require => false
  gem 'serverspec',    :require => false
  gem 'vagrant-wrapper',:require => false
  gem 'beaker-puppet_install_helper', :require => false
  if RUBY_VERSION =~ /^1\.8/
    gem 'addressable', '< 2.4'
    gem 'highline', '< 1.7.0'
    gem 'parallel', '< 1.3.4'
    gem 'rainbow', '< 2.1.0'
  end
end
