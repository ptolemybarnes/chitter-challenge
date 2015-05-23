require 'cucumber/rake/task'
require 'rspec/core/rake_task'
require 'rubocop/rake_task'

RuboCop::RakeTask.new :cop
RSpec::Core::RakeTask.new :spec
Cucumber::Rake::Task.new :cuke

task :default do
  %x( bundle exec rackup )
end

task test: [:cop, :spec, :cuke]
