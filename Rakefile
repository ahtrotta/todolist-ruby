require 'rake/testtask'
require 'find'

desc 'Say hello'
task :hello do
  puts "Hello there. This is the 'hello' task."
end

desc 'Run tests'
task :default => :test

Rake::TestTask.new(:test) do |t|
  t.libs << "test"
  t.libs << "lib"
  t.test_files = FileList['test/**/*_test.rb']
end

desc 'List project files'
task :list do
  files = []
  parent_dir = '/home/ahtrotta/Documents/launch-school/todolist_project/'

  Find.find(parent_dir) do |path|
    name = path.gsub(parent_dir, '')
    files << name if File.file?(path) && name[0] != '.' && name[-1] != '~'
  end

  puts files
end
