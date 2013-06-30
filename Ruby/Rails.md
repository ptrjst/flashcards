# Ruby on Rails

### What are the default directories for testing?

1. `test/fixtures` - text/sample data in YAML or ERB used to populate the test database

2. `test/functional` - test for your controllers

3. `integration` - test where two → infinite controllers interact

4. `unit` - test for your models

### What's the command for restarting a Rails app using Passenger?

Create a file called `restart.txt` in the `tmp` folder of your Rails application. From inside the root of your Rails app:

`touch tmp/restart.txt`