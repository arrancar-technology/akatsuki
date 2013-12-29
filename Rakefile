require 'rake'

namespace :project do
  task :install do
    puts "======================================================"
    puts "Downloading submodules...please wait"
    puts "======================================================"
    sh('git submodule update --init --recursive')
    puts
    puts "======================================================"
    puts "Installation has been completed successfully..."
    puts "======================================================"
  end
  task :push do
    puts "======================================================"
    puts "Pushing project and submodules...please wait"
    puts "======================================================"
    ['presentation', 'presentation-functional', 'presentation-stubulator'].each { |project|
      sh %{cd #{project} && git push --all}
    }
    sh('git push --all')
    puts
    puts "======================================================"
    puts "Pushing has been completed successfully..."
    puts "======================================================"
  end
end
