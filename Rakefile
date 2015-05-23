

task :default do
  `bundle exec rackup`
end

task test: [:cop, :rspec, :cuke]

begin
  require 'cucumber/rake/task'
  require 'rspec/core/rake_task'
  require 'rubocop/rake_task'
  RuboCop::RakeTask.new :cop
  RSpec::Core::RakeTask.new :rspec
  Cucumber::Rake::Task.new :cuke
rescue LoadError => e
  puts "Test dependencies could not be loaded"
end


