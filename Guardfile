# guard options are too long for the rspec line, so set them here
guard_options = {
  cli: "--color --format=doc",
  all_after_pass: false,
  all_on_start: false,
  keep_failed: false,
}

guard 'rspec', guard_options do
  watch(%r{^spec/.+_spec\.rb$}) {|m| m}
  watch(%r{^lib/(.+)\.rb$})     { |m| "spec/#{m[1]}_spec.rb" }
  watch('spec/spec_helper.rb')  { "spec" }
end
