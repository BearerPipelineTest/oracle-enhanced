# frozen_string_literal: true

source "https://rubygems.org"

git_source(:github) do |repo_name|
  repo_name = "#{repo_name}/#{repo_name}" unless repo_name.include?("/")
  "https://github.com/#{repo_name}.git"
end

group :development do
  gem "rspec"
  gem "rdoc"
  gem "rake"

  gem "activerecord",   github: "rails/rails", branch: "master"
  gem "arel",   github: "yahonda/arel", branch: "follow_up_add_bind_for_oracle_visitor"
  gem "ruby-plsql", github: "rsim/ruby-plsql", branch: "master"

  platforms :ruby do
    gem "ruby-oci8",    github: "kubo/ruby-oci8"
    gem "byebug"
  end

  platforms :jruby do
    gem "pry"
    gem "pry-nav"
  end
end

group :test do
  gem "simplecov",  github: "colszowka/simplecov", branch: "master", require: false
end
