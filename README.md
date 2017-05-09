# ansible-papertrail

An Ansible role for installing [Papertrail](https://papertrailapp.com).

## Role Variables

- `papertrail_version` - Release of [remote_syslog2](https://github.com/papertrail/remote_syslog2) to use
- `papertrail_conf` - Application logs configuration file (default: `/etc/log_files.yml`)
- `papertrail_files` - Files to send to papertrails (default `[]`). Should include path and tag properties.
- `papertrail_host` - Host for Papertrail's logging endpoint (default: `logs2.papertrail.com`)
- `papertrail_hostname` - Hostname used for events sent to Papertrail (default: `no`)
- `papertrail_newfile_interval` - Interval for checking for new files in file globs (default: `10`)
- `papertrail_port` - Port for Papertrail's logging endpoint (default: `45551`)
- `papertrail_preserve_fqdn` - Configure if rsyslog need to respect FQDN (default: `off`)
- `papertrail_rsyslog_enabled` - Configure if rsyslog should send to Papertrail (default: `true`)


## Usage

Ensure that `papertrail_host` and `papertrail_port` are set to the endpoints provided to your account by Papertrail. Both can be found in the user [account settings](https://papertrailapp.com/systems/setup).


## Example Playbook

See the [examples](./examples/) directory.
