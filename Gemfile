source 'https://rubygems.org'
ruby '2.3.3'
gem 'rails', '5.0.1'

 # Rails defaults
gem 'sqlite3'
gem 'sass-rails', '~> 5.0'
gem 'uglifier', '>= 1.3.0'
gem 'coffee-rails', '~> 4.2'
gem 'jquery-rails'
gem 'turbolinks'
gem 'jbuilder', '~> 2.5'

 # learn-rails
gem 'activerecord-tableless'
gem 'compass-rails', '~> 2.0.alpha.0'
gem 'figaro'
gem 'gibbon'
gem 'google_drive'
gem 'high_voltage'
gem 'simple_form'
gem 'zurb-foundation'
group :development do
 gem 'better_errors'
 # gem 'quiet_assets' (not compatible with rails 5 atm)
 gem 'rails_layout'

 #wpp suggestion try

class Item
  # include ActiveModel::Validations
  # include ActiveModel::Conversion
  extend ActiveModel::Naming

  attr_accessor :name, :email, :content

  validates_presence_of :name
  validates_format_of :email, :with => /^[-a-z0-9_+\.]+\@([-a-z0-9]+\.)+[a-z0-9]{2,4}$/i
  validates_length_of :content, :maximum => 500

  class << self
    def all
      return []
    end
  end

  def initialize(attributes = {})
    attributes.each do |name, value|
      send("#{name}=", value)
    end
  end

  def persisted?
    false
  end
end

# wpp end sug

end