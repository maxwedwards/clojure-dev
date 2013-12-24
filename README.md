# Clojure-Dev

This package builds a working Clojure development environment from scratch on Unbuntu Linux

Includes

+ Leiningen
+ Java 7
+ Emacs

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
