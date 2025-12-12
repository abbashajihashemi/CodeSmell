# CodeSmell


## Bloaters

### 1) LongMethod

** Signs :
   - A method contains too many lines of code. Generally, any method longer than ten lines should make you start asking questions.
   - It’s easier to write code than to read it.
   - You feel the need to comment on something inside a method.

  <img width="681" height="340" alt="image" src="https://github.com/user-attachments/assets/7eeb165c-8df0-4ba1-aad4-82b1c58f094e" />


** Solutions :
   - To reduce the length of a method body, use Extract Method.
  <img width="952" height="245" alt="image" src="https://github.com/user-attachments/assets/bf3aa28f-ea04-46c1-bcee-e526d52031f9" />


### 2) Large Class

** Signs:
   - A class contains many fields/methods/lines of code.
   - Classes usually start small. But over time, they get bloated as the program grows.


** Solutions:
   - Extract Class: helps if part of the behavior of the large class can be spun off into a separate component.
   - Extract Subclass: helps if part of the behavior of the large class can be implemented in different ways or is used in rare cases.
   - Extract Interface: helps if it’s necessary to have a list of the operations and behaviors that the client can use.


   #### Extract Class
<img width="200" alt="image" src="https://github.com/user-attachments/assets/38b14c4d-cf0f-476e-8382-1a38b749713b" />
<img width="500" height="267" alt="image" src="https://github.com/user-attachments/assets/630f8094-f67d-4930-b19c-c7c8a841cb5e" />


Benfit: Single Responsibilty

Drawbacks: If you “overdo it” with this refactoring technique, you will have to resort to Inline Class.

### 3) Primitive Obsession

   - Use of primitives instead of small objects for simple tasks (such as currency, ranges, special strings for phone numbers, etc.)
   - Use of constants for coding information (such as a constant USER_ADMIN_ROLE = 1 for referring to users with administrator rights.)
   - Use of string constants as field names for use in data arrays.


