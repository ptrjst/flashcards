# Unix on a Mac

This deck is all about the Terminal on OS X.

### What is the difference between `.bash_profile` and `.bashrc`?

According to the [bash man page](http://linux.die.net/man/1/bash):

> ~/.bash_profile  
> The personal initialization file, executed for login shells
>
> ~/.bashrc  
> The individual per-interactive-shell startup file

Further reading: [.bash_profile vs .bashrc by Josh Staiger](http://www.joshstaiger.org/archives/2005/07/bash_profile_vs.html)

### What is the `.bash_prompt` file?

This isn't actually a thing. It's just the convention for some users to put their custom prompt-related settings, like colors or showing the current directory and SCM information. You still have to source this `.bash_prompt` file from `.bash_profile`.

### Kill all processes by name with grep

	kill $(ps aux | grep zeus | awk '{print $2}')

[Source](http://stackoverflow.com/questions/3510673/find-and-kill-a-process-in-one-line-using-bash-and-regex)

## Resources

[The Art of Unix Programming by Eric S. Raymond](http://www.faqs.org/docs/artu/)

