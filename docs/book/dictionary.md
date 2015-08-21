# Dictionary

In this dictionary you will find some nice descriptions about how some words
mean in the Elcodi ecosystem.

### Attribute



### Bamboo

Bamboo is a simple and basic E-commerce application based on Symfony, that uses
all Elcodi components for it's own business logic. All Elcodi related best 
practices are applied and used in this project.

### Component

A component is a simple PHP Library. Only PHP Classes are placed inside this 
package and must be framework agnostic.

### Factory

PHP Class with one single responsibility: create a new entity instance. This
class should know as well how this entity instance must be initialized given
an specific environment

- My CustomerFactory initializes all my Customer new instances as females 
  because my project is focused on women.

### Plugin

Because Bamboo must be a project with a well-designed extension point. For such
reason, and taking advantage of how Symfony Bundles work, we have created a 
plugin engine in order to allow people overwriting and extending Bamboo in a
very simple and intuitive way.

When we refer to a Plugin then, we refer to these Bundles that are thought as 
Plugins, following their specification.

### Variant

Sometimes a Product is not enough when we need to define something we want to 
sell. Let's see an example.

* In our store we sell a T-shirt
* If your T-Shirt is only sold only in red color and you only have one size, 
  then that's good enough for you
* But what happens when your T-shirt is available in many colors or many sizes?
* Your product will still be the same T-shirt, but you need a new entity to say
  that people can buy this T-shirt in red, blue and grey, and in several sizes,
  like small, medium or large.
* When we talk about Variant, we talk about each available combination, 
  containing the original product, the color and the size.
* Of course, if your have several Variants of a specific Product, people will be
  able to add these variants to their carts, instead of the Product.
