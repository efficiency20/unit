require 'rspec/core/rake_task'
require 'bundler'

ENV["RUBYGEMS_HOST"] = "http://localhost:2000"

Bundler::GemHelper.install_tasks

task :default => :spec

desc "Run specs"
task :spec => ["spec:no_dsl", "spec:dsl"]

namespace :spec do
  desc "Run specs without DSL"
  RSpec::Core::RakeTask.new(:no_dsl) do |t|
    t.rspec_opts = "-t ~dsl"
  end

  desc "Run specs with DSL"
  RSpec::Core::RakeTask.new(:dsl) do |t|
    # Run all tests
  end
end

task :push do
  puts "Use rake release instead"
  exit 1
end
