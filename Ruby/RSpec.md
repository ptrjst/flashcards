# RSpec

### Who created RSpec?

RSpec was created by Steven Baker in 2005.

### What do you use RSpec for?

The RSpec Book:

> "We use RSpec to write executable examples of the expected behavior of a small bit of code in a controlled context."

### What does the `it()` method create?

The `it()` method creates an *example* of how the code should operate -- the behavior.

### How do you run the specs for only one specific file?

From the command line, run:

`spec specs/example_spec.rb`

### What is the core pattern for specs?

    describe MovieList do
      context "when first created" do
        it "is empty" do
          movie_list = MovieList.new
          movie_list.should be_empty
        end
      end
    end
    
The `it()` method creates an *example* of the behavior of a `MovieList`, with the *context* being that the `MovieList` was just created.

### What is given/when/then?

In Behavior-Driven Development, everyone has to describe scenarios using specific language: *Given* some context, *when* some event occurs, *Then* I expect some outcome. This is known as the "BDD triad".

### What is red/green/factor?

In Test-Driven Development, you develop using the red/green/refactor cycle.

1. Write a small test for code that doesn't exist yet. What that test *fail*.

2. Write enough code to watch your test *pass*.

3. Observe resulting design. *Refactor* any duplication you see.

## Resources

http://tutorials.jumpstartlab.com/topics/internal_testing/rspec_and_bdd.html