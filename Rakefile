require 'pry'

task :environment do
  require_relative './config/environment'
end

desc 'outputs hello to the terminal'
namespace:greeting do
  task :hello do
    puts "hello from Rake!"
  end

  task :hola do
    puts "hola de Rake!"
  end
end

desc 'drop into Pry'
task :console => :environment do
  Pry.start
end

namespace:db do
  task :migrate => :environment do
    require_relative './config/environment'
  end
  
  desc 'seed the database with some dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end



# desc 'outputs hola to the terminal'
# task :hola do
#   puts "hola de Rake!"
# end

