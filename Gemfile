source "http://rubygems.org"

# Specify your gem's dependencies in oauth-plugin.gemspec
gemspec

require 'rbconfig'

group :development do
  gem 'opentransact', git: 'https://github.com/onemedical/opentransact-ruby.git', ref: '0f66b3889f5f6c0c9ea8fbf2d8fe26692cff0783'
end

platforms :ruby do
  if RbConfig::CONFIG['target_os'] =~ /darwin/i
    gem 'rb-fsevent'
    gem 'growl'
  end
  if RbConfig::CONFIG['target_os'] =~ /linux/i
    gem 'rb-inotify', '>= 0.5.1'
    gem 'libnotify',  '~> 0.1.3'
  end
end

platforms :jruby do
  if RbConfig::CONFIG['target_os'] =~ /darwin/i
    gem 'growl'
  end
  if RbConfig::CONFIG['target_os'] =~ /linux/i
    gem 'rb-inotify', '>= 0.5.1'
    gem 'libnotify',  '~> 0.1.3'
  end
end
