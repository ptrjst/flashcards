# Ruby Time, DateTime, etc.

### What is `Time`?

- Implemented in C (POSIX)
- Limited Date Range
- Large API

### What is `DateTime`?

- Implemented in Ruby
- Large Date Range
- Small API

### What is better -- `Time` or `DateTime`?

`Time`

### Does `DateTime` support time zones?

No. DateTime doesn't support time zones—it supports offsets from UTC.

### What is timezone mapping?

It's a fancy thing `DateTime` does, such as mapping:

	"Central Time (US & Canada)" => "America/Chicago"
	
### How do you get system time with `Date`?
	
	Date.today

### How do you get user time with `Date`?

	Date.current

### What's the difference between `Date.today` and `Date.current`?

Do not use (system time):

	Date.today
	
You probably want (user time):

	Date.current

