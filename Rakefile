task default: :usage

desc 'Deploy'
task :deploy do
  source_path = './src'
  deploy_path = './dist'
  github_path = './docs'
  rm_rf "#{github_path}"
  cp_r "#{source_path}", "#{github_path}"
  %w[scss css].each { |dir| rm_rf "#{github_path}/#{dir}" }
  cp_r "#{deploy_path}/.", "#{github_path}"
end

desc 'Usage'
task :usage do
  puts `rake -T`
end
