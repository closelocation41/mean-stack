## Technology Docs

- [Angular](Angular.md)  
- [MongoDB](MongoDB.md)  
- [MySQL](Mysql.md)  
- [Node.js](Node-Js.md)  
- [TypeScript](TypeScript.md)  
- [JavaScript](JavaScript.md)

Here’s a collection of **100 TypeScript interview questions** categorized into **basic** and **advanced** sections, complete with brief answers and examples.

### **Basic TypeScript Interview Questions**

1. **What is TypeScript?**
   - TypeScript is a superset of JavaScript that adds static typing and other features, allowing for better tooling and error checking during development.

2. **How do you define a variable in TypeScript?**
   - You can define a variable using `let`, `const`, or `var`, with type annotations.
   ```typescript
   let name: string = "John";
   const age: number = 30;
   ```

3. **What are the basic types in TypeScript?**
   - The basic types are:
     - `number`, `string`, `boolean`, `void`, `null`, `undefined`, `any`, `never`, `object`, `array`.

4. **What is an interface in TypeScript?**
   - An interface defines the structure of an object or class.
   ```typescript
   interface Person {
     name: string;
     age: number;
   }
   ```

5. **What is the difference between `any` and `unknown`?**
   - `any` allows any type, whereas `unknown` requires type checking before usage.
   ```typescript
   let x: any = 10;
   let y: unknown = 20;
   if (typeof y === "number") {
     console.log(y); // Valid after type check
   }
   ```

6. **How do you define a function in TypeScript?**
   ```typescript
   function greet(name: string): string {
     return `Hello, ${name}`;
   }
   ```

7. **What is a tuple in TypeScript?**
   - A tuple is an array with fixed sizes and known types at each index.
   ```typescript
   let person: [string, number] = ["John", 30];
   ```

8. **Explain TypeScript’s type inference.**
   - TypeScript infers types based on the assigned values.
   ```typescript
   let num = 5; // TypeScript infers `num` as number
   ```

9. **What is a class in TypeScript?**
   - A class in TypeScript is a blueprint for creating objects with properties and methods.
   ```typescript
   class Car {
     make: string;
     model: string;
     constructor(make: string, model: string) {
       this.make = make;
       this.model = model;
     }
   }
   ```

10. **What is the purpose of `readonly` in TypeScript?**
    - It marks a property as immutable.
    ```typescript
    class Person {
      readonly name: string;
      constructor(name: string) {
        this.name = name;
      }
    }
    ```

### **Intermediate TypeScript Interview Questions**

11. **What is a union type in TypeScript?**
    - A union type allows a variable to hold more than one type.
    ```typescript
    let value: string | number = "hello";
    value = 42;
    ```

12. **What is the `never` type in TypeScript?**
    - The `never` type represents values that will never occur (e.g., functions that throw errors or have infinite loops).
    ```typescript
    function throwError(message: string): never {
      throw new Error(message);
    }
    ```

13. **What are generics in TypeScript?**
    - Generics allow you to write reusable code components that work with any data type.
    ```typescript
    function identity<T>(value: T): T {
      return value;
    }
    ```

14. **What is the difference between `interface` and `type`?**
    - Both `interface` and `type` are used to define object shapes, but `interface` is more flexible for merging and extending, while `type` is more general and can define types for anything.
    ```typescript
    interface Person { name: string; }
    type PersonType = { name: string; };
    ```

15. **What is a type alias in TypeScript?**
    - A type alias creates a new name for a type.
    ```typescript
    type StringOrNumber = string | number;
    ```

16. **What are modules in TypeScript?**
    - Modules allow you to split code into separate files and include them using `import` and `export`.
    ```typescript
    // file1.ts
    export const greet = () => "Hello";

    // file2.ts
    import { greet } from './file1';
    console.log(greet());
    ```

17. **What is the `keyof` type operator in TypeScript?**
    - `keyof` returns the type of all keys in a given type.
    ```typescript
    type Person = { name: string; age: number };
    type PersonKeys = keyof Person; // 'name' | 'age'
    ```

18. **What is the purpose of the `as` keyword in TypeScript?**
    - The `as` keyword is used for type assertion, telling TypeScript to treat a value as a different type.
    ```typescript
    let input = "123";
    let num = input as number; // Type assertion
    ```

19. **Explain the concept of `null` and `undefined` in TypeScript.**
    - `null` is used for explicitly empty values, while `undefined` is used for variables that are declared but not assigned a value.

20. **How do you handle asynchronous code in TypeScript?**
    - TypeScript supports promises and async/await syntax.
    ```typescript
    async function fetchData(): Promise<string> {
      return "Data fetched";
    }
    ```

### **Advanced TypeScript Interview Questions**

21. **What is the `this` keyword in TypeScript?**
    - `this` refers to the current instance of the class or function context.
    ```typescript
    class Person {
      name: string;
      constructor(name: string) {
        this.name = name;
      }
      greet() {
        console.log(`Hello, ${this.name}`);
      }
    }
    ```

22. **What is a conditional type in TypeScript?**
    - Conditional types select one of two types based on a condition.
    ```typescript
    type IsString<T> = T extends string ? "Yes" : "No";
    ```

23. **What are mapped types in TypeScript?**
    - Mapped types allow you to create new types by transforming properties of an existing type.
    ```typescript
    type ReadOnly<T> = { readonly [K in keyof T]: T[K] };
    ```

24. **Explain the `Partial<T>` utility type.**
    - `Partial<T>` makes all properties of type `T` optional.
    ```typescript
    interface Person { name: string; age: number; }
    const person: Partial<Person> = { name: "John" };
    ```

25. **What is the `Omit<T, K>` utility type in TypeScript?**
    - `Omit<T, K>` constructs a type by excluding properties `K` from type `T`.
    ```typescript
    interface Person { name: string; age: number; }
    type PersonWithoutAge = Omit<Person, 'age'>;
    ```

26. **How do you extend types in TypeScript?**
    - You can extend types using `extends`.
    ```typescript
    interface Animal { name: string; }
    interface Dog extends Animal { breed: string; }
    ```

27. **What are decorators in TypeScript?**
    - Decorators are special functions that modify classes, methods, or properties.
    ```typescript
    function Log(target: any, key: string) {
      console.log(`Logged: ${key}`);
    }

    class Example {
      @Log
      method() {}
    }
    ```

28. **What is a union type with `null` or `undefined` in TypeScript?**
    - You can combine `null` or `undefined` with other types using union.
    ```typescript
    let value: string | null = null;
    value = "Hello";
    ```

29. **Explain the concept of type guards in TypeScript.**
    - Type guards are used to narrow down types based on conditional checks.
    ```typescript
    function isString(value: any): value is string {
      return typeof value === 'string';
    }
    ```

30. **How do you handle complex type transformations in TypeScript?**
    - You can use mapped types, conditional types, or recursive types for complex transformations.
    ```typescript
    type Flatten<T> = T extends Array<infer U> ? U : T;
    ```
Here are more **advanced TypeScript interview questions** with detailed answers and examples to help deepen your understanding of TypeScript:

### **Advanced TypeScript Interview Questions (Continued)**

31. **What are `infer` and `extends` used for in TypeScript?**
    - `infer` is used in conditional types to infer a type within the condition. `extends` is used to constrain a generic type or to create a conditional type.
    ```typescript
    type ExtractString<T> = T extends string ? T : never;
    type Result = ExtractString<string | number>; // Result is string
    ```

32. **How do you create a recursive type in TypeScript?**
    - Recursive types refer to themselves and are useful for modeling hierarchical data structures like trees.
    ```typescript
    type NestedArray<T> = T | NestedArray<T>[];
    const nestedNumbers: NestedArray<number> = [1, [2, [3]]];
    ```

33. **What is ` keyof typeof` in TypeScript?**
    - `keyof typeof` is a way to infer the keys of an object using `typeof` and then access the type of those keys.
    ```typescript
    const person = { name: "John", age: 30 };
    type PersonKeys = keyof typeof person;  // 'name' | 'age'
    ```

34. **What are `as const` and its benefits?**
    - The `as const` assertion tells TypeScript to infer values as literal types, rather than the more general types.
    ```typescript
    const obj = { name: "John", age: 30 } as const;
    // obj.name is inferred as 'John', not string
    ```

35. **What is the difference between `abstract class` and `interface`?**
    - An abstract class can have implementation for some methods, while an interface only defines the structure. Abstract classes can be extended, while interfaces can be implemented.
    ```typescript
    abstract class Animal {
      abstract sound(): string;
      move(): void { console.log("Moving..."); }
    }
    ```

36. **What are the differences between `interface` and `type` in terms of extendability?**
    - An `interface` can be extended using `extends`, and it supports declaration merging. A `type` can be extended using intersection (`&`) but does not support declaration merging.
    ```typescript
    interface A { name: string; }
    interface A { age: number; }  // Merges to { name: string; age: number; }
    ```

37. **What are `conditional types` and how are they used?**
    - Conditional types allow the creation of types based on conditions, enabling dynamic type construction.
    ```typescript
    type IsNumber<T> = T extends number ? "Yes" : "No";
    type Result = IsNumber<42>; // Result is "Yes"
    ```

38. **Explain `string literal types` in TypeScript.**
    - String literal types allow you to define specific string values rather than the broader `string` type.
    ```typescript
    type Direction = "North" | "South" | "East" | "West";
    ```

39. **How do you use TypeScript with `async/await` for better type checking?**
    - TypeScript infers types of promises and returns, improving the type safety of asynchronous operations.
    ```typescript
    async function fetchData(): Promise<string> {
      return "Data fetched";
    }
    ```

40. **What are utility types in TypeScript, and can you list some common ones?**
    - Utility types are predefined types in TypeScript that help with common transformations of types.
      - `Partial<T>` makes all properties optional.
      - `Required<T>` makes all properties required.
      - `Readonly<T>` makes all properties read-only.
      - `Pick<T, K>` creates a new type by selecting properties `K` from `T`.
      - `Omit<T, K>` creates a new type by omitting properties `K` from `T`.
    ```typescript
    type Person = { name: string; age: number };
    type ReadOnlyPerson = Readonly<Person>;  // { readonly name: string; readonly age: number }
    ```

### **Advanced Patterns and Techniques**

41. **How do you perform `deep cloning` of objects in TypeScript?**
    - You can use recursion or libraries like `lodash` for deep cloning. TypeScript provides type safety when working with complex objects.
    ```typescript
    function deepClone<T>(obj: T): T {
      return JSON.parse(JSON.stringify(obj));
    }
    ```

42. **What are `module augmentation` and `declaration merging`?**
    - Module augmentation allows you to add new functionality to an existing module. Declaration merging allows multiple declarations of the same entity (like an interface) to merge.
    ```typescript
    // Adding new methods to an existing interface
    interface String {
      reverse(): string;
    }

    String.prototype.reverse = function() {
      return this.split('').reverse().join('');
    };
    ```

43. **What is the use of the `in` keyword in TypeScript?**
    - The `in` keyword is used in type narrowing and to check if a property exists in an object.
    ```typescript
    type Person = { name: string; age: number };
    function hasProperty(obj: any, prop: string): boolean {
      return prop in obj;
    }
    ```

44. **What is `as const` and how does it improve type inference?**
    - `as const` asserts that the value is of a literal type, which makes it more specific than the broader types.
    ```typescript
    const arr = [1, 2, 3] as const;
    // arr[0] is inferred as 1, not number
    ```

45. **What is `void` in TypeScript?**
    - `void` represents the absence of a type. It’s used for functions that don’t return anything.
    ```typescript
    function logMessage(message: string): void {
      console.log(message);
    }
    ```

46. **How do you make an object immutable in TypeScript?**
    - You can use `Readonly<T>` or `as const` to make an object immutable.
    ```typescript
    const obj = { name: "John", age: 30 } as const;
    ```

47. **How do you handle `null` or `undefined` in TypeScript?**
    - TypeScript has a strict null check option. You can use `?` for optional chaining or use `null` and `undefined` with union types.
    ```typescript
    let name: string | null = null;
    let length = name?.length;  // Returns undefined if name is null
    ```

48. **How do you use the `ReturnType` utility type?**
    - `ReturnType<T>` gets the return type of a function type.
    ```typescript
    function getAge(): number { return 30; }
    type AgeReturnType = ReturnType<typeof getAge>;  // number
    ```

49. **What is `Exclude` and `Extract` in TypeScript?**
    - `Exclude` removes a type from a union type. `Extract` extracts a type from a union type.
    ```typescript
    type T = Exclude<string | number | boolean, boolean>; // string | number
    type U = Extract<string | number | boolean, string>;  // string
    ```

50. **What are `template literal types` in TypeScript?**
    - Template literal types allow the creation of string types based on template literals.
    ```typescript
    type Greeting = `Hello, ${string}!`;
    let message: Greeting = "Hello, John!";  // Valid
    ```

Here are more **advanced TypeScript interview questions** to expand your knowledge further:

### **Advanced TypeScript Interview Questions (Continued)**

51. **What is the `infer` keyword in TypeScript, and how is it used in conditional types?**
    - `infer` is used to declare a variable within a conditional type that can infer the type inside the condition. It's useful when you need to extract a type from a more complex type.
    ```typescript
    type ExtractReturnType<T> = T extends (...args: any[]) => infer R ? R : never;
    type Func = (x: number) => string;
    type ReturnTypeOfFunc = ExtractReturnType<Func>; // string
    ```

52. **What are the differences between `interface` and `type` when dealing with function types?**
    - Both `interface` and `type` can be used to describe function types, but `type` can also describe more complex structures like unions, intersections, and tuple types, whereas `interface` is often more suitable for describing objects and classes.
    ```typescript
    interface Add {
      (a: number, b: number): number;
    }

    type AddType = (a: number, b: number) => number;
    ```

53. **How does TypeScript handle `typeof` in type checking?**
    - The `typeof` operator in TypeScript is used to refer to the type of a variable or property in the code. It's especially useful when you're working with dynamic values.
    ```typescript
    const person = { name: "John", age: 30 };
    type PersonType = typeof person;  // { name: string, age: number }
    ```

54. **What is the `unknown` type, and how is it different from `any`?**
    - The `unknown` type is safer than `any` because you cannot perform any operations on a variable of type `unknown` unless you first narrow it down through type checking.
    ```typescript
    let data: unknown = "hello";
    if (typeof data === "string") {
      console.log(data.toUpperCase());  // Valid after type narrowing
    }
    ```

55. **How do you create a `deep readonly` type in TypeScript?**
    - To create a deep `readonly` type, you need to recursively apply `Readonly` to all nested properties.
    ```typescript
    type DeepReadonly<T> = {
      readonly [P in keyof T]: DeepReadonly<T[P]>;
    };
    type Person = { name: string; address: { street: string; city: string } };
    const person: DeepReadonly<Person> = {
      name: "John",
      address: { street: "Main St", city: "New York" },
    };
    // person.address.city = "Boston";  // Error: Cannot assign to 'city' because it is a read-only property.
    ```

56. **What is the `as` keyword used for in TypeScript?**
    - The `as` keyword is used for type assertions, telling TypeScript to treat a variable as a certain type without performing any checks.
    ```typescript
    let someValue: any = "hello";
    let strLength: number = (someValue as string).length;
    ```

57. **What is the purpose of `this` type in TypeScript?**
    - The `this` type refers to the type of the object that the function is a method of, and it can be used to provide better type safety for method calls.
    ```typescript
    class Person {
      name: string;
      constructor(name: string) {
        this.name = name;
      }
      greet(this: Person): void {
        console.log(`Hello, ${this.name}`);
      }
    }
    ```

58. **How does TypeScript handle method overloading?**
    - TypeScript supports method overloading, where multiple method signatures can be provided for a single function or method.
    ```typescript
    class Calculator {
      add(a: number, b: number): number;
      add(a: string, b: string): string;
      add(a: any, b: any): any {
        return a + b;
      }
    }

    const calc = new Calculator();
    console.log(calc.add(1, 2));  // 3
    console.log(calc.add("a", "b"));  // ab
    ```

59. **What are `indexed access types` in TypeScript?**
    - Indexed access types allow you to retrieve the type of a property from an object type using an index (either a string or a number).
    ```typescript
    type Person = { name: string; age: number };
    type NameType = Person["name"];  // string
    ```

60. **What are `extract` and `exclude` in TypeScript, and how are they used?**
    - `Extract<T, U>` extracts the types from `T` that are assignable to `U`. `Exclude<T, U>` removes types from `T` that are assignable to `U`.
    ```typescript
    type T = Extract<"a" | "b" | "c", "a" | "b">;  // 'a' | 'b'
    type U = Exclude<"a" | "b" | "c", "a">;  // 'b' | 'c'
    ```

### **Types of Generics**

61. **What are generic constraints in TypeScript?**
    - Generic constraints allow you to restrict the type that can be passed into a generic, ensuring that the generic type satisfies certain conditions.
    ```typescript
    function echo<T extends string>(value: T): T {
      return value;
    }

    echo("Hello");  // Valid
    echo(123);      // Error: Argument of type 'number' is not assignable to parameter of type 'string'.
    ```

62. **What is the `ReadonlyArray` in TypeScript?**
    - `ReadonlyArray<T>` represents an array that cannot be modified (i.e., its elements are read-only).
    ```typescript
    let arr: ReadonlyArray<number> = [1, 2, 3];
    arr.push(4);  // Error: Property 'push' does not exist on type 'readonly number[]'.
    ```

63. **How do you create a generic class in TypeScript?**
    - You can create a class with a generic type to allow flexibility when working with different data types.
    ```typescript
    class Box<T> {
      value: T;
      constructor(value: T) {
        this.value = value;
      }
      getValue(): T {
        return this.value;
      }
    }
    const stringBox = new Box("Hello");
    const numberBox = new Box(123);
    ```

64. **What is `keyof` in TypeScript and how does it work?**
    - `keyof` is a type operator that creates a union of all the property names (keys) of a given type.
    ```typescript
    type Person = { name: string; age: number };
    type PersonKeys = keyof Person;  // 'name' | 'age'
    ```

65. **What is `type inference` and how does TypeScript use it?**
    - TypeScript uses type inference to automatically infer the type of variables based on their initialization.
    ```typescript
    let x = 10;  // TypeScript infers the type of x as 'number'
    ```

66. **What are `ambient` declarations in TypeScript?**
    - Ambient declarations are used to define types for values that exist at runtime but aren't necessarily defined in TypeScript files, such as global variables or imported modules.
    ```typescript
    declare const myGlobalVar: string;
    ```

67. **How does TypeScript handle `strict mode` and what are its benefits?**
    - TypeScript's strict mode enables stricter type checking and better safety, helping catch more errors at compile-time.
    ```json
    {
      "compilerOptions": {
        "strict": true
      }
    }
    ```

68. **What are `template literal types` in TypeScript?**
    - Template literal types allow you to create types based on string template literals.
    ```typescript
    type Greeting = `Hello, ${string}!`;
    let greeting: Greeting = "Hello, John!";
    ```

69. **What are `type predicates` and how do they help in type narrowing?**
    - A type predicate is a special type of function that narrows down types in TypeScript.
    ```typescript
    function isString(value: unknown): value is string {
      return typeof value === "string";
    }

    let result: unknown = "hello";
    if (isString(result)) {
      console.log(result.toUpperCase());  // TypeScript knows 'result' is a string here
    }
    ```

70. **What are `declaration files` in TypeScript?**
    - Declaration files (`.d.ts`) provide type information about a module or library, which allows you to use external JavaScript code with TypeScript's type checking.
    ```typescript
    // declare a global variable
    declare const myGlobal: string;
    ```

Here are even more **advanced TypeScript interview questions** with detailed explanations and examples:

### **Advanced TypeScript Interview Questions (Continued)**

71. **What is `typeof` used for in TypeScript and how does it differ from JavaScript?**
    - `typeof` in TypeScript works similarly to JavaScript but can be used to get the type of a variable or property at compile time. It can be used in type annotations and type assertions.
    ```typescript
    const user = { name: "Alice", age: 30 };
    type UserType = typeof user; // { name: string, age: number }
    ```

72. **What are `conditional types` in TypeScript and how are they used?**
    - Conditional types allow you to define a type that depends on another type. It works like a ternary operator, where the type is conditionally chosen based on whether a type extends another type.
    ```typescript
    type IsString<T> = T extends string ? "String" : "Not a string";
    type A = IsString<string>; // "String"
    type B = IsString<number>; // "Not a string"
    ```

73. **Explain `distributive conditional types` in TypeScript.**
    - Distributive conditional types apply a conditional type to each member of a union type individually, making the condition run for every type in the union.
    ```typescript
    type Flatten<T> = T extends (infer U)[] ? U : T;
    type FlattenedType = Flatten<number[] | string[]>; // number | string
    ```

74. **How do you make a type `nullable` in TypeScript?**
    - You can make a type nullable by using the union operator with `null` or `undefined`.
    ```typescript
    type Nullable<T> = T | null;
    type Person = Nullable<string>; // string | null
    ```

75. **What is `indexed access` in TypeScript and how is it useful?**
    - Indexed access types allow you to access the type of a specific property of a given type using the square brackets notation.
    ```typescript
    type Person = { name: string; age: number };
    type NameType = Person['name'];  // string
    ```

76. **How do you extend multiple interfaces in TypeScript?**
    - TypeScript allows you to extend multiple interfaces using `extends`. The resulting interface will combine the properties of all the extended interfaces.
    ```typescript
    interface Person {
      name: string;
    }
    interface Employee {
      role: string;
    }
    interface Manager extends Person, Employee {
      department: string;
    }
    const manager: Manager = { name: "John", role: "Manager", department: "HR" };
    ```

77. **What is the `keyof` operator in TypeScript?**
    - The `keyof` operator creates a union type of all the property names of a given object type.
    ```typescript
    type Person = { name: string; age: number };
    type PersonKeys = keyof Person; // "name" | "age"
    ```

78. **What is the `in` keyword used for in TypeScript?**
    - The `in` keyword is used to iterate over the keys of an object type in a mapped type or in a `for` loop.
    ```typescript
    type Shape = { [key in 'circle' | 'square']: number };
    const area: Shape = { circle: 10, square: 20 };
    
    for (const key in area) {
      console.log(key); // Outputs 'circle' and 'square'
    }
    ```

79. **Explain the `Exclude` and `Extract` utility types in TypeScript.**
    - `Exclude<T, U>` removes types from `T` that are assignable to `U`. `Extract<T, U>` extracts types from `T` that are assignable to `U`.
    ```typescript
    type Excluded = Exclude<'a' | 'b' | 'c', 'a'>; // 'b' | 'c'
    type Extracted = Extract<'a' | 'b' | 'c', 'a'>; // 'a'
    ```

80. **How do you use `Readonly<T>` in TypeScript?**
    - `Readonly<T>` creates a type where all the properties of `T` are read-only, meaning their values cannot be changed.
    ```typescript
    interface Person {
      name: string;
      age: number;
    }
    const person: Readonly<Person> = { name: "John", age: 30 };
    // person.age = 35; // Error: Cannot assign to 'age' because it is a read-only property.
    ```

81. **What is the `never` type in TypeScript and when should it be used?**
    - The `never` type represents values that never occur, such as functions that throw exceptions or never return a value.
    ```typescript
    function throwError(message: string): never {
      throw new Error(message);
    }
    ```

82. **What are `template literal types` in TypeScript?**
    - Template literal types allow you to construct types using string templates and placeholders.
    ```typescript
    type Greeting = `Hello, ${string}!`;
    const message: Greeting = "Hello, Alice!"; // Valid
    ```

83. **How can you use `assertion functions` in TypeScript?**
    - Assertion functions are used to narrow types in a more specific manner. You use `asserts` to signal that a function narrows the type of a variable.
    ```typescript
    function isString(value: any): asserts value is string {
      if (typeof value !== 'string') {
        throw new Error('Not a string');
      }
    }

    let x: unknown = "Hello";
    isString(x);  // Now TypeScript knows that x is a string
    console.log(x.toUpperCase());  // Valid after type assertion
    ```

84. **What is the `unknown` type and how does it differ from `any`?**
    - `unknown` is a safer alternative to `any`. You can't perform operations on `unknown` types until you explicitly check their types.
    ```typescript
    let x: unknown = 5;
    // let y: number = x; // Error: Type 'unknown' is not assignable to type 'number'.
    if (typeof x === "number") {
      let y: number = x;  // Now it's valid
    }
    ```

85. **How do you create a `type alias` for a function in TypeScript?**
    - You can create a type alias for a function using the `type` keyword.
    ```typescript
    type AddFn = (a: number, b: number) => number;
    const add: AddFn = (a, b) => a + b;
    ```

86. **What are the advantages of using TypeScript over JavaScript?**
    - TypeScript offers several advantages over JavaScript:
      - **Static type checking**: Helps catch errors at compile-time instead of run-time.
      - **Improved tooling**: Provides features like autocompletion, type inference, and refactoring support.
      - **Better maintainability**: Types improve code readability and maintainability.
      - **Rich configuration options**: TypeScript provides flexibility in configuration for different project needs.

87. **How do you use `type guards` in TypeScript?**
    - Type guards allow you to narrow the type of a variable within a specific scope. You can create custom type guards using `is` to check types dynamically.
    ```typescript
    function isString(value: unknown): value is string {
      return typeof value === 'string';
    }

    let value: unknown = "Hello";
    if (isString(value)) {
      console.log(value.toUpperCase());  // TypeScript knows 'value' is a string
    }
    ```

88. **What are `generics` in TypeScript and how do they work?**
    - Generics provide a way to create components that work with any type, while still maintaining type safety.
    ```typescript
    function identity<T>(value: T): T {
      return value;
    }

    let result = identity(42);  // T is inferred as number
    let result2 = identity("hello");  // T is inferred as string
    ```

89. **What are `mapped types` in TypeScript?**
    - Mapped types allow you to transform properties of an existing type into a new one.
    ```typescript
    type Person = { name: string; age: number };
    type ReadonlyPerson = {
      readonly [K in keyof Person]: Person[K];
    };
    const person: ReadonlyPerson = { name: "John", age: 30 };
    // person.age = 40; // Error: Cannot assign to 'age' because it is a read-only property.
    ```

90. **How does TypeScript handle `declaration merging`?**
    - TypeScript allows you to define the same interface multiple times, and they will automatically merge their definitions.
    ```typescript
    interface Person {
      name: string;
    }

    interface Person {
      age: number;
    }

    const person: Person = { name: "Alice", age: 30 };  // Merged interface
    ```

Here are even more **advanced TypeScript interview questions** to continue your learning:

### **Advanced TypeScript Interview Questions (Continued)**

91. **What is the `Exclude` utility type, and how does it work?**
    - `Exclude<T, U>` constructs a type by excluding from `T` all properties that are assignable to `U`.
    ```typescript
    type T = Exclude<'a' | 'b' | 'c', 'a'>;  // 'b' | 'c'
    ```

92. **How do `as const` and literal types work in TypeScript?**
    - Using `as const` tells TypeScript to infer the narrowest possible type, preserving literals rather than broadening them to more general types like `string` or `number`.
    ```typescript
    const fruit = "apple" as const;
    type Fruit = typeof fruit;  // "apple"
    ```

93. **What is the `ReturnType` utility type in TypeScript, and how is it used?**
    - The `ReturnType` utility type extracts the return type of a given function type.
    ```typescript
    type Add = (a: number, b: number) => number;
    type AddReturnType = ReturnType<Add>;  // number
    ```

94. **What is the `Parameters` utility type in TypeScript, and how is it used?**
    - The `Parameters` utility type extracts the parameter types of a function into a tuple type.
    ```typescript
    type Add = (a: number, b: number) => number;
    type AddParameters = Parameters<Add>;  // [number, number]
    ```

95. **Explain the difference between `any`, `unknown`, and `never` types in TypeScript.**
    - `any` can be assigned to any type and any type can be assigned to it, making it very permissive. `unknown` is safer than `any` because it requires type checking before performing operations. `never` represents a value that never occurs (such as functions that throw errors or have infinite loops).
    ```typescript
    let x: any = 5;  // can assign any value
    let y: unknown = 10;  // cannot directly assign to other types without type checking
    function throwError(): never {
      throw new Error("This function throws an error");
    }
    ```

96. **What is the `keyof` and `in` operators in TypeScript?**
    - `keyof` creates a union of all property names (keys) of a given type. `in` is used to iterate over object keys and create mapped types.
    ```typescript
    type Person = { name: string, age: number };
    type PersonKeys = keyof Person;  // "name" | "age"
    
    type ReadOnlyPerson = {
      readonly [K in keyof Person]: Person[K];
    };
    ```

97. **What is the difference between `interface` and `type` in TypeScript?**
    - Both `interface` and `type` can be used to describe the shape of an object, but `interface` can be extended or implemented (by classes or other interfaces), while `type` is more versatile and can describe unions, intersections, and other advanced types.
    ```typescript
    interface Person {
      name: string;
      age: number;
    }
    type Employee = Person & { salary: number };  // Intersection
    ```

98. **How does TypeScript handle `null` and `undefined`?**
    - In TypeScript, `null` and `undefined` are considered separate types. You can specify a variable as potentially `null` or `undefined` by using the union operator (`|`).
    ```typescript
    let value: string | null = null;
    let optionalValue: string | undefined = undefined;
    ```

99. **How do you use the `infer` keyword in TypeScript's conditional types?**
    - The `infer` keyword is used in conditional types to infer a type based on a condition. This is commonly used for extracting types from more complex structures like function return types.
    ```typescript
    type ReturnTypeOfFunction<T> = T extends (...args: any[]) => infer R ? R : never;
    type Func = (x: number) => string;
    type Result = ReturnTypeOfFunction<Func>;  // string
    ```

100. **What are the differences between `type` and `interface` when defining callable or indexable types?**
    - Both `type` and `interface` can define callable and indexable types. However, interfaces are more commonly used to describe object shapes and can be extended, while `type` is used for more complex structures, including unions, intersections, and conditional types.
    ```typescript
    interface Callable {
      (x: number): string;
    }

    type Indexable = {
      [key: string]: number;
    };
    ```

101. **How do you use `extends` in a generic type parameter?**
    - The `extends` keyword is used in generics to constrain a type parameter. It ensures that the type passed into the generic type extends or satisfies the given constraint.
    ```typescript
    function getLength<T extends { length: number }>(item: T): number {
      return item.length;
    }

    const length = getLength([1, 2, 3]);  // 3
    ```

102. **What is the `this` type in TypeScript, and how does it work?**
    - The `this` type is used to define the type of `this` in methods or functions. It can be particularly useful when working with instance methods and ensuring that the correct object is referenced within a method.
    ```typescript
    class Person {
      name: string;
      constructor(name: string) {
        this.name = name;
      }

      greet(this: Person): void {
        console.log(`Hello, ${this.name}`);
      }
    }
    ```

103. **How do you create a `default` type for a function parameter in TypeScript?**
    - TypeScript allows you to set default values for function parameters. When no argument is passed for a parameter, the default value is used.
    ```typescript
    function greet(name: string = "Guest"): string {
      return `Hello, ${name}`;
    }
    ```

104. **How does TypeScript handle `typeof` for type inference?**
    - `typeof` can be used in TypeScript to infer the type of a value, which is particularly useful for inferring types from variables or objects.
    ```typescript
    const person = { name: "Alice", age: 30 };
    type PersonType = typeof person;  // { name: string, age: number }
    ```

105. **What are `mixin types` in TypeScript, and how do they work?**
    - Mixins allow you to combine multiple class behaviors. In TypeScript, you can implement mixins by using `extends` in a class or type to combine functionalities from different sources.
    ```typescript
    class Logger {
      log(message: string) {
        console.log(message);
      }
    }

    class Greeter {
      greet() {
        console.log("Hello!");
      }
    }

    class GreeterLogger implements Logger, Greeter {
      log(message: string) {
        console.log(message);
      }

      greet() {
        console.log("Hello!");
      }
    }
    ```

106. **What is `mapped type` in TypeScript, and how is it useful?**
    - Mapped types allow you to transform properties of an existing type into a new type, useful for making all properties optional or readonly, or for renaming properties.
    ```typescript
    type Person = { name: string; age: number };
    type ReadOnlyPerson = {
      readonly [K in keyof Person]: Person[K];
    };

    const person: ReadOnlyPerson = { name: "Alice", age: 30 };
    // person.age = 35; // Error: Cannot assign to 'age' because it is a read-only property.
    ```

107. **What is `type assertion` in TypeScript, and how do you use it?**
    - Type assertions in TypeScript allow you to override the type that TypeScript infers for a variable. It's used when you're sure that a variable is of a certain type, but TypeScript can't automatically infer it.
    ```typescript
    let value: unknown = "Hello";
    let strLength: number = (value as string).length;
    ```

108. **What is the `never` type, and how is it used in TypeScript?**
    - The `never` type represents values that never occur. It's commonly used in functions that always throw an error or in infinite loops.
    ```typescript
    function throwError(message: string): never {
      throw new Error(message);
    }

    function infiniteLoop(): never {
      while (true) {}
    }
    ```

109. **How does TypeScript handle `structural typing` vs. `nominal typing`?**
    - TypeScript uses **structural typing**, meaning types are compatible based on their structure rather than their name or declaration. Nominal typing (used in languages like Java) compares types based on their names.
    ```typescript
    type Point = { x: number; y: number };
    const point1: Point = { x: 1, y: 2 };
    const point2 = { x: 1, y: 2 };  // This is valid even though it isn't explicitly declared as `Point`
    ```


