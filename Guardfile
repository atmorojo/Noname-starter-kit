# A sample Guardfile
# More info at https://github.com/guard/guard#readme

guard 'coffeescript', :input => 'public/js'

# Guard::Compass
#
# You don't need to configure watchers for guard 'compass' declaration as they generated
# from your Compass configuration file. You might need to define the Compass working directory
# and point to the configuration file depending of your project structure.
#
# Available options:
#
# * working_directory: Define the Compass working directory, relative to the Guardfile directory
# * configuration_file: Path to the Compass configuration file, relative to :project_path
#
# Like usual, the Compass configuration path are relative to the :project_path

# guard 'compass', project_path: 'not_current_dir', configuration_file: 'path/to/my/compass_config.rb'
guard :compass

# This will concatenate the javascript files specified in :files to public/js/all.js
guard :concat, type: "js", files: %w(), input_dir: "public/js", output: "public/js/all"

# guard :concat, type: "css", files: %w(), input_dir: "public/css", output: "public/css/all"

guard 'livereload' do
  watch(%r{app/views/.+\.(erb|haml|slim)$})
  watch(%r{app/helpers/.+\.rb})
  watch(%r{public/.+\.(css|js|html)})
  watch(%r{config/locales/.+\.yml})
  # Rails Assets Pipeline
  watch(%r{(app|vendor)(/assets/\w+/(.+\.(css|js|html|png|jpg))).*}) { |m| "/assets/#{m[3]}" }
end

# guard 'uglify', :destination_file => "public/javascripts/application.js" do
#   watch (%r{app/assets/javascripts/application.js})
# end
