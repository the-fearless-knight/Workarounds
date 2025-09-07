# error: 
```
evil-winrm 
/usr/share/evil-winrm/vendor/bundle/ruby/3.4.0/gems/logging-2.4.0/lib/logging.rb:10: warning: syslog was loaded from the standard library, but is not part of the default gems starting from Ruby 3.4.0.
You can add syslog to your Gemfile or gemspec to silence this warning.
/usr/share/evil-winrm/vendor/bundle/ruby/3.4.0/gems/winrm-2.3.9/lib/winrm/psrp/fragment.rb:35: warning: redefining 'object_id' may cause serious problems
/usr/share/evil-winrm/vendor/bundle/ruby/3.4.0/gems/winrm-2.3.9/lib/winrm/psrp/message_fragmenter.rb:29: warning: redefining 'object_id' may cause serious problems
/usr/share/evil-winrm/vendor/bundle/ruby/3.4.0/gems/winrm-fs-1.3.5/lib/winrm-fs/core/file_transporter.rb:20: warning: benchmark was loaded from the standard library, but will no longer be part of the default gems starting from Ruby 3.5.0.
You can add benchmark to your Gemfile or gemspec to silence this warning.
/usr/share/evil-winrm/vendor/bundle/ruby/3.4.0/gems/winrm-fs-1.3.5/lib/winrm-fs/core/file_transporter.rb:21: warning: csv was loaded from the standard library, but is not part of the default gems starting from Ruby 3.4.0.
You can add csv to your Gemfile or gemspec to silence this warning.
bundler: failed to load command: /usr/share/evil-winrm/evil-winrm.rb (/usr/share/evil-winrm/evil-winrm.rb)
/usr/lib/ruby/3.4.0/bundled_gems.rb:82:in 'Kernel.require': cannot load such file -- csv (LoadError)
	from /usr/lib/ruby/3.4.0/bundled_gems.rb:82:in 'block (2 levels) in Kernel#replace_require'
	from /usr/share/evil-winrm/vendor/bundle/ruby/3.4.0/gems/winrm-fs-1.3.5/lib/winrm-fs/core/file_transporter.rb:21:in '<top (required)>'
	from /usr/share/evil-winrm/vendor/bundle/ruby/3.4.0/gems/winrm-fs-1.3.5/lib/winrm-fs/file_manager.rb:20:in 'Kernel#require_relative'
	from /usr/share/evil-winrm/vendor/bundle/ruby/3.4.0/gems/winrm-fs-1.3.5/lib/winrm-fs/file_manager.rb:20:in '<top (required)>'
	from /usr/share/evil-winrm/vendor/bundle/ruby/3.4.0/gems/winrm-fs-1.3.5/lib/winrm-fs.rb:22:in 'Kernel#require_relative'
	from /usr/share/evil-winrm/vendor/bundle/ruby/3.4.0/gems/winrm-fs-1.3.5/lib/winrm-fs.rb:22:in '<top (required)>'
	from /usr/lib/ruby/3.4.0/bundled_gems.rb:82:in 'Kernel.require'
	from /usr/lib/ruby/3.4.0/bundled_gems.rb:82:in 'block (2 levels) in Kernel#replace_require'
	from /usr/share/evil-winrm/evil-winrm.rb:11:in '<top (required)>'
	from /usr/lib/ruby/3.4.0/bundler/cli/exec.rb:59:in 'Kernel.load'
	from /usr/lib/ruby/3.4.0/bundler/cli/exec.rb:59:in 'Bundler::CLI::Exec#kernel_load'
	from /usr/lib/ruby/3.4.0/bundler/cli/exec.rb:23:in 'Bundler::CLI::Exec#run'
	from /usr/lib/ruby/3.4.0/bundler/cli.rb:451:in 'Bundler::CLI#exec'
	from /usr/lib/ruby/3.4.0/bundler/vendor/thor/lib/thor/command.rb:28:in 'Bundler::Thor::Command#run'
	from /usr/lib/ruby/3.4.0/bundler/vendor/thor/lib/thor/invocation.rb:127:in 'Bundler::Thor::Invocation#invoke_command'
	from /usr/lib/ruby/3.4.0/bundler/vendor/thor/lib/thor.rb:538:in 'Bundler::Thor.dispatch'
	from /usr/lib/ruby/3.4.0/bundler/cli.rb:35:in 'Bundler::CLI.dispatch'
	from /usr/lib/ruby/3.4.0/bundler/vendor/thor/lib/thor/base.rb:584:in 'Bundler::Thor::Base::ClassMethods#start'
	from /usr/lib/ruby/3.4.0/bundler/cli.rb:29:in 'Bundler::CLI.start'
	from /usr/lib/ruby/gems/3.4.0/gems/bundler-2.7.1/exe/bundle:28:in 'block in <top (required)>'
	from /usr/lib/ruby/3.4.0/bundler/friendly_errors.rb:118:in 'Bundler.with_friendly_errors'
	from /usr/lib/ruby/gems/3.4.0/gems/bundler-2.7.1/exe/bundle:20:in '<top (required)>'
	from /sbin/bundle:25:in 'Kernel#load'
	from /sbin/bundle:25:in '<main>'
```

# fix: 
```
cd /usr/share/evil-winrm && sudo bundle add csv benchmark syslog
```
