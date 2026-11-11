source "https://rubygems.org"

# For local preview only. GitHub Pages builds the live site with its own
# gem versions and ignores this file.
#
#     bundle install
#     bundle exec jekyll serve
#
gem "jekyll", "~> 4.3"

group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.17"
  gem "jekyll-sitemap", "~> 1.4"
end

# Ruby 3 no longer ships webrick, which `jekyll serve` needs.
gem "webrick", "~> 1.8"

# Windows does not include zoneinfo files.
gem "tzinfo", ">= 1", "< 3", platforms: [:windows, :jruby]
gem "tzinfo-data", platforms: [:windows, :jruby]
