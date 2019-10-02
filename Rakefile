namespace :greeting do 
desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end

desc "outputs hallo to the terminal bash"
task :hallo do 
  puts "greeting from plannet suturn"
  end
end

task :environment do 
  require_relative './config/environment'
end

namespace :db do
  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
  end
end

namespace :db do 
  desc 'seed the database with some dummy data'
  task :seed do 
    require_relative './db/seeds.rb'
  end
end

desc 'drop into Pry console'
task :console => :environment do 
  Pry.start 
end