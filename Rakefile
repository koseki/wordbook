require 'fileutils'

DIR = File.dirname(__FILE__)
REPOS = 'https://github.com/koseki/wordbook'
GIT = 'git'

TYPES = %w{talks books}

task :default do
  TYPES.each do |type|
    FileUtils.mkdir_p(File.join(DIR, 'gh-pages/ja/en', type))
  end
end

desc 'initialize gh-pages directory'
task :ghpages do
  break if File.exist?(File.join(DIR, 'gh-pages'))
  %x{#{ GIT } clone -b gh-pages #{ REPOS } gh-pages}
end
