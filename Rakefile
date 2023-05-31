namespace :greeting do
desc "print out 'hello from Rake!' "
task :hello do
  puts "hello from Rake!"
end
desc "print out 'hola de Rake!'"
task :hola do
  puts 'hola de Rake!'
end


end

desc 'drop into the Pry console'
task console: :environment do
  Pry.start
end

namespace :db do

  desc 'migrate changes to your database'
  task migrate: :environment do
    Student.create_table
  end

  desc 'seed the database with some dummy data'
  task seed: :environment do
    require_relative './db/seeds'
  end
end

task :environment do
  require_relative './config/environment'
end

