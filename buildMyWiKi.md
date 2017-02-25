**一:工作环境**<br>
MacOS Sierra 10.12.3<br>
Homebrew 1.1.10<br>
ruby 2.0.0p648 (2015-12-16 revision 53162) [universal.x86_64-darwin16]<br>

**二：名称解释**<br>
Homebrew是Mac OSX上的软件包管理工具，能在Mac中方便的安装软件或者卸载软件，相当于linux下的apt-get、yum神器

RubyGems是一个方便而强大的Ruby程序包管理器（ package manager），类似RedHat的RPM.它将一个Ruby应用程序打包到一个gem里，作为一个安装单元。无需安装，最新的Ruby版本已经包含RubyGems了。

Bundler是管理Gem相依性的工具，执行bundle install是，会根据应用程式目标中Gemfile的设定，检查指定的Gem与相依套件是否已安装，如果已安裝了Gem，就会显示Using，如果是新下再安裝的Gem，就会显示Installing，想知道已安裝的Gem裝到哪，可以使用bundle show gemname來得知。

RVM

用于帮你安装Ruby环境，帮你管理多个Ruby环境，帮你管理你开发的每个Ruby应用使用机器上哪个Ruby环境。Ruby环境不仅仅是Ruby本身，还包括依赖的第三方Ruby插件。都由RVM管理。

Gem

Gem是封装起来的Ruby应用程序或代码库。
注：在终端使用的gem命令，是指通过RubyGems管理Gem包。

Rake
Rake是一门构建语言，和make类似。Rake是用Ruby写的，它支持自己的DSL用来处理和维护Ruby程序。 Rails用rake扩展来完成多种不容任务，如数据库初始化、更新等。

Bundle
相当于多个RubyGems批处理运行。在配置文件gemfilel里说明你的应用依赖哪些第三方包，他自动帮你下载安装多个包，并且会下载这些包依赖的包。 > Bundler maintains a consistent environment for ruby applications. It tracks an application’s code and the rubygems it needs to run, so that an application will always have the exact gems (and versions) that it needs to run.

**三：安装相关软件**<br>
homebrew安装
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

bundle 安装
gem install bundler

安装gollum
git clone https://github.com/gollum/gollum
cd gollum
bundle install
gollum --v  //查看是否success

创建自己的wiki系统
mkdir wiki
cd wiki
git init
gollum


**四：遇到的问题**<br>
1:软件版本不对<br>
solve:<br>
brew update<br>
brew reinstall icu4c

2:找不到安装路径 /usr/bin/opt<br>
solve:<br>
建立文件夹opt<br>
配置环境变量：<br>
vim ~/.bash_profile <br>export PATH="/usr/local/opt/icu4c/bin:$PATH"<br>
export PATH="/usr/local/opt/icu4c/sbin:$PATH"










