require 'rake'

desc "Table of Contents を挿入する"
task :toc, :file do |task, args|
  sh "./gh-md-toc --insert #{args[:file]} && rm -f #{args[:file]}.*.*"
end
