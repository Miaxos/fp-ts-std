---
title: Number.ts
nav_order: 11
parent: Modules
---

## Number overview

Various functions to aid in working with numbers.

Added in v0.1.0

---

<h2 class="text-delta">Table of contents</h2>

- [utils](#utils)
  - [add](#add)
  - [decrement](#decrement)
  - [divide](#divide)
  - [floatFromString](#floatfromstring)
  - [fromString](#fromstring)
  - [fromStringWithRadix](#fromstringwithradix)
  - [increment](#increment)
  - [isValid](#isvalid)
  - [mod](#mod)
  - [multiply](#multiply)
  - [negate](#negate)
  - [rem](#rem)
  - [subtract](#subtract)

---

# utils

## add

Add two numbers together.

**Signature**

```ts
export declare const add: (x: number) => Endomorphism<number>
```

```hs
add :: number -> Endomorphism number
```

**Example**

```ts
import { add } from 'fp-ts-std/Number'

assert.strictEqual(add(2)(3), 5)
```

Added in v0.1.0

## decrement

Decrement a number.

**Signature**

```ts
export declare const decrement: Endomorphism<number>
```

```hs
decrement :: Endomorphism number
```

**Example**

```ts
import { decrement } from 'fp-ts-std/Number'

assert.strictEqual(decrement(3), 2)
```

Added in v0.1.0

## divide

Divide the second number (the _dividend_) by the first number (the
_divisor_).

**Signature**

```ts
export declare const divide: (divisor: number) => Endomorphism<number>
```

```hs
divide :: number -> Endomorphism number
```

**Example**

```ts
import { divide } from 'fp-ts-std/Number'

assert.strictEqual(divide(2)(4), 2)
assert.strictEqual(divide(4)(2), 0.5)
```

Added in v0.2.0

## floatFromString

Convert a string to a floating point number.

**Signature**

```ts
export declare const floatFromString: (x: string) => Option<number>
```

```hs
floatFromString :: string -> Option number
```

**Example**

```ts
import { floatFromString } from 'fp-ts-std/Number'
import { some, none } from 'fp-ts/Option'

assert.deepStrictEqual(floatFromString('3.3'), some(3.3))
assert.deepStrictEqual(floatFromString('abc'), none)
```

Added in v0.1.0

## fromString

Convert a string to a number.

**Signature**

```ts
export declare const fromString: (string: string) => Option<number>
```

```hs
fromString :: string -> Option number
```

**Example**

```ts
import { fromString } from 'fp-ts-std/Number'
import { some, none } from 'fp-ts/Option'

assert.deepStrictEqual(fromString('3'), some(3))
assert.deepStrictEqual(fromString('abc'), none)
```

Added in v0.1.0

## fromStringWithRadix

Convert a string to a number.

**Signature**

```ts
export declare const fromStringWithRadix: (radix: number) => (string: string) => Option<number>
```

```hs
fromStringWithRadix :: number -> string -> Option number
```

**Example**

```ts
import { fromStringWithRadix } from 'fp-ts-std/Number'
import { some, none } from 'fp-ts/Option'

assert.deepStrictEqual(fromStringWithRadix(16)('0xF'), some(15))
assert.deepStrictEqual(fromStringWithRadix(16)('xyz'), none)
```

Added in v0.1.0

## increment

Increment a number.

**Signature**

```ts
export declare const increment: Endomorphism<number>
```

```hs
increment :: Endomorphism number
```

**Example**

```ts
import { increment } from 'fp-ts-std/Number'

assert.strictEqual(increment(3), 4)
```

Added in v0.1.0

## isValid

Check if a number is actually valid. Specifically, all this function is
doing is checking whether or not the number is `NaN`.

**Signature**

```ts
export declare const isValid: Predicate<number>
```

```hs
isValid :: Predicate number
```

**Example**

```ts
import { isValid } from 'fp-ts-std/Number'

const valid = 123
const invalid = NaN

assert.strictEqual(isValid(valid), true)
assert.strictEqual(isValid(invalid), false)
```

Added in v0.7.0

## mod

Calculate the modulus. See also `rem`.

**Signature**

```ts
export declare const mod: (divisor: number) => Endomorphism<number>
```

```hs
mod :: number -> Endomorphism number
```

**Example**

```ts
import { mod } from 'fp-ts-std/Number'

assert.strictEqual(mod(2)(5.5), 1.5)
assert.strictEqual(mod(-4)(2), -2)
assert.strictEqual(mod(5)(-12), 3)
```

Added in v0.7.0

## multiply

Multiply two numbers together.

**Signature**

```ts
export declare const multiply: (x: number) => Endomorphism<number>
```

```hs
multiply :: number -> Endomorphism number
```

**Example**

```ts
import { multiply } from 'fp-ts-std/Number'

assert.strictEqual(multiply(2)(3), 6)
```

Added in v0.2.0

## negate

Unary negation.

**Signature**

```ts
export declare const negate: Endomorphism<number>
```

```hs
negate :: Endomorphism number
```

**Example**

```ts
import { negate } from 'fp-ts-std/Number'

assert.strictEqual(negate(42), -42)
assert.strictEqual(negate(-42), 42)
```

Added in v0.7.0

## rem

Calculates the remainder. See also `mod`.

**Signature**

```ts
export declare const rem: (divisor: number) => Endomorphism<number>
```

```hs
rem :: number -> Endomorphism number
```

**Example**

```ts
import { rem } from 'fp-ts-std/Number'

assert.strictEqual(rem(2)(5.5), 1.5)
assert.strictEqual(rem(-4)(2), 2)
assert.strictEqual(rem(5)(-12), -2)
```

Added in v0.7.0

## subtract

Subtract the first number (the _subtrahend_) from the second number (the
_minuend_).

**Signature**

```ts
export declare const subtract: (subtrahend: number) => Endomorphism<number>
```

```hs
subtract :: number -> Endomorphism number
```

**Example**

```ts
import { subtract } from 'fp-ts-std/Number'

assert.strictEqual(subtract(2)(3), 1)
assert.strictEqual(subtract(3)(2), -1)
```

Added in v0.2.0
