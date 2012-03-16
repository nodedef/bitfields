task :spec do
  sh "rspec spec"
end

task :default do
  sh "AR=2.3.14 && (bundle || bundle install) && bundle exec rake spec"
  sh "AR=3.0.10 && (bundle || bundle install) && bundle exec rake spec"
  sh "AR=3.1.1 && (bundle || bundle install) && bundle exec rake spec"
end

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = 'bitfields'
    gem.summary = "Save migrations and columns by storing multiple booleans in a single integer. Variation on Micheal Grosser's version http://github.com/grosser/#{gem.name}."
    gem.email = "driedtoast@gmail.com"
    gem.homepage = "http://github.com/nodedef/#{gem.name}"
    gem.authors = ["Daniel Marchant"]
  end

  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler, or one of its dependencies, is not available. Install it with: sudo gem install jeweler"
end
