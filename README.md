No Brainer
===========

No Brainer is a Ruby ORM for [RethinkDB](http://www.rethinkdb.com/).

Installation
-------------

```ruby
gem 'nobrainer'
```

Features
---------

* creation of database and tables on demand
* find/create
* attributes accessors
* create, update, save callbacks

Usage
------

```ruby
NoBrainer.connect "rethinkdb://host:port/database"

class Model < NoBrainer::Base
  field :field1
  field :field2
  field :field3
end

doc = Model.create(:field1 => 'hello')
doc = Model.find(doc.id)

doc.field1 = 'ohai'
doc.save
```

License
--------

MIT License