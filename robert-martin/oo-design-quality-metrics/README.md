# Design Quality Metrics by Uncle Bob

## *NOT FINISHED*

## Problems
What makes a design **rigid**, **fragile** and **difficult to reuse**.

1. A design is **rigid** if it cannot be easily changed. A single change causes a cascade of changes in dependant modules.
   
2. **Fragility** is the tendency of a program to break in many places when a single change is made.

3. A design is **difficult to reuse** when the desirable parts of the design are highly dependent upon other details which are not desired

### Example

There is a Copy class which depends on classes Keyboard and Printer. This system has all mentioned problems. We will encounter troubles in case we decide to change input or output.

In order to fix it, we have to change dependencies from classes to abstractions Reader and Writer (**Dependency Inversion**). Now out class Copy depends only on abstractions whicj have their own realizations.

> We can say that a "Good Dependency" is a dependency upon something that is very stable.

**Stability** is being achieved by an entity via becoming **independant** and **responsible**.

The less dependecies an entity has the more **independant** is it. From another side, the more dependants an antity has the more **responsible** is it. In other words, that antity is stable because has no reason to change and lots of reasonds not to change.

A group of highly cohesive classes could be called a **Class Category**.

Dependancies between categories are the ones that needs to be managed. The interdependace inside these categories is, so to say, something that could be sacrified.