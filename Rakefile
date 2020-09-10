require 'yaml'

desc "Update _config.yml with env variables"
task :config_env do
  filename = '_config.yml'

  data = YAML.load_file filename

  data['jekyll_get_json'].each.with_index do |v, i|
    data['jekyll_get_json'][i]['json'].gsub!(/\$([a-zA-Z_]+[a-zA-Z0-9_]*)|\$\{(.+)\}/) { ENV[$1 || $2] }
  end

  File.open(filename, "w") { |file| file.write(data.to_yaml) }
end
