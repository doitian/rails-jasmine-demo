# A sample Guardfile
# More info at https://github.com/guard/guard#readme

require 'guard/jasmine'
port = ::Guard::Jasmine.find_free_server_port
guard :jasmine, :server => :jasmine_gem, :port => port, :jasmine_url => "http://localhost:#{port}/" do
  watch(%r{spec/javascripts/support/.+\.(?:rb|yml)$}) { 'spec/javascripts' }
  watch(%r{spec/javascripts/helpers/.+\.rb$}) { 'spec/javascripts' }
  watch(%r{spec/javascripts/spec\.(?:js\.coffee|js|coffee)$}) { 'spec/javascripts' }
  watch(%r{spec/javascripts/.+_spec\.(?:js\.coffee|js|coffee)$})
  watch(%r{app/assets/javascripts/(.+?)\.(js\.coffee|js|coffee)(?:\.\w+)*$}) { |m| "spec/javascripts/#{ m[1] }_spec.#{ m[2] }" }
end
