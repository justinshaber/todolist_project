require 'rake/testtask'
require 'find'
require 'bundler/gem_tasks'

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

# desc 'List Files'
# task :list_files do
#   files = []
#   Find.find('/Users/justinshaber/coding_projects/todolist_project') do |path|
#     next if FileTest.directory?(path)
#     files << path.split('/').last unless path.include?('/.')
#   end
#   puts files
# end

desc 'List Files'
task :list_files do
  Find.find('.') do |name|
    next if name.include?('/.') # Excludes files and directories with . names
    puts name if File.file?(name)
  end
end