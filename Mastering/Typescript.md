**I. Introduction to TypeScript**

*   Understanding TypeScript's Purpose
    *   Addressing limitations of JavaScript: maintainability, scalability
    *   Benefits: static typing, enhanced tooling, improved code organization
*   Setting up a TypeScript Development Environment
    *   Installing Node.js and npm (Node Package Manager)
    *   Installing TypeScript globally: `npm install -g typescript`
    *   Verifying TypeScript installation: `tsc -v`
*   Basic TypeScript Compilation
    *   Creating a simple TypeScript file (`.ts`)
        *   Example: `console.log("Hello, TypeScript!");`
    *   Compiling TypeScript to JavaScript: `tsc your_file.ts`
    *   Understanding the output JavaScript file (`.js`)
*   Configuration with `tsconfig.json`
    *   Creating a `tsconfig.json` file: `tsc --init`
    *   Common configuration options: `target`, `module`, `outDir`, `rootDir`, `sourceMap`
        *   `target`: Specifies the ECMAScript target version (e.g., `ES5`, `ES6`, `ES2020`).
        *   `module`: Specifies the module code generation style (e.g., `commonjs`, `esnext`).
        *   `outDir`: Specifies the output directory for compiled JavaScript files.
        *   `rootDir`: Specifies the root directory for input TypeScript files.
        *   `sourceMap`: Enables source map generation for debugging.
    *   Compiling using `tsconfig.json`: `tsc` (without specifying the file)

**II. Basic Types in TypeScript**

*   Understanding Static Typing
    *   Type annotations: Explicitly declaring the type of a variable.
        *   Example: `let message: string = "Hello";`
    *   Type inference: TypeScript automatically determining the type based on the value.
        *   Example: `let count = 10;` (TypeScript infers `count` as `number`)
*   Primitive Types
    *   `boolean`: `true` or `false`
    *   `number`: All numeric values (integers and floating-point numbers)
    *   `string`: Textual data
    *   `null`: Represents a null value
    *   `undefined`: Represents an uninitialized value
    *   `symbol`: (ES6) Represents a unique identifier
    *   `bigint`: Represents integers of arbitrary precision (ES2020)
*   `any` Type
    *   Disabling type checking: Assigning `any` to a variable.
        *   Example: `let anything: any = "Can be anything";`
    *   Use cases and drawbacks of using `any`.
*   `void` Type
    *   Representing the absence of a return value in a function.
        *   Example: `function logMessage(): void { console.log("Logged!"); }`
*   `never` Type
    *   Representing functions that never return (e.g., always throw an error or infinite loop).
        *   Example: `function throwError(message: string): never { throw new Error(message); }`
*   `unknown` Type
    *   Type-safe alternative to `any` when the type is not known at compile time.
    *   Requires type assertions or type narrowing before use.
        *   Example:
            ```typescript
            let userInput: unknown;
            userInput = "Hello";
            if (typeof userInput === "string") {
              let message: string = userInput; // Type narrowing
              console.log(message.toUpperCase());
            }
            ```

**III. Complex Types in TypeScript**

*   Arrays
    *   Declaring arrays of specific types: `let numbers: number[] = [1, 2, 3];`
    *   Using generic array type: `let names: Array<string> = ["Alice", "Bob"];`
    *   Readonly arrays: `let readonlyArray: readonly number[] = [1, 2, 3];`
*   Tuples
    *   Declaring tuples with fixed types and lengths: `let person: [string, number] = ["John", 30];`
    *   Accessing tuple elements by index: `person[0]`, `person[1]`
    *   Limitations and best practices of tuple usage.
*   Objects
    *   Defining object types using interfaces or type aliases.
    *   Object type literals: `let point: { x: number, y: number } = { x: 10, y: 20 };`
*   Enums
    *   Defining named constants: `enum Color { Red, Green, Blue }`
    *   Numeric enums: Assigning numeric values to enum members.
        *   Example: `enum StatusCode { OK = 200, NotFound = 404, InternalServerError = 500 }`
    *   String enums: Assigning string values to enum members.
        *   Example: `enum Direction { Up = "UP", Down = "DOWN", Left = "LEFT", Right = "RIGHT" }`
    *   Using enums to improve code readability and maintainability.
*   Type Aliases
    *   Creating aliases for existing types: `type Point = { x: number, y: number };`
    *   Using type aliases to simplify complex type declarations.
*   Union Types
    *   Allowing a variable to have multiple types: `let result: string | number = "Success";`
    *   Type narrowing with union types.
        *   Example:
            ```typescript
            function printId(id: string | number) {
              if (typeof id === "string") {
                console.log(id.toUpperCase());
              } else {
                console.log(id * 2);
              }
            }
            ```
*   Intersection Types
    *   Combining multiple types into a single type: `type Colorful = { color: string }; type Circle = { radius: number }; type ColorfulCircle = Colorful & Circle;`
    *   Creating complex types by combining existing types.

**IV. Functions in TypeScript**

*   Function Declarations and Expressions
    *   Declaring functions with type annotations for parameters and return values.
        *   Example: `function add(x: number, y: number): number { return x + y; }`
    *   Function expressions: `const multiply = (x: number, y: number): number => x * y;`
*   Optional Parameters
    *   Marking parameters as optional using `?`: `function greet(name: string, greeting?: string): string { ... }`
    *   Handling optional parameters within the function body.
*   Default Parameters
    *   Providing default values for parameters: `function greet(name: string, greeting: string = "Hello"): string { ... }`
*   Rest Parameters
    *   Accepting a variable number of arguments as an array: `function sum(...numbers: number[]): number { ... }`
*   Function Overloading
    *   Defining multiple function signatures with different parameter types and return types.
    *   Providing specific implementations for each overload.
        *   Example:
            ```typescript
            function add(x: number, y: number): number;
            function add(x: string, y: string): string;
            function add(x: any, y: any): any {
              return x + y;
            }
            ```

**V. Interfaces and Classes**

*   Interfaces
    *   Defining contracts for objects: specifying required properties and their types.
        *   Example:
            ```typescript
            interface Person {
              name: string;
              age: number;
              greet(): string;
            }
            ```
    *   Implementing interfaces in classes.
    *   Extending interfaces: creating new interfaces based on existing ones.
    *   Optional properties in interfaces: `interface Config { timeout?: number; }`
    *   Readonly properties in interfaces: `interface Point { readonly x: number; readonly y: number; }`
*   Classes
    *   Defining classes with properties and methods.
        *   Example:
            ```typescript
            class Animal {
              name: string;
              constructor(name: string) {
                this.name = name;
              }
              move(): void {
                console.log("Moving...");
              }
            }
            ```
    *   Constructors: Initializing object properties.
    *   Access modifiers: `public`, `private`, `protected`.
        *   `public`: Accessible from anywhere.
        *   `private`: Accessible only within the class.
        *   `protected`: Accessible within the class and its subclasses.
    *   Inheritance: Creating subclasses that inherit properties and methods from parent classes.
    *   Method overriding: Providing a different implementation for a method in a subclass.
    *   Abstract classes and methods: Defining classes that cannot be instantiated directly and methods that must be implemented by subclasses.
    *   Implementing interfaces in classes: Enforcing specific contracts.

**VI. Generics**

*   Understanding Generics
    *   Creating reusable components that can work with different types.
    *   Type parameters: Defining placeholders for types that will be specified later.
        *   Example: `function identity<T>(arg: T): T { return arg; }`
*   Generic Functions
    *   Using type parameters in function signatures.
    *   Type inference with generic functions.
*   Generic Interfaces
    *   Defining interfaces with type parameters.
    *   Using generic interfaces to create reusable data structures.
*   Generic Classes
    *   Defining classes with type parameters.
    *   Using generic classes to create reusable components.
*   Constraints
    *   Limiting the types that can be used with a generic type parameter.
    *   Using `extends` keyword to define constraints.
        *   Example: `function logIdentity<T extends { message: string }>(arg: T): T { ... }`
*   Keyof Operator
    *   Using the `keyof` operator to get the union of keys from an object type.
        *   Example:
            ```typescript
            function getProperty<T, K extends keyof T>(obj: T, key: K): T[K] {
              return obj[key];
            }
            ```

**VII. Modules**

*   Understanding Modules
    *   Organizing code into reusable units.
    *   Avoiding naming conflicts.
*   Internal Modules (Namespaces)
    *   Grouping related code within a namespace.
    *   Declaring namespaces: `namespace MyNamespace { ... }`
    *   Exporting members from a namespace: `export class MyClass { ... }`
*   External Modules (ES Modules)
    *   Using `import` and `export` statements to share code between files.
    *   Exporting individual members: `export const PI = 3.14;`
    *   Exporting multiple members: `export { PI, E };`
    *   Default exports: `export default class MyClass { ... }`
    *   Importing modules: `import { PI } from "./math";`
    *   Importing default exports: `import MyClass from "./my-class";`
    *   Module resolution: How TypeScript finds modules.
*   Working with Third-Party Libraries
    *   Installing type definitions for JavaScript libraries using `@types`.
        *   Example: `npm install --save-dev @types/jquery`
    *   Using ambient declarations to define types for libraries without type definitions.

**VIII. Advanced Types**

*   Conditional Types
    *   Defining types that depend on other types.
    *   Using the `infer` keyword to extract types.
        *   Example: `type ReturnType<T extends (...args: any) => any> = T extends (...args: any) => infer R ? R : any;`
*   Mapped Types
    *   Transforming existing types to create new types.
    *   Using the `readonly` and `?` modifiers in mapped types.
        *   Example: `type ReadonlyPerson = { readonly [K in keyof Person]: Person[K] };`
*   Template Literal Types (TypeScript 4.1+)
    *   Creating types based on template literals.
    *   Using template literal types to create string-based types.
        * Example: `type EventName<T extends string> = `${T}Changed`;`
*   Discriminated Unions
    *   Creating union types where each member has a common, discriminating property.
        *   Example:
            ```typescript
            interface SuccessResult {
              success: true;
              value: string;
            }

            interface ErrorResult {
              success: false;
              error: string;
            }

            type Result = SuccessResult | ErrorResult;

            function handleResult(result: Result) {
              if (result.success) {
                console.log("Success:", result.value);
              } else {
                console.error("Error:", result.error);
              }
            }
            ```

**IX. Decorators**

*   Understanding Decorators
    *   Adding metadata and modifying the behavior of classes, methods, properties, and parameters.
    *   Enabling experimentalDecorators in `tsconfig.json`: `"experimentalDecorators": true`
*   Class Decorators
    *   Applying decorators to classes.
    *   Modifying the constructor of a class.
        *   Example:
            ```typescript
            function sealed(constructor: Function) {
              Object.seal(constructor);
              Object.seal(constructor.prototype);
            }

            @sealed
            class MyClass {
              // ...
            }
            ```
*   Method Decorators
    *   Applying decorators to methods.
    *   Modifying the behavior of a method.
        * Example:
            ```typescript
            function log(target: any, propertyKey: string, descriptor: PropertyDescriptor) {
                const originalMethod = descriptor.value;
                descriptor.value = function(...args: any[]) {
                    console.log("Calling", propertyKey, "with arguments", args);
                    const result = originalMethod.apply(this, args);
                    console.log("Method", propertyKey, "returned", result);
                    return result;
                };
                return descriptor;
            }

            class MyClass {
                @log
                add(x: number, y: number): number {
                    return x + y;
                }
            }
            ```
*   Property Decorators
    *   Applying decorators to properties.
    *   Modifying the behavior of a property.
        * Example:
            ```typescript
            function LogProperty(target: any, key: string) {
                let _val = target[key];
                const getter = function() {
                    console.log(`Get: ${key} => ${_val}`);
                    return _val;
                };
                const setter = function(newVal: any) {
                    console.log(`Set: ${key} => ${newVal}`);
                    _val = newVal;
                };
                if (delete target[key]) {
                    Object.defineProperty(target, key, {
                        get: getter,
                        set: setter,
                        enumerable: true,
                        configurable: true
                    });
                }
            }

            class Example {
                @LogProperty
                name: string;

                constructor(name: string) {
                    this.name = name;
                }
            }
            ```
*   Parameter Decorators
    *   Applying decorators to parameters.
    *   Adding metadata to parameters.
*   Decorator Factories
    *   Creating functions that return decorators.
    *   Using decorator factories to configure decorators.

**X. TypeScript with React**

*   Setting up a React Project with TypeScript
    *   Using Create React App with TypeScript template: `npx create-react-app my-app --template typescript`
*   Typing React Components
    *   Defining prop types using interfaces or type aliases.
    *   Using `React.FC` (Functional Component) type.
        *   Example: `interface Props { name: string; } const MyComponent: React.FC<Props> = ({ name }) => { ... };`
    *   Typing state using interfaces or type aliases.
    *   Using `useState` hook with type annotations.
        *   Example: `const [count, setCount] = useState<number>(0);`
    *   Typing event handlers.
        *   Example: `<button onClick={(event: React.MouseEvent<HTMLButtonElement>) => handleClick(event)}>Click me</button>`
*   Using Generics with React Components
    *   Creating reusable components that can work with different types.
*   Working with `useRef`
    *   Typing refs to specific DOM elements: `const inputRef = useRef<HTMLInputElement>(null);`
*   Context API with TypeScript
    *   Typing the context value using interfaces or type aliases.
*   Redux with TypeScript
    *   Typing actions, reducers, and the store.
*   Best Practices for Using TypeScript with React

**XI. Asynchronous Programming with TypeScript**

*   Promises
    *   Understanding the concept of Promises.
    *   Creating Promises using the `Promise` constructor.
    *   Using `then`, `catch`, and `finally` methods.
    *   Typing Promises with generic types.
        *   Example: `const fetchData: Promise<string> = new Promise((resolve, reject) => { ... });`
*   Async/Await
    *   Simplifying asynchronous code with `async` and `await` keywords.
    *   Using `async` functions to handle Promises.
    *   Typing `async` functions with return type annotations.
        *   Example: `async function getData(): Promise<string> { ... }`
*   Error Handling in Asynchronous Code
    *   Using `try...catch` blocks to handle errors in `async` functions.
*   Working with Multiple Promises
    *   Using `Promise.all` to execute multiple Promises concurrently.
        *   Example: `const results = await Promise.all([fetchData1(), fetchData2()]);`
    *   Using `Promise.race` to get the result of the first Promise to resolve.
*   Generators and Iterators (Less Common, but Useful)
    *   Understanding generator functions and iterators.
    *   Using `yield` keyword to pause and resume execution.
    *   Typing generator functions with `Generator` type.
        *   Example: `function* myGenerator(): Generator<number, string, any> { ... }`

**XII. Testing TypeScript Code**

*   Choosing a Testing Framework
    *   Popular options: Jest, Mocha, Jasmine
*   Setting up a Testing Environment
    *   Installing testing frameworks and necessary dependencies.
    *   Configuring TypeScript compiler for testing.
*   Writing Unit Tests
    *   Testing individual functions and classes.
    *   Using assertions to verify expected behavior.
*   Writing Integration Tests
    *   Testing the interaction between different modules.
*   Mocking Dependencies
    *   Replacing real dependencies with mock objects for testing.
*   Code Coverage
    *   Measuring the percentage of code covered by tests.
    *   Using code coverage tools to identify areas that need more testing.
*   Continuous Integration (CI)
    *   Integrating tests into a CI pipeline for automated testing.
    *   Using CI tools like Jenkins, Travis CI, or GitHub Actions.

**XIII. Advanced Configuration and Tooling**

*   Linting with ESLint
    *   Setting up ESLint with TypeScript.
    *   Configuring ESLint rules to enforce code style and prevent errors.
*   Formatting with Prettier
    *   Setting up Prettier to automatically format code.
    *   Integrating Prettier with ESLint.
*   Debugging TypeScript Code
    *   Using source maps to debug TypeScript code in the browser.
    *   Using a debugger in VS Code or other IDEs.
*   Custom Type Definitions
    *   Creating custom type definitions for JavaScript libraries that don't have them.
    *   Using declaration files (`.d.ts`) to define types.
*   Build Tools
    *   Using build tools like Webpack or Parcel to bundle TypeScript code.
    *   Configuring build tools to optimize code for production.
*   Monorepos
    *   Managing multiple packages in a single repository.
    *   Using tools like Lerna or Nx to manage monorepos.
