
# Comments

## **5 Types Of Ruby Comments & How to Use Them Correctly**

<br/>

Comment generally adds information to the code that may be helpful for developers.


The most common type of comment is the single-line comment.


## Single Line Comments

-   The comment starts with a hash(#) symbol
    
-   The space is put between the content and the start of the comment to make it easier to read.
    

Syntax:

```ruby
# I like apples & oranges

[].size # get array size
```

<br/>

## Multi-Line Comments

Multi-line comments are regular single line comments. We can also call it block comments.

Syntax:

```ruby
# aaa

# bbb

# ccc
```

<br/>

## SheBang Comments

A shebang (#!) is a special kind of comment that tells a Unix shell (like bash) how to interpret this file.

When this comment is added at the top of the file…We will be able to run your Ruby files as executable files, assuming they have the right permissions to do that.

  

Syntax:

```ruby
#!/usr/bin/env ruby
```

This also allows us to set specific command-line options, like the warning option.

  

Example:

```ruby
#!/usr/bin/env ruby -w
```

Every time we run this code it will run with these options, so we don’t have to pass them in manually

<br/>  

## Magic Comments

A magic comment changes the behavior of the Ruby interpreter in some way.

For example:

```ruby
The  frozen_string_literals  comment will make the strings frozen by default.
```
  
Syntax:

```ruby
# frozen_string_literal: true

# encoding: utf-8

# warn_indent: true
```

This will show a warning whenever your indentation is wrong.

Example:

```ruby
def comments

end
```

Which results

```ruby
warning: mismatched indentations at 'end' with 'def' at 3
```

## ERB Comments

If we are using rails erb for view, we use these comments.

Syntax:

```ruby
<%# ERB comment %>
```
  
<br/>
<br/>


# Spacing

## Tabs or space

Normally we use only space for indentation. We don’t use hard tabs.

## Indentation

Use two spaces per indentation.

# Bad - Four spaces

```ruby
def some_method

do_something

end
```

### Good

```ruby
def some_method

do_something

end
```

### Maximum Line Length

- Limit lines to 80 characters.

<br/>

### No Trailing Whitespace

- Better to Avoid trailing whitespace.

<br/>

### Line Endings

- Unix-style line endings

<br/>

### Should I Terminate Files with a Newline?

- End each file with a newline.

<br/>
<br/>

## Spaces and Operators

- Use spaces around operators, after commas, colons and semicolons. Whitespace might be irrelevant to the ruby interpreter, but its proper use is the key to writing easily readable code.

### Bad

```ruby
sum=1+2

a,b=1,2

class FooError<StandardError;end
```

### Good

```ruby
sum = 1 + 2

a, b = 1, 2

class FooError < StandardError; end
```

<br/>

## There are a few exceptions:

-   Exponent operator:

### Bad

```ruby
e = M * c ** 2
```

### Good

```ruby
e = M * c**2
```

<br/>

### Slash in rational literals:

### Bad

```ruby
o_scale = 1 / 48r
```

### Good

```ruby
o_scale = 1/48r
```

-   Safe navigation operator:

### Bad

```ruby
foo &. bar

foo &.bar

foo&. bar
```

### Good

```ruby
foo&.bar
```

<br/>

## Spaces and Braces

No spaces after (, [ or before ], ). Use spaces around { and before }.

### Bad

```ruby
some( arg ).other

[ 1, 2, 3 ].each{|e| puts e}
```
  
### Good

```ruby
some(arg).other

[1, 2, 3].each { |e| puts e }
```

{ and } deserve a bit of clarification, since they are used for block and hash literals, as well as string interpolation.

For hash literals two styles are considered acceptable. The first variant is slightly more readable (and arguably more popular in the Ruby community in general). The second variant has the advantage of adding visual difference between block and hash literals. Whichever one you pick - apply it consistently.

### Good - space after { and before }

```ruby
{ one: 1, two: 2 }
```

### Good - no space after { and before }

```ruby
{one: 1, two: 2}
```

With interpolated expressions, there should be no padded-spacing inside the braces.

### Bad

```ruby
"From: #{ user.first_name }, #{ user.last_name }"
```

### Good

```ruby
"From: #{user.first_name}, #{user.last_name}"
```

<br/>

## No Space Inside Range Literals

### Bad

```ruby
1 .. 3

'a' ... 'z'
```

### Good

```ruby
1..3

'a'...'z'
```
<br/>


## Empty Lines Between Methods

Use empty lines between method definitions and also to break up methods into logical paragraphs internally.

### Bad

```ruby
def some_method

data = initialize(options)

data.manipulate!

data.result

end


def some_other_method

result

end
```

### Good

```ruby
def some_method

data = initialize(options)

data.manipulate!

data.result

end
  

def some_other_method

result

end
```
<br/>


## Two or More Empty Lines

Don’t use several empty lines in a row.


### Bad - It has two empty lines.

```ruby
some_method


some_method
```
  

### Good - It has one empty line.

```ruby
some_method

some_method
```
<br/>


## Empty Lines Between Attribute Accessor

Use empty lines around the access modifier.

### Bad

```ruby
class Foo
def bar; end
private
def baz; end
end
```

### Good

```ruby
class Foo
def bar; end

private 

def baz; end
end
```

<br/>

## Spaces Around Equals

Use spaces around the = operator when assigning default values to method parameters:

### Bad

```ruby
def some_method(arg1=:default, arg2=nil, arg3=[])

# do something...

end
```

### Good

```ruby
def some_method(arg1 = :default, arg2 = nil, arg3 = [])

# do something...

end
```

<br/>

## Empty Lines Around Bodies

Don’t use empty lines around method, class, module, block bodies. 

### Bad

```ruby
class Foo

    def foo

        begin

            do_something do

                something

            end

        rescue

            something

        end

        true

    end

end
```

### Good

```ruby
class Foo
    def foo
        begin
            do_something do
                something
            end
        rescue
            something
        end
    end
end
```
  
<br/>

## Space in Method Calls

Do not put a space between a method name and the opening parenthesis.

### Bad

```ruby
puts (x + y)
```
  
### Good

```ruby
puts(x + y)
```

## Space in Brackets Access

Do not put a space between a receiver name and the opening brackets.

### Bad

```ruby
collection [index_or_key]
```

### Good

```ruby
collection[index_or_key]
```
