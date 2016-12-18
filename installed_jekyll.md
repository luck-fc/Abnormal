# Abnormal
Problems encountered in the installation of Jekyll

[installed_jekyll.md](https://github.com/luck-fc/Abnormal/blob/master/installed_jekyll.md)

1.https://www.ruby-lang.org/en/documentation/installation/  download RubyInstaller x.x.x
   windows https://rubyinstaller.org/ 
   
2.gem install jekyll

(1) SSL_connect returned=1 errno=0 state=SSLv3 read server certificate B: certificate verify failed

(2) ERROR:  Could not find a valid gem 'jekyll' (>= 0) in any repository
	ERROR:  Possible alternatives: jekyll` 
	
Solve the problem:

$ gem sources --remove http://rubygems.org/
$ gem sources -a http://gems.ruby-china.org/  （RubyGems 镜像- Ruby China）
$ gem sources -l
*** CURRENT SOURCES ***
http://gems.ruby-china.org/ 
$ gem install jekyll

ok

Very nice

