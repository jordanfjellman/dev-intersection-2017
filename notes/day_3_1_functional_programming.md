# Functional Techniques for C#

- Kathleen Dollard

## Method Purity

She adds _substringAfter()_ and _substringBefore()_ for testing purposes if the language doesn't have them.

Make decisions on logging and exceptions for purity's sake

- Does logging make a method impure?
- How do you treat exceptions for impurity?

## Linq

Imparative programming is the opposite of function programming.

If you switch the order of imparative programming, you don't know if you've changed the program.
Functional programming is more predicatable.

## Inside-Out Programming

## Exceptions

Don't carry accross bounderies, because it gives information about the technology used.
Instead, use a data result.
(This was designed before tuples, which may change the way to return data)
