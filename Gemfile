source "https://rubygems.org"

# Hello! This is where you manage which Jekyll version is used to run.
# When you want to use a different version, change it below, save the
# file and run `bundle install`. Run Jekyll with `bundle exec`, like so:
#
#     bundle exec jekyll serve
#
# This will help ensure the proper Jekyll version is running.
# Happy Jekylling!
gem "jekyll", "~> 4.2.2"

## Jekyll Plugins ##
## Used to ensure we're getting the latest version of the different plugins ##
group :jekyll_plugins do 
  gem 'jekyll-feed', '~> 0.16.0'          # RSS/Atom Feeds
  gem 'jekyll-seo-tag', '~> 2.8'          # SEO stuff
  #gem 'jekyll-sitemap', '~> 1.4'          # Sitemap 
  gem 'jekyll-last-modified-at', '~> 1.3' # Last Modified
  gem 'jekyll-minifier', '~> 0.1.10'      # HTML Minifier
end

# Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
install_if -> { Gem.win_platform? } do
  gem "tzinfo", "~> 1.2"
  gem "tzinfo-data"
  gem "wdm", "~> 0.1.1"
end

# Lock `http_parser.rb` gem to `v0.6.x` on JRuby builds since newer versions of the gem
# do not have a Java counterpart.
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]
