source 'https://rubygems.org'
git_source(:github) { |repo| "https://github.com/#{repo}.git" }

ruby '2.7.6'

# Bundle edge Rails instead: gem "rails", github: "rails/rails", branch: "main"
gem 'rails', '~> 7.0.3', '>= 7.0.3.1'

# The modern asset pipeline for Rails [https://github.com/rails/propshaft]
gem 'propshaft'

# Use postgresql as the database for Active Record
gem 'pg', '~> 1.4'

# Use the Puma web server [https://github.com/puma/puma]
gem 'puma', '~> 5.6'

# Use JavaScript with ESM import maps [https://github.com/rails/importmap-rails]
gem 'importmap-rails'

# Hotwire's SPA-like page accelerator [https://turbo.hotwired.dev]
gem 'turbo-rails'

# Hotwire's modest JavaScript framework [https://stimulus.hotwired.dev]
gem 'stimulus-rails'

# Build JSON APIs with ease [https://github.com/rails/jbuilder]
# gem "jbuilder"

# Use Redis adapter to run Action Cable in production
gem 'redis', '~> 4.7'

# Use Kredis to get higher-level data types in Redis [https://github.com/rails/kredis]
# gem "kredis"

# Use Active Model has_secure_password [https://guides.rubyonrails.org/active_model_basics.html#securepassword]
# gem "bcrypt", "~> 3.1.7"

# Windows does not include zoneinfo files, so bundle the tzinfo-data gem
gem 'tzinfo-data', platforms: %i[mingw mswin x64_mingw jruby]

# Reduces boot times through caching; required in config/boot.rb
gem 'bootsnap', require: false

# Use Active Storage variants [https://guides.rubyonrails.org/active_storage_overview.html#transforming-images]
gem 'image_processing'

group :development, :test do
  # See https://guides.rubyonrails.org/debugging_rails_applications.html#debugging-with-the-debug-gem
  gem 'debug', platforms: %i[mri mingw x64_mingw]
end

group :development do
  # Use console on exceptions pages [https://github.com/rails/web-console]
  gem 'web-console'

  # Add speed badges [https://github.com/MiniProfiler/rack-mini-profiler]
  gem 'rack-mini-profiler'

  # Speed up commands on slow machines / big apps [https://github.com/rails/spring]
  # gem "spring"
end

group :test do
  # Use system testing [https://guides.rubyonrails.org/testing.html#system-testing]
  gem 'capybara'
  gem 'selenium-webdriver'
  gem 'webdrivers', require: ENV['driverless'] != 'true' # allow using system drivers
end

# ---- end rails 7 default gems (rails new railsnew7 -d postgresql -a propshaft)
# Generally we're importmaps, esbuild, dartass, propshaft

# Foreman for running procfiles
# `foreman start -f Procfile.dev` for the development procfile
gem 'foreman'

# Scheduling tools
gem 'shoryuken'
gem 'sidekiq'

# AWS tools
gem 'aws-sdk-chime'
gem 'aws-sdk-ecs'
gem 'aws-sdk-elastictranscoder'
gem 'aws-sdk-s3'
gem 'aws-sdk-sqs'
gem 'aws-sdk-transcribeservice'
gem 'aws-sigv4'

# Web/HTML tools
gem 'dartsass-rails'
gem 'slim-rails'
gem 'view_component'
# Pagination
gem 'pagy'
# UserAgent Parser
gem 'user_agent_parser'
# Slug support
gem 'friendly_id'
# Generate fake data
gem 'faker'

# Calendar tools
gem 'icalendar'

# Authorization
gem 'devise'
gem 'devise_invitable' # for inviting users
gem 'devise_saml_authenticatable'
gem 'devise-two-factor'
gem 'omniauth'
gem 'omniauth-google-oauth2'
gem 'omniauth-oauth2'
gem 'omniauth-rails_csrf_protection'
gem 'rqrcode' # for devise-two-factor qr code generation

# API Auth
gem 'jwt'

# Chopping block
gem 'discard' # REMOVEME after v1 depro
gem 'draper' # REMOVEME decorators then remove this gem
gem 'net-http' # REMOVEME - required to silence warning: https://github.com/ruby/net-protocol/issues/10
gem 'pundit' # REMOVEME after v1 depro

group :production, :staging, :review do
  # Monitoring tools
  gem 'appsignal'
  gem 'skylight'
end

group :development do
  gem 'rufo'
  gem 'solargraph' # ruby languge server for editor integration (VSCode/Sublime etc)
end

group :development, :review do
  gem 'letter_opener_web'
end

group :development, :test do
  gem 'rspec-rails'
  gem 'shoulda-matchers'

  # === Ruby static code analyzer and formatter
  gem 'rubocop', '~> 1.31', require: false
  gem 'rubocop-performance'
  gem 'rubocop-rails', require: false
  gem 'rubocop-rspec'
  gem 'rubocop-thread_safety'

  gem 'slim_lint'

  gem 'annotate'

  gem 'coveralls_reborn', require: false
end

group :test do
  gem 'factory_bot_rails'
  gem 'rails-controller-testing'
  # CI test reporting
  gem 'rspec_junit_formatter'

  gem 'timecop'

  gem 'vcr'
  gem 'webmock'
end

group :heroku do
  gem 'sprockets' # REMOVEME: also remove app/assets/config/.manifest.js
end
