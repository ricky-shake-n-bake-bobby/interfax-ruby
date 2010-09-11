require 'rubygems'
require 'rake'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = "interfax"
    gem.summary = %Q{A ruby wrapper for the interfax webservice (SOAP)}
    gem.description = %Q{A ruby wrapper for the interfax webservice (SOAP)}
    gem.email = "sascha.brink@gmail.com"
    gem.homepage = "http://github.com/sbrink/interfax"
    gem.authors = ["Sascha Brink"]
    gem.add_development_dependency "rspec", ">= 1.2.9"
    gem.files =  FileList["[A-Z]*", "{lib,spec}/**/*"] - FileList["**/*.log"]
    # gem is a Gem::Specification... see http://www.rubygems.org/read/chapter/20 for additional settings
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: gem install jeweler"
end

#require 'spec/rake/spectask'
#Spec::Rake::SpecTask.new(:spec) do |spec|
#  spec.libs << 'lib' << 'spec'
#  spec.spec_files = FileList['spec/**/*_spec.rb']
#end

#Spec::Rake::SpecTask.new(:rcov) do |spec|
#  spec.libs << 'lib' << 'spec'
#  spec.pattern = 'spec/**/*_spec.rb'
#  spec.rcov = true
#end

task :spec => :check_dependencies

task :default => :spec

require 'rake/rdoctask'
Rake::RDocTask.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "interfax #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
