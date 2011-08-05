repo = "git@github.com:mikelewis/my_website.git"

desc 'Setup Cold'
task :cold do
  exec("ssh deployec2 'cd ~/ && git clone #{repo}'")
end

desc 'Deploy site to produciton'
task :deploy do
  exec("ssh deployec2 'cd ~/my_website && git pull origin master'")
end
