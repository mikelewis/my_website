remote_path = "/usr/local/nginx/html"
repo = "git@github.com:mikelewis/my_website.git"

desc 'Setup Cold'
task :cold => :environment do
  exec("ssh -x ec2 'cd #{remote_path} && git clone #{repo}'")
end

desc 'Deploy site to produciton'
task :deploy => :environment do
  exec("ssh -x ec2 'cd #{remote_path} && git pull origin master'")
end
