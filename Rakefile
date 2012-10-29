# encoding: utf-8

require 'rubygems'
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
	gem.name = "mjt-dojo"
	gem.homepage = "http://github.com/mtrense/mjt-dojo"
	gem.license = "MIT"
	gem.summary = %Q{TODO: one-line summary of your gem}
	gem.description = %Q{TODO: longer description of your gem}
	gem.email = "dev@trense.info"
	gem.authors = ["Max Trense"]
	gem.files = FileList[%W{dojo/**/* lib/**/*.rb spec/**/*_spec.rb README.* LICENSE.* }]
	gem.add_dependency 'mojito', '~> 0.3'
	gem.add_development_dependency "rspec", "~> 2.8.0"
	gem.add_development_dependency "rdoc", "~> 3.12"
	gem.add_development_dependency "bundler", "~> 1.0.0"
	gem.add_development_dependency "jeweler", "~> 1.8.4"
	gem.add_development_dependency "rcov", ">= 0"
end
Jeweler::RubygemsDotOrgTasks.new

require 'rspec/core'
require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new(:spec) do |spec|
	spec.pattern = FileList['spec/**/*_spec.rb']
end

RSpec::Core::RakeTask.new(:rcov) do |spec|
	spec.pattern = 'spec/**/*_spec.rb'
	spec.rcov = true
end

task :default => :spec

require 'rdoc/task'
Rake::RDocTask.new do |rdoc|
	version = File.exist?('VERSION') ? File.read('VERSION') : ""

	rdoc.rdoc_dir = 'rdoc'
	rdoc.title = "mjt-dojo #{version}"
	rdoc.rdoc_files.include('README*')
	rdoc.rdoc_files.include('lib/**/*.rb')
end
