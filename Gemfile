source "https://rubygems.org"

# The site is built and deployed by GitHub Actions (.github/workflows/pages.yml)
# rather than the legacy github-pages gem, so it can use current Jekyll and Ruby.
gem "jekyll", "~> 4.4"

group :jekyll_plugins do
  gem "jekyll-sitemap"
end

# Ruby 3.4+ (and 4.0) no longer ship these as default gems, but Jekyll and its
# dependencies still require them.
gem "csv"
gem "base64"
gem "bigdecimal"
gem "logger"
gem "webrick"
