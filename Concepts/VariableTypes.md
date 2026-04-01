# Variable types
Every variable has a type which determines what you can do with it. It also has a variety of different states which can be encoded into it (eg: Integer and Float store numbers, Strings store text etc). The variables type also influences what you can do with it. For example it makes sense to be able to add two numbers (Floats or Integers) but what would adding two Booleans look like (it doesn't work!)

```rust
fn main() {
    let boolean: bool = false;
    let integer: i8 = 67;
    let float: f64 = -745.32;
    // Rust does have a String type but it is easier to understand using just the str type instead.
    let str: &str = "hello";
    let array: [bool; 2] = [true, true];
}
```
# Common variable types
Here is a list of the common variable types which you will come across while programming:

| Type       | Aliases             | What it is                                                                   |
| ---------- | ------------------- | ---------------------------------------------------------------------------- |
| Boolean    | `bool`              | A value of `true` or `false`                                                 |
| Integer    | `int`,`i8`          | Numbers which are not decimal                                                |
| Float      | `double`, `f64`     | Numbers which are decimal                                                    |
| String     | `str`               | Text                                                                         |
| Array      | `Vec`, `List`, `[]` | A list of another type of variable                                           |
| Dictionary | `HashMap`, `{}`     | A selection of key value pairs where u can find the values by inputting keys |
## Boolean
These are the most basic variable and can be in either one if two states, `true` or `false`. These are primarily used with control flow statements which take in a Boolean value to change how the program runs. For anyone that knows binary you might think that each bool is stored on a single bit but it is actually stored on a full byte instead for performance reasons.
## Integer
These can only store a number without a decimal part. Most of the time they can store negative values however you can opt out of this in some languages and get a larger amount of space if you know it will always be positive.

> [!NOTE]
> ### Integer overflow
> It is important to note that these numbers are not infinite. This means that when they become sufficiently large they will wrap around to the lowest number. If you are lucky this will result in a  error, if you are unlucky it will silently corrupt your programs state. Normally this number is too big for you to care but it is still good to know.

## Float
This is so called because it is a "floating point number". It can store numbers with a decimal point and has two other special states called `NAN` (**N**ot **A** **N**umber) and `INF` (**Inf**inity). It is important to bote that there are generally two different Floats you have access to, a single and double precision version. The double can store roughly 15 decimal places whereas the single can only store about 8. They are stored in a binary version of standard form so you do not need to worry about integer overflow (if you do somehow reach the maximum or minimum it will become `INF` and `-INF` respectively)
## String
These store "strings" of characters which can be interpreted as text. There are generally two ways these are stored, with a length and with a "null byte terminator". I won't go into too much detail on Strings here as they are highly variable per language but on general there is a way of formatting string which you should use to display other variables.

> [!NOTE]
> ### Text Encoding
> String support can be very patchy in some languages *(looking at you C)* so it is important to understand what you can and cannot put in Strings. If a language only supports ASCII Strings you are limited to Latin glyphs and similar. To find out more I recommend reading this [excellent article](https://www.joelonsoftware.com/2003/10/08/the-absolute-minimum-every-software-developer-absolutely-positively-must-know-about-unicode-and-character-sets-no-excuses/).
## Array
These can store a long list of variables which can be added to and removed from. They are generally created with the form `[x, y, z]`. You can generally access elements of this array using the `array_variable_name[x]` where x is the "index" (position) in the Array. The convention is that Array indexes start from 0 and grow upwards (Apart from lua which starts from 1). Adding to x to an Array generally takes the form of `array_variable_name.push(x)`.
## Dictionary
These allow you to organise data using keys. You insert new keys into it with attached data and then edit them by modifying the value at the key.

[Previous](<./Variables.md>) | [Next](<./Expressions.md>)