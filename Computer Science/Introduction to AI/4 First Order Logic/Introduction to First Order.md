First order logic (Predicate logic) is an expansion on prepositional logic that allows for more expression. It's very hard to describe objects and their properties within prepositional logic because of the number of variables required. **Prepositional logic gets quite large with few objects**. I'm sure you've seen it if you've tried to do a few larger problems.

In particular prepositional logic has the following problems
1. It cannot represent objects
2. Cannot represent relationships between things
3. Not really that expressive

Because of this problem of lacking expression we need to expand our definitions in order to allow for something greater. This can be done by adding additional logical elements

# Elements of First Order Logic
## [[Computer Science/Introduction to AI/0 Lectures/Lecture 16.pdf#page=16|Objects]]
These are instances of *something* which has parts or can be entire classes of objects.

There are subtypes of objects which are slightly more specific
- Constants: An individual objects such as a specific box
- Variables: These describe entire types of objects which have some similar properties such as a person

## [[Computer Science/Introduction to AI/0 Lectures/Lecture 16.pdf#page=20|Predicates]]
A type of symbol which **maps from an object to a boolean value**. These take objects (variables or constants) as input and return true or false depending on if the "query" is true or not
 
## [[Computer Science/Introduction to AI/0 Lectures/Lecture 16.pdf#page=22|Functions]]
Another symbol which **maps from an object to another object**. They are very similar to predicates but instead focus entirely on manipulating objects

## [[Computer Science/Introduction to AI/0 Lectures/Lecture 16.pdf#page=27|Quantifiers]]
These express how sets of objects relate to each other. They are useful for describing properties of entire collections of objects. There are two major types of quantifiers

### Universal Quantifiers
In english they state "for all" or that something is true about all possible values of some reference variable. These can be combined with functions to get specific properties about specific objects

Example sentence
$$
\forall x \space \text{Friends}(\text{Joel}, x) \implies \text{likes}(x, \text{cake})
$$
Which implies that all of the friends of Joel like cake

### Existential Quantifier
In english this states "there exists" or "there is at least one". This effectively say that there is at least one person for which the sentence is true

Here's an example
$$
\exists x \space \text{Friends}(Joel, x) \implies \text{likes}(x, \text{cake})
$$
Which translates to there being at least one friend of Joel's that likes cake

# Translating Sentences
Translating first order logic sentences can be more difficult because of the larger expression that occurs