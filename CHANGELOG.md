## Version 20150715

Upgrading to this version is strongly recommended because of the OpenSSL upgrade, which fixes some security vulnerabilities!

 * Upgraded to OpenSSL 1.0.2d.

## Version 20150517

 * The Ruby versions that we now support are: 2.1.6 and 2.2.2.
 * Added additional native extensions: puma, unicorn, kgio, raindrops, fast-stemmer, hitimes, redcarpet, snappy, curses.
 * Upgraded bundler gem to version 1.9.9.
 * Upgraded mysql2 gem to version 0.3.11.
 * Upgraded pg gem to version 0.18.2.
 * Upgraded bundler gem to version 1.9.9.
 * The sqlite3, pg, rugged and charlock_holmes gems are now smaller because they are now compiled with better compiler optimizations. The total reduction of all these gems together is 4 MB uncompressed.

## Version 20150210

 * Added support for Ruby 2.2.0. Version 2.1.5 and 2.2.0 are supported in parallel for the time being.
 * Added support for creating Windows packages. But there are currently a number of caveats:
   - Traveling Ruby supports creating packages *for* Windows, but it does not yet support creating packages *on* Windows. That is, the Traveling Ruby tutorials and the documentation do not work when you are a Ruby developer on Windows. To create Windows packages, you must use OS X or Linux.

     This is because in our documentation we make heavy use of standard Unix tools. Tools which are not available on Windows. In the future we may replace the use of such tools with Ruby tools so that the documentation works on Windows too.
   - Only Ruby 2.1.5 is supported for Windows, not 2.2.0. This is because [the RubyInstaller project](http://rubyinstaller.org/) hasn't released Ruby 2.2.0 binaries yet.
 * Fixed a problem with the 'rugged' native extension on Linux. Closes GH-33.
 * Fixed a problem with the 'charlock_holmes' native extension on Linux. Closes GH-34.
 * Header files are no longer packaged. This saves 256 KB.
 * RDoc and various unnecessary Bundler files have been removed. This saves about 1.2 MB.
 * Upgraded Bundler to 1.7.12.

## Version 20150204

 * Added additonal native extension versions:
   - bcrypt 3.1.10
   - eventmachine 1.0.6
   - json 1.8.2
   - mini_portile 0.6.2
   - nokogiri 1.6.6.2
   - sqlite3 1.3.10
   - nokogumbo 1.2.0
   - rugged 0.22.0b5

## Version 20150130

Upgrading to this version is strongly recommended because of the OpenSSL upgrade, which fixes some security vulnerabilities!

 * Added the following native extension gems: RedCloth, escape_utils, posix-spawn, nokogumbo, github-markdown, rugged, charlock_holmes, unf_ext.
 * Upgraded to OpenSSL 1.0.1l.
 * The Linux version and the OS X version now use the same CA root certificates. Closes GH-24.

## Version 20141224

 * Fixed the mysql2 native extension not working on Linux. This is done by dynamically linking against libstdc++. Closes GH-21.
 * Added the eventmachine and thin native extension gems.

## Version 20141219

 * Removed header files. This makes the package 100 KB smaller.
 * Removed the sdbm extension because almost nobody uses it. The sqlite3 gem is almost always a better choice anyway.
 * Added the yajl-ruby native extension gem.

## Version 20141215

 * The Linux packages now include libffi.so.6, which was forgotten in the previous release. Closes GH-16.

## Version 20141213

 * Further removed unnecessary files. The Ruby binary packages were about 10 MB before. They are now about 6 MB.
 * Supports native extensions.

## Version 20141209

 * Fixed inclusion of Bundler.

## Version 20141206

 * Initial release.
