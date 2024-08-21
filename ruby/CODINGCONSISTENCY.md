# Coding Consistency

Consistency leads to predictability, reliability, and ultimately quality.

Achieve coding consistency with:

## Standard Naming Conventions

Inconsistency in naming conventions should be avoided. A standard guideline for naming conventions should be followed to avoid this.

<br/>

**Naming conventions guideline:**

- Use `snake_case` for symbols, methods, and variables.
- Use `CamelCase` for classes and modules, but keep acronyms like `HTTP`, `RFC`, `XML` uppercase.
- Use `snake_case` for naming files and directories, e.g., `hello_world.rb`.
- Define a single class or module per source file. Name the file after the class or module, but replace `CamelCase` with `snake_case`.
- Use `SCREAMING_SNAKE_CASE` for other constants.
- When using `inject` with short blocks, name the arguments according to what is being injected, e.g., `|hash, e|` (mnemonic: hash, element).
- Name predicate methods with a `?`. Predicate methods are methods that return a boolean value. Avoid ending method names with a `?` if they don't return a boolean.
- Avoid prefixing method names with `is_`.

### Bad:
```ruby
def is_empty?
end
```

### Good:
```ruby
def empty?
end
```
- Avoid starting method names with get_.
- Avoid ending method names with ! when there is no equivalent method without the bang. Bangs are to mark a more dangerous version of a method, e.g. save returns a boolean in ActiveRecord, whereas save! will throw an exception on failure. 
- Avoid magic numbers. Use a constant and give it a meaningful name.

<br/>

### Bad - Inconsistent Method Naming Conventions

```ruby
def some_method
  # do something
end

def anotherMethod
  # do another thing
end
```

### Good

```ruby
def some_method
  # do something
end

def another_method
  # do another thing
end
```

## Indenting and Spacing

Consistency in indentation and spacing will make studying the code easier.

**Guidelines for indentation and spacing:**

- For guidelines to comments and spacing, please refer to [COMMENTSANDSPACING.md](COMMENTSANDSPACING.md).

### Bad - Inconsistent Indentations

```ruby
def some_method
  a = 5
    b=6
  c= a+b
  d = a -b
end

 def another_method
 a=2+3
 end
```

### Good

```ruby
def some_method
  a = 5
  b = 6
  c = a + b
  d = a - b
end

def another_method
  a = 2 + 3
end
```

## Standardized Architecture

The architecture and patterns used should be consistent throughout the project. Using one pattern in one part and another in another part will only bring confusion in the long run.

<br/>
<br/>

## Be Consistent with Existing Code

> Using one style consistently throughout our codebase lets us focus on other (more important) issues. Consistency also allows for automation: tools that format your code only work properly when your code is consistent with the expectations of the tooling. In many cases, rules that are attributed to "Be Consistent" boil down to "Just pick one and stop worrying about it"; the potential value of allowing flexibility on these points is outweighed by the cost of having people argue over them. However, there are limits to consistency; it is a good tie breaker when there is no clear technical argument, nor a long-term direction. It applies more heavily locally (per file, or for a tightly-related set of interfaces). Consistency should not generally be used as a justification to do things in an old style without considering the benefits of the new style, or the tendency of the codebase to converge on newer styles over time.

> If you're editing code, take a few minutes to look at the code around you and determine its style. If they use spaces around all their arithmetic operators, you should too. If their comments have little boxes of hash marks around them, make your comments have little boxes of hash marks around them too.

>The point of having style guidelines is to have a common vocabulary of coding so people can concentrate on what you're saying rather than on how you're saying it. We present global style rules here so people know the vocabulary, but local style is also important. If code you add to a file looks drastically different from the existing code around it, it throws readers out of their rhythm when they go to read it. Avoid this.

— [Google C++ Style Guide](https://google.github.io/styleguide/cppguide.html)


**NOTE:**

> ℹ️ **Info:** Consistency does not mean to stick to one rule no matter what. Sometimes style guide recommendations just may not be applicable.
