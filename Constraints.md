## Four elements of simple design

1. Passes its tests
2. Minimizes duplication (of concepts) - DRY
3. Maximizes clarity (revealing intent) - Naming!
4. Has fewer elements (exactly what you need) - Small

## Constraints

### Quality Code Constraints

- Max 4 statements per method
- No naked primitives (includes Arrays)
- No predefined data structures
- No conditionals
- No loops
- Immutable code / Pure functions
- Void functions (including getters)

---

### Missing Tools Constraints

1. No Mouse
2. Ball & Board (Driver has keyboard, Navigator has mouse)
3. Text editor only
4. Pen and paper
5. Don’t build until the end

---

### Testing Constraints

#### 1. TDD as if you Meant It

1. Write one failing test
2. Make it pass by writing implementation code in the test function
3. When duplication is spotted extract implementation from tests to:
   - a new field in the test class
   - a new function in the test class
   - an existing function in the test class
4. When more functions belong together extract them into a new class
5. Refactor as required

#### 2. Baby steps

1. Setup a timer for 5 (or lesser) minutes interval when you start.
2. Write exactly one test. When the timer rings:
   - if test is red then delete and start over.
   - if the test is green then continue.
3. Restart timer (no discussions in between timers)
4. Refactor. If the:
   - timer rings and the refactoring is not complete then delete and start over.
   - refactoring is complete before the timer rings then continue.
5. Restart the timer (no discussions in between timers)
6. Go to 3.

This can also be done using git to commit/revert the changes

---

### Pairing Constraints

#### 3. Ping-Pong

1. One person starts writing a test
2. Switch the keyboard to the second person
3. The second person becomes driver and implements the first test
4. The second person writes a test
5. The first person implements the code
6. The first person writes a test ...

#### 4. Pomodoro/Timed Ping-Pong

- Same as Ping-Pong but change roles every 5 (or lesser) mins

#### 5. Evil Ping-Pong / Evil Coder

- Same as Ping-Pong but The driver must implement the test in an evil way, not following the intention of the test

#### 6. Silent/Mute Ping-Pong

- You are not allowed to talk with your pair
- No discussion (comments in code, on paper etc) is allowed

#### 7. Yes, and...

- You are not allowed to delete code
- Any change in the existing code is made by Refactoring, Adding the existing code

The intention is to be able to say “Even if I don’t agree with this code, **Yes** I accept it **and** I can improve it by ....”

#### 8. Beginner’s Mind

- The driver writes code.
- The navigator keeps asking questions like a beginner like why did you write this method, do you need this, how will this work, etc
- The driver needs to explain all the decisions
- Switch roles

#### 9. Blind pairing

- Driver is blind, Navigator cannot touch the keyboard

---

### Miscellaneous

#### 10. Focus on Refactoring

- Use naming that reveals intent
- Rename concepts to improve naming (use domain language)
- Extract duplicate identical chunks of code
- Extract methods having the same noun into their class
- Split methods containing Or, And in their names

#### 11. A Developer in Test

1. Don’t delete the code from the previous session except the existing tests
2. Swap the code in-between pairs
3. Your job now is to write software that tests the code.
4. You are not allowed to change the existing code

---

### Mix n match (Advanced)

#### 12. Single Responsibility Principle

- No conditionals
- No try/catch
- Exactly one assert per test
- Test one behaviour per test

#### 13. Code in the Dark

- You are allowed to use only a basic text editor
- You are not allowed to compile the code until the end of the session
- No autocomplete allowed
- At the end of the session compile and see if you have errors

#### 14. Design Patterns Only

- You are not allowed to add anything without being related to a design pattern.
- All the classes, functions, methods need to contain a commentary with the design pattern that generated the use of that structure.

#### 15. Event Driven Only

- All the connections between structures are done with events

#### 16. NOOOP (Not only Object Oriented Programming)

- All the types are boxed (not primitives)
- Functions and not classes
- Write only pure functions
- No nullables
- Do not use a functional language

#### 17. Object Calisthenics

    Object Calisthenics are programming exercises, formalized as a set of 9 rules invented by Jeff Bay in his book The ThoughtWorks Anthology

- Only one level of indentation per method
- Don’t use the else keyword
- Wrap all primitives and strings
- First class collections
- One dot per line
- Don’t abbreviate
- Keep all entities small
- No classes with more than two instance variables
- No getters/setters/properties

#### 18. Any other combinations

- Mute Ping-Pong + Evil Coder etc
- Whole > Sum of parts (All constraints from the previous sessions apply)

---
