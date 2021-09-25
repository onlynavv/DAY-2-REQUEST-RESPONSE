**1. console.log(typeof(1))**

> output: number

description: the data type here is number, because 1 is a number

**2. console.log(typeof(1.1))**

> output: number

description: the number 1.1 is a float number, so the data type will be number

**3. console.log(typeof('1.1'))**

> output: string

description: '1.1' is a string becuase it is enclosed with single/double quotes, it is considered as string in js

**4. console.log(typeof(true))**

> output: boolean

description: its a boolean data type, boolean has only two values true and false, it will be helpful in comparision expressions and condiitional statements. We will get true value for non empty, non zero, objects and arrays.
boolean is one of the primitive data type, which is immutable, we cannot modify the value, in javascript there are 6
primitve data types they are: _number, string, boolean, null, undefined, symbol_, one complex data type is _object_
which is mutable, the _function_ and _array_ is also an object which is also mutable.

**5. console.log(typeof(null))**

> output: object

description: the data type of null is _object_, null is one of the primitive data type, it has only one value _null_
in js null is an _empty object pointer_, the null means _absence of value_

ex:

var item = null
console.log(typeof item)

> output: _object_

interesting fact is the null has been mistakenly implemented as object in early javascript implementation

**6. console.log(typeof(undefined))**

> output: undefined

description:
undefined is one of the property in global scope/object, whose initial value is the primitive value undefined.

if you check:

> window.undefined
> output: _undefined_

undefined is also one of the primitive data type in js , it cannote be mutated and it has only one value
_undefined_, undefined is given when a variable is declared and hasn't been initialized with a value, which means it
doesn't has a value to it

**7. console.log(typeof([]))**

> output: object

description: the type of an array is _object_, object is a complex data type/reference, where it is mutable, the array stores multiple values in a single variable. In both array and object when the variables are copied/assigned to each other, the memory address is copied not the values or key/value pairs

**8. console.log(typeof({}))**

> output: object

description: the data type of object is _object_, that allows to store collection of data

**9. console.log(typeof(NaN))**

> output: number

description: NaN stands for Not a Number, which is a numeric data type, it is also one of the property in the global object , it cannot be used for operations like addition, division, etc. According to ECMAScript standards the numbers should be IEEE-754 floating point data which means they way of writing real numbers in hardwares in single precision and double precision formats, in that _-Infinity, Infinity and NaN are included_, but it is undefined as a real number
