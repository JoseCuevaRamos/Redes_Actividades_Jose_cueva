# Expansion
Each time we type a command line and press the enter key, bash performs several processes upon the text before it carries out our command. We have seen a couple of cases of how a simple character sequence, for example “*”, can have a lot of meaning to the shell. The process that makes this happen is called expansion. With expansion, we type something and it is expanded into something else before the shell acts upon it. To demonstrate what we mean by this, let's take a look at the echo command. echo is a shell builtin that performs a very simple task. It prints out its text arguments on standard output:

That's pretty straightforward. Any argument passed to echo gets displayed. Let's try another example:
# Pathname Expansion
The mechanism by which wildcards work is called pathname expansion. If we try some of the techniques that we employed in our earlier lessons, we will see that they are really expansions. Given a home directory that looks like this:
# Tilde Expansion
As we recall from our introduction to the cd command, the tilde character (“~”) has a special meaning. When used at the beginning of a word, it expands into the name of the home directory of the named user, or if no user is named, the home directory of the current user:
# Arithmetic Expansion
The shell allows arithmetic to be performed by expansion. This allow us to use the shell prompt as a calculator:
# Brace Expansion
Perhaps the strangest expansion is called brace expansion. With it, we can create multiple text strings from a pattern containing braces. Here's an example:
# Parameter Expansion
We're only going to touch briefly on parameter expansion in this lesson, but we'll be covering it more later. It's a feature that is more useful in shell scripts than directly on the command line. Many of its capabilities have to do with the system's ability to store small chunks of data and to give each chunk a name. Many such chunks, more properly called variables, are available for our examination. For example, the variable named “USER” contains our user name. To invoke parameter expansion and reveal the contents of USER we would do this:

# Command Substitution
Command substitution allows us to use the output of a command as an expansion:

# Quoting
Now that we've seen how many ways the shell can perform expansions, it's time to learn how we can control it. Take for example:

# Double Quotes
The first type of quoting we will look at is double quotes. If we place text inside double quotes, all the special characters used by the shell lose their special meaning and are treated as ordinary characters. The exceptions are “$”, “\” (backslash), and “`” (back- quote). This means that word-splitting, pathname expansion, tilde expansion, and brace expansion are suppressed, but parameter expansion, arithmetic expansion, and command substitution are still carried out. Using double quotes, we can cope with filenames containing embedded spaces. Imagine we were the unfortunate victim of a file called two words.txt. If we tried to use this on the command line, word-splitting would cause this to be treated as two separate arguments rather than the desired single argument:
# Single Quotes
When we need to suppress all expansions, we use single quotes. Here is a comparison of unquoted, double quotes, and single quotes:

# Escaping Characters
Sometimes we only want to quote a single character. To do this, we can precede a character with a backslash, which in this context is called the escape character. Often this is done inside double quotes to selectively prevent an expansion:

