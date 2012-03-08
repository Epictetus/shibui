require './lib/shibui'

namespace :gem do

  desc "Build the gem"
  task :build do
    system "gem build *.gemspec"
  end
 
  desc "Build and release the gem"
  task :release => :build do
    system "gem push shibui-#{Shibui::VERSION}.gem"
  end
  
end