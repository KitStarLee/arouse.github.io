# 环境搭建
- 按照管理程序 brew install rbenv
- 设置shell 来加载 rbenv rbenv init
- 查询可用版本 rbenv install -l
- 安装版本 rbenv install 3.4.4
- 设置全局版本 rbenv global 3.4.4
- 重新加载 rbenv rehash
- 验证版本 rbenv versions
- 查看当前版本 ruby -v  ，如果不是 3.4.4，证明环境变量没有配置成功
- 查看 gem版本：gem -v
- 更新 Gem : gem update --system
- 检查 GCC/Make 版本：
  - gcc -v
  - g++ -v
  - make -v
- gem安装 jekyll 和Bundler
  - gem install jekyll bundler


# 项目搭建
- 克隆项目 git clone https://github.com/KitStarLee/arouse.github.io.git
- 进入项目目录 cd arouse.github.io
- 安装依赖 bundle install
  - 选定目录 bundle install --path vendor/bundle
- 安装 webrick : bundle add webrick
-  touch favicon.ico
- 更新依赖 bundle update
- 运行项目 bundle exec jekyll serve --livereload
- 重启命令 bundle exec jekyll clean && bundle exec jekyll serve --livereload