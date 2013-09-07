# Active Record

This deck will train you on the ORM built into Ruby on Rails, Active Record.

### What is the difference between `count`, `length, and `size`?

In Ruby, `length` and `size` are symonyms. They do the same thing—tell you how many elements are in an array or hash.

In Rails, `count` runs a SQL COUNT to find how many records exist for a given model. It is also a method that takes querying parameters:

	# clients with their age present in the database
	Client.count(:age)