require 'rubygems'
require 'rake'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    summary = "A Ruby on Rails plugin that puts a countdown timer on the session object"
    gem.name = "session_countdown"
    gem.summary = summary
    gem.description = summary
    gem.email = "gems-kevdev@snkmail.com"
    gem.homepage = "http://github.com/kswope/session_countdown"
    gem.authors = ["Kevin Swope"]
    # gem is a Gem::Specification... see http://www.rubygems.org/read/chapter/20 for additional settings
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: gem install jeweler"
end

desc "build README.html from README.doc (for previewing in browser)"
task :readme do
  system "rdoc README.rdoc --one-file > README.html"
end

task :default => :test
task :test => [:test_rails2x, :test_rails3x]

task :test_rails2x do |t|
  chdir "test/rails2x_root" do
    system "rake"
  end
end

task :test_rails3x do |t|
  chdir "test/rails3x_root" do
    system "rake"
  end
end

