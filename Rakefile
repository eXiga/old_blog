require 'rake'

def execute(command)
  system(command) or raise "** EXECUTION OF SHELL COMMAND IS FAILED **"
end

desc 'Start site on lolcalhost:4000'
task :start do
  execute "bundle exec jekyll serve"
end