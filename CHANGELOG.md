# Varnish Changelog

All notable changes to this project will be documented in this file.

## Unreleased

## 5.0.6 - *2023-02-27*

## 5.0.5 - *2023-02-27*

## 5.0.4 - *2023-02-23*

## 5.0.3 - *2023-02-23*

Standardise files with files in sous-chefs/repo-management

## 5.0.2 - *2023-02-15*

Standardise files with files in sous-chefs/repo-management

## 5.0.1 - *2022-12-13*

Standardise files with files in sous-chefs/repo-management

Standardise files with files in sous-chefs/repo-management

- Standardise files with files in sous-chefs/repo-management
- Remove delivery folder
- Update tested platforms

## 5.0.0 - *2021-10-14*

- Enable `unified_mode`
- Require Chef >= 15.5
- Remove chef-sugar dependency
- Fix support for RHEL 8
- Add new known Varnish releases
- Fix reload when using Varnish >= 7.0
- Use apt pinning on Debian/Ubuntu when using vendor packages
- Remove sysvinit support
- Deprecate various unused parameters in `varnish_config` resource
- Various cookstyle fixes
- Update test kitchen to standard modern platforms
- Switch to InSpec for integration testing

## 4.1.2 - *2021-08-30*

- Standardise files with files in sous-chefs/repo-management

## 4.1.1 - *2021-06-01*

- resolved cookstyle error: test/fixtures/cookbooks/disable_ipv6/metadata.rb:1:1 convention: `Style/Encoding`
- resolved cookstyle error: test/fixtures/cookbooks/disable_ipv6/recipes/default.rb:1:1 convention: `Style/Encoding`
- resolved cookstyle error: test/fixtures/cookbooks/disable_ipv6/recipes/disable_ipv6.rb:1:1 convention: `Style/Encoding`
- resolved cookstyle error: test/integration/distro/serverspec/default_spec.rb:1:1 convention: `Style/Encoding`
- resolved cookstyle error: test/integration/distro/serverspec/spec_helper.rb:1:1 convention: `Style/Encoding`
- resolved cookstyle error: test/integration/full_stack/serverspec/default_spec.rb:1:1 convention: `Style/Encoding`
- resolved cookstyle error: test/integration/full_stack/serverspec/spec_helper.rb:1:1 convention: `Style/Encoding`
- resolved cookstyle error: test/integration/varnish3/serverspec/default_spec.rb:1:1 convention: `Style/Encoding`
- resolved cookstyle error: test/integration/varnish3/serverspec/spec_helper.rb:1:1 convention: `Style/Encoding`
- resolved cookstyle error: test/integration/varnish4/serverspec/default_spec.rb:1:1 convention: `Style/Encoding`
- resolved cookstyle error: test/integration/varnish4/serverspec/spec_helper.rb:1:1 convention: `Style/Encoding`
- resolved cookstyle error: test/integration/varnish41/serverspec/default_spec.rb:1:1 convention: `Style/Encoding`
- resolved cookstyle error: test/integration/varnish41/serverspec/spec_helper.rb:1:1 convention: `Style/Encoding`
- resolved cookstyle error: test/integration/varnish5/serverspec/default_spec.rb:1:1 convention: `Style/Encoding`
- resolved cookstyle error: test/integration/varnish5/serverspec/spec_helper.rb:1:1 convention: `Style/Encoding`
- resolved cookstyle error: test/integration/varnish51/serverspec/default_spec.rb:1:1 convention: `Style/Encoding`
- resolved cookstyle error: test/integration/varnish51/serverspec/spec_helper.rb:1:1 convention: `Style/Encoding`
- resolved cookstyle error: test/integration/varnish52/serverspec/default_spec.rb:1:1 convention: `Style/Encoding`
- resolved cookstyle error: test/integration/varnish52/serverspec/spec_helper.rb:1:1 convention: `Style/Encoding`
- resolved cookstyle error: test/integration/varnish60/serverspec/default_spec.rb:1:1 convention: `Style/Encoding`
- resolved cookstyle error: test/integration/varnish60/serverspec/spec_helper.rb:1:1 convention: `Style/Encoding`
- resolved cookstyle error: test/integration/varnish61/serverspec/default_spec.rb:1:1 convention: `Style/Encoding`
- resolved cookstyle error: test/integration/varnish61/serverspec/spec_helper.rb:1:1 convention: `Style/Encoding`

## 4.1.0 - 2020-05-05

### Added

### Changed

- Updated the yum_repository resource to use the newer baseurl property instead of the legacy url property
- Migrated to actions
- resolved cookstyle error: resources/config.rb:6:1 refactor: `ChefStyle/TrueClassFalseClassResourceProperties`
- resolved cookstyle error: resources/log.rb:4:1 refactor: `ChefStyle/TrueClassFalseClassResourceProperties`
- resolved cookstyle error: resources/varnish_repo_debian.rb:7:1 refactor: `ChefStyle/TrueClassFalseClassResourceProperties`
- resolved cookstyle error: resources/varnish_repo_debian.rb:14:5 refactor: `ChefRedundantCode/AptRepositoryDistributionDefault`

### Deprecated

### Removed

## 4.0.2

- Test using CircleCI

## 4.0.1

- Adds support for Varnish 3 and 4.0 on CentOS 7
- Adds support for Varnish 4.0 and 4.1 on Ubuntu 1604

## 4.0.0

- Adds support Varnish 6.0
- Allow systemd platforms to set instance names. PR #157 and #153
  - Note: In some cases (instance_name is set when using systemd) this will change the varnish instance name.
- Escape ncsa_format_string for systemd. Fixes #137
- Don't set -n when instance_name is nil or empty on systemd

## 3.5.0

- Removed ChefSpec matchers as these are autogenerated by recent releases of ChefSpec in ChefDK
- Allow all platform families to set instance name in varnishlog
- Removed the unused build-essential dependency
- Require Chef 12.9 or later so we don't introduce issues with the apt cookbook
- Set the Varnish TTL
- Moved files and templates out of the default directories. This was a Chef 11-ism
- Renamed the resource files to let chef auto generate the resource names properly
- Removed the usage of kind_of in the resources since that's a LWRP-ism
- Swapped name_attribute for name_property in the resources
- Removed unnecessary default_action from the resources
- Removed the name properties from the resources since Chef auto generates these for us

## 3.4.0

- Adds support Varnish 5
- Updates reload-vcl file from upstream packaging
- Add varnish5 TravisCI tests

Known Bugs:

- Specifying `5.0` as the major version can cause an older version to be installed, use `5` instead. <https://github.com/sous-chefs/varnish/issues/150>

## 3.3.1

- Remove upper bound on yum cookbook dependency. #147
- Add repo_gpgcheck to redhat varnish repo. #145

## 3.3.0

- Updates to the new upstream varnish repo. <https://github.com/sous-chefs/varnish/issues/140>
- Deprecates using the upstream varnish 4 repo on CentOS 7 (distro version still works). <https://github.com/sous-chefs/varnish/issues/142>

## 3.2.0

- Links /etc/sysconfig/varnishlog and varnishncsa to defaults file in /etc/default. Fixes <https://github.com/sous-chefs/varnish/issues/125>.
- Fixes default varnishncsa format string (double quotes where getting added).
- Fixes an conflict when using both varnishlog and varnishncsa.
- Fixes distro_install integration tests. <https://github.com/sous-chefs/varnish/issues/126>
- Reverts the removal of reload-vcl since this is not fixed upstream in ubuntu's system packages yet.

## 3.1.0

- Varnish expects the varnish instance name to be `hostname` by default however this is sometimes different then `hostname -s` which is used by `ohai's hostname`. This seemed to only be an issue on CentOS 7.2.
- Use /etc/varnish/varnish.params for systemd init file. This is what the package uses and I think will remove some confusion about how settings are set. #103
- Remove /usr/share/varnish/reload-vcl on debian. This was added to support the '-j' option in varnish 4.1 however it has been fixed upstream.
- including yum-epel for centos
- Removing old testing files(CircleCi, kitchen-rackspace, rake) and replacing with (TravisCI, kitchen-dokken, delivery).
- adding integration testing in ci.

## 3.0.0

- Move recipes in default to custom resources / Move recipe and lwrp defaults config to custom resource
- Remove unused properties
- Don't append '.vcl' to file name
- Fix percent_of_total_mem function
- Include default recipe in integrations tests
- Add configure recipe
- Don't use default recipe to install/setup varnish
- Don't fetch the repository key over insecure HTTP

## 2.4.0

- Add additional attributes to allow use of template source from a wrapper cookbook
- Move define_systemd_daemon_reload to helpers (#97)
- Fix Chef::Exceptions::ChecksumMismatch error
- Set Ruby vers to 2.2.3 to satisfy ruby_dep requirements (#104)

## 2.3.0

- Fix chef 12.5 compatibility. This required a bunch of workarounds we should fix later.

## 2.2.2

- # 86 - Removed monkey patching of service providers

## 2.2.1

- Fix a bug in the monkey patched service resource, so that the changes needed for Varnish don't affect other services. #83.
- Update docs, Rakefile, standards. #79.
- Add additional examples to the documentation. #74.

## 2.2.0

- Fix default storage bug. Specify a default file storage location, as one is required with file backend, fixes #72\. Adjust template for default configuration of varnish so that it won't do the file backend without a path, since that's illegal syntax.

- Cause varnish reload to happen after restart. Delayed notifications are queued up in order. In this case, it makes sense for the reload to happen after the restart.

- Switch from service restart to service reload. The varnish_default_vcl has been updated to perform a service reload instead of a service restart. This will prevent the cache from being cleared when a reload of the vcl file is enough.

## 2.1.1

- Fixes #56\. The apt resource may not be included, so no need to run a notification on it.

## 1.2.0

- Make resource_name compatible with older Chef. Switch from passing an argument into resource_name to using the assignment operator '='. This will make resource_name compatible with older versions of Chef.

## 1.1.0 (2015-02-16)

- Created libraries, to eventually replace recipe functionality, currently can be used along side recipes
- Added CircleCI support for automated testing
- Added logrotate support
- Added varnish(log|nsca) support

## 0.9.12 (2014-03-12)

- [COOK-4368] - Improve documentation to include all attributes

## 0.9.10

### Bug

- **[COOK-3531](https://tickets.chef.io/browse/COOK-3531)** - Fix default instance name

## 0.9.8

### Improvement

- **[COOK-3095](https://tickets.chef.io/browse/COOK-3095)** - Add MiniTest Chef Handler and Test Kitchen

## 0.9.6

### Bug

- [COOK-2892]: Varnish restarts when vcl is updated instead of reloading

## 0.9.4

- [COOK-1261] - fix issues with default.vcl handling

## 0.9.0

- [COOK-873] - full daemon configuration through attributes
- [COOK-1091] - fix path for default.vcl, via COOK-873
- [COOK-1162] - add apt_repo recipe for using official varnish repository

## 0.8.0

- Current public release.
