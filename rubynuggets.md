Ruby Coding Tips / Tricks / Things to Remember
==============================================

- Implicit "return" so you don't need to write "return" you can just write the variable.
- You can chain methods by adding methods to an "end" statement. Looks quite weird, but also slick :)
- In Ruby, symbols are often used as keys in hashes because they are more efficient than strings. Symbols are immutable which is great for hashes as changing the key breaks the relationship between key and value.

Handy In-Built Methods
-----------------------

- The max method returns the max value of a collection of elements such as an array or range. Usually used like this:

>numbers = [3, 5, 2, 8, 1] max_number = numbers.max = returns the highest number, 8.

- If we were to use numbers.max(2), [8, 5] is returned.
- Max method can also take a block, which is useful if we want to determine the value of each element in a collection. E.g. If we want to know what is the longest string of an array.
- Another, seemingly rarer, use of .max method is to set a cap at a specified number.

>e.g. [var1 - var2, 0].max ensures that after subtracting var1 from var2, the highest result will be 0. Ensuring no negative numbers can be returned from this calculation.

- In the last bit of code, .max simply returns whatever is the highest value, var1-var2 or 0.

- The .map method is great when you want to construct an array from an "enumerable". You can use .map on anything that Ruby includes in the enumerable module. e.g. You can call .map on: ranges, arrays, hashes and more!

>(1..5).map { |n| n**2 } # returns [1, 4, 9, 16, 25]
>{ name: "John", age: 30 }.map { |k, v| "#{k}: #{v}" } # returns ["name: John", "age: 30"]

- .map(&:name) is shorthand for when you want to use .map on an enumerable and want to apply one method to each element.

> [1,2,3].map {|n| n.is_even?} === [1,2,3].map(&:even?)

- My last codewars exercise was to transform *just* the first element of each array inside a nested array. So [["20", age], ["30", age]] would be: [[20, age], [30, age]]. In the .map block I used I created a new array that represents the elements of the nested array:

>arr.map {|n| [n.first.to_i, n.last] } # creates a new array with first element changing to an int and last element unchanged.
>arr.map {|n| [n[0].to_i, n[-1]]} # this is the same thing

- If there were three elements to each nested array, I could add another element into the block e.g. [n[0]to_i, n[1], n[-1]]. As we can see .map is useful for performing an operation on particular elements of a nested array. We can also use .map_with_index to return the index along with the elements if we so wish.

- Turn a multidimensional(nested array) into a regular array using .flatten  e.g.

> [[1], [5], [20]].flatten # returns [1, 5, 20] # useful if you want to add numbers from a nested array.
> [[1], [5], [20]].flatten.sum # returns 26, as .sum wont work on a nested array
