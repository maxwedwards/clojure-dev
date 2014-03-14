# Clojure-Dev

This package builds a working Clojure development environment from scratch on Ubuntu Linux
that can be used to build Clojure environments locally and for production apps.

Includes

+ Leiningen
+ Java 7

Building development enviroments should be easy. Install Vagrant and Ansible then you're good to go.

## Use

```
vagrant up

# Make a coffee...

vagrant ssh

# Write some Clojure

cd /vagrant

lein new myproject
cd myproject
lein test
```

If all goes well you should see a failing test ready for you to get to work

```
FAIL in (a-test) (core_test.clj:7)
FIXME, I fail.
expected: (= 0 1)
  actual: (not (= 0 1))

Ran 1 tests containing 1 assertions.
1 failures, 0 errors.
Tests failed.
```

## Running the playbook manually

Here we tell ansible to run the playbook against the vagrant user with the vagrant private key

```
ansible-playbook -i hosts clojure/setup.yml -u vagrant --private-key ~/.vagrant.d/insecure_private_key
```
