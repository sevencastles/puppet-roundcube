#roundcube

##Overview

Puppet module to install and manage Roundcube, the web-base email client.

##Usage

To install Roundcube with all defaults simply use.

```
class { 'roundcube': ]
```

Specify a certain mail server

```
class { 'roundcube':
  imap_host => 'ssl://localhost',
  imap_port => 993,
}
```

Specify the database to be used to store the Roundcube state

```
class { 'roundcube':
  db_type     => 'postgresql',
  db_name     => 'roundcube',
  db_host     => 'localhost',
  db_username => 'roundcube',
  db_password => 'secret',
}
```

Specify a couple of plugins to activate

```
class { 'roundcube':
  plugins => [
    'emoticons',
    'markasjunk2',
    'password',
  ],
}
```

##Limitations

The module has been tested on the following operating systems. Testing and patches for other platforms are welcome.

* Debian Linux 6.0 (Squeeze)

[![Build Status](https://travis-ci.org/tohuwabohu/puppet-roundcube.png?branch=master)](https://travis-ci.org/tohuwabohu/puppet-roundcube)

##Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request