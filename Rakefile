require 'rake'

targets = []
Dir.glob('./chapter*.md').each do |file|
  target = File.basename(file)
  targets << target
end

desc '全ての Chapter マークダウンに Table of Contents を挿入する'
task toc: 'toc:all'

namespace :toc do
  task :all => targets
  task :default => :all

  targets.each do |target|
    desc "#{target} に Table of Contents を挿入する"
    task target.to_sym do
      sh "./gh-md-toc --insert #{target} && rm -f #{target}.*.*"
    end
  end
end
