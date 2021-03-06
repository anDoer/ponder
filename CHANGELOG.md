
Ponder Changelog
----------------

- [Notes with examples on blog](http://billyquith.github.io/ponder/blog/).

### 2.0

- Version 1.4 was unreleased and morphed into 2.0 because of extensive design changes.
- Runtime functionality (object factory and function calling) decoupled (issue #49).
- Many things renamed in the hope that this will clarify things.
  - FunctionType now FunctionKind. Avoid clash with "type".
  - ValueType now ValueKind. Avoid clash with "type".
  - Arguments now parameters. Functions have parameters and are called with arguments.
- Added support for binding to static functions (issue #46).
- Lua binding generator. Functional but sparse functionality. (issue #40).
- `PONDER_RTTI` renamed to `PONDER_POLYMORPHIC` (issue #36).
- Added function call return policies (issue #51).
- Removed UserObject parent-child. Simplification, unused.
- Removed Function callable behaviour. Unused complication.
- Class::create() allows object creation without an Args list.
- Class::tryFunction() and Class::tryProperty() added.
- Remove properties with 3 accessors. Simplification, use lambdas.


### 1.3

- Ids/Names now configurable using `IdTrait`s.
- Default `IdTrait` uses `string_view` so is more efficient (issue #11).
- Lambda functions recognised as class functions.
- `std::auto_ptr` removed as deprecated in C++11 and causes warning spam in GCC.
- Internal string_view class added as std one still experimental.
- Function and object classifiers.
- Bug fixes.

### 1.2

- Properties now support method chaining or named parameter idiom (issue #28).
- UserObjects can be created from user pointers (issue #30).
- Change `ponder::Type` to enum class `ValueType` (issue #26).
- Remove composed function bindings. Use lambdas instead.
- Re-add function unit tests.

### 1.1

- Placement new creation of objects added.
- Class function and property iterators added.
- Class function and property access by index added.
- Ability to undeclare Classes and Enums.
- Dictionaries ordered internally. Allows for fast binary searching of keys.
- Documentation fixes.

### 1.0.2

- Moved to Catch for unit testing. 

### 1.0

- Boost dependency removed.
