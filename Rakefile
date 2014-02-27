require 'rubygems'
require 'rake'
require 'fileutils'
require 'optparse'
require 'yaml'

task :np do
  OptionParser.new.parse!
  ARGV.shift
  title = ARGV.join(' ')

  path = "_posts/#{Date.today}-#{title.downcase.gsub(/[^[:alnum:]]+/, '-')}.markdown"
  
  if File.exist?(path)
  	puts "[WARN] File exists - skipping create"
  else
    File.open(path, "w") do |file|
      file.puts YAML.dump({'layout' => 'post', 'published' => false, 'title' => title})
      file.puts "---"
    end
  end
  `gedit #{path}`

  exit 1
end

###search and edit###
task :se do
  throw "WTF did you modify?" unless ARGV[1]
  search = ""
  ARGV[1..ARGV.length - 1].each { |v| search += " #{v}" }
  search.strip!
  sh "find _posts -iregex .*#{search}.* | xargs gedit &"
  exit
end


desc "Startup Jekyll"
task :start do
  sh "jekyll serve --watch"
end

task :default => :start

