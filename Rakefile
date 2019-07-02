require 'standalone_migrations'
require_relative "config/environment"

StandaloneMigrations::Tasks.load_tasks

desc 'Start IRB with application environment loaded'
task "console" do
  exec "irb -r ./config/environment"
end

namespace :db do
  desc "populate the database with sample data"
  task :seed_fix do
    require APP_ROOT.join('db', 'seeds.rb')
  end
end