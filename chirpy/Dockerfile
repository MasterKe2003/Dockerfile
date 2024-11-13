# 使用官方 Ruby 镜像作为基础镜像
FROM ruby:3.1

# 设置工作目录
WORKDIR /app

# 配置 RubyGems 镜像源
RUN gem sources --add https://mirrors.aliyun.com/rubygems/ --remove https://rubygems.org/

# 安装 Jekyll 和 Bundler
RUN gem install jekyll bundler

# 复制 Gemfile 和 Gemfile.lock
COPY Gemfile* ./

# 安装项目依赖
RUN bundle install

# 配置容器启动时运行 Jekyll 服务器
CMD ["jekyll", "serve", "--host", "0.0.0.0"]