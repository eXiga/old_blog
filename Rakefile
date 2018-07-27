require 'rake'
require 'date'

def execute(command)
  system(command) or raise "** EXECUTION OF SHELL COMMAND IS FAILED **"
end

desc 'Start site on lolcalhost:4000'
task :start do
  execute "bundle exec jekyll serve"
end

desc 'Create post with given name'
task :post, [:post_name] do |task, args|
  current_date = Time.now.strftime("%Y-%m-%d")
  post_name = args[:post_name].strip.downcase.gsub(/ /, '-')
  file_name = "#{[current_date, post_name].join('-')}.markdown"
  
  execute "touch _posts/#{file_name}"
end