# How JavaScript Code is executed? & Call Stack

### What happens when you run JavaScript Code?

- When you run a JavaScript program, there are a lot of things happening behind the scenes inside the JavaScript engine.
- We'll be covering everything right now. Just keep watching Namaste JavaScript.
- Remember in the last video, we discussed that everything in JavaScript happens inside an execution context. Remember?
- And JavaScript isn't possible without this beautiful execution context.
- So here's one question for you. So what happens when you run a JavaScript program?
- Yes, you're right.
- An execution context is created.

### Code Example for Execution Context Creation

- So let us now see how this beautiful execution context is created with the help of a JavaScript program.
- So we have this variable `n` which is two and there's a function `square` which returns the square of a number that is being passed inside this function.
- And there are two other variables `square2` and `square4` which are just invoking this already created function.
- So now let us see how this whole JavaScript code is run behind the scenes.
- So when you run this whole code, a global execution context is created.

### Global Execution Context Creation

- Let us create this execution context.
- So remember we told that it's like a big box and it has two components, okay?
- These two components are the memory component and the code component.

### Memory Allocation Phase & Code Execution Phase

- Now listen to this very carefully. This execution context is created in two phases.
- So the first phase is also known as the creation phase. Remember this. This is also known as the memory creation phase. Okay. So this is a very critical phase. Okay. Memory creation phase.
- Let us see how this phase is done. And then afterwards the second phase, which is the code execution phase. Okay. So let us first see the first phase.
- So if we have this code.

  - in the first phase of memory creation, javascript will allocate memory to all the variables and functions.
  - As soon as javascript encounters this line 1, it allocates memory to N.
  - So let us now allocate the memory to N. How will it allocate? It will reserve a memory space here for N.
  - So similarly, now the javascript goes to the line 2, so in this it sees that there is also a function which is named as square.
  - So it will allocate memory to square.
  - Okay, so now it allocates some memory to square. Here, like this.
  - In this, it stores a spatial value which is known as undefined.
  - And in case of functions, it literally stores the whole code of the function inside this memory space.
  - So in the first phase,

  - And in case of functions, functions are very beautiful.
  - So in case of functions, this function square, this whole function code is like literally, you can assume it to be copied over here in the memory space.
  - And now it will also allocate memory to square 2 and square 4.
  - and as they are another variable, so it will again store undefined for them.
  - undefined.

  - It's a bit tricky, let me give you a quick recap.
  - So in the first phase, the JavaScript skims through the whole program, line by line, and it allocates memory to all the variables and functions.
  - As soon as it encounters n, so it reserves memory for it, and allocates a special value undefined to it.
  - Okay, remember this value undefined, we'll be talking a lot about this in a... I'll make a separate video altogether for undefined, but for now just understand, undefined is placed over here.
  - It's like a placeholder, it's a special keyword in JavaScript.
  - And in case of functions, functions are very beautiful.
  - So in case of functions, this function square, this whole function code is like literally, you can assume it to be copied over here in the memory space.
  - Okay, so that's how it is.
  - And for the remaining two, remaining two variable, it again allocates memory and stores this special keyword undefined to them.

  - in the first phase. Let us now see what happens in the phase two.
  - The second phase is the code execution phase. Okay, it is the code execution phase.
  - So let's see how this code is now executed after the memory allocation.
  - So now JavaScript once again runs through this whole JavaScript program line by line and it executes the code now.
  - This is the point when all these functions and every calculation in the program is done.

  - So as soon as it encounters this first line where n is equals to 2, it actually places the 2 inside the n.
  - So till now the value of n was undefined.
  - Now in the second phase of creation of execution context, that is the code execution phase, in this phase, this 2 value over here of n is now being placed actually in this placeholder or the identifier which is n.
  - So now this 2 in the second phase is now allocated here.
  - So let me just remove this undefined for a while.
  - And now replace this with the spatial value which we got 2.
  - And this is in the phase 2. Remember this carefully. After finishing line 1, it goes to line 2 and sees that we have nothing to do here. So line number 2 to 5, there is nothing to execute literally. So it then moves to the line number 6.

### Function Invocation and Execution Context Creation

- So line number 6 is the most amazing part. Here we invoke a function. Here's a function invocation. What do you mean by a function invocation? Whenever you see a function name with these parentheses, with these round brackets, it means that the function is now being executed.
- Functions are the heart of JavaScript, and you know, they behave very differently in JavaScript than any other language. Okay, so functions over here are like a mini program.
- And whenever a new function is invoked, you know, a mini program is invoked, altogether new execution context is created.
- Remember that whole thing, what we were running this whole program was inside the global execution context. Now, when you run a function or when you invoke a function, this function, a brand new execution context is created.
- OK, so let us see. This is going to be interesting. Just keep following. So here.

  - brand new execution context inside this is created. Okay.
  - Now let us see, and this execution context again has these two components, which is the memory component. Okay. And a code component. Got it.
  - So now we will again go through the creation of this execution context, and there will again be two phases involved. Remember, what were these two phases? So let us see it. It will be interesting.

- #### Memory Allocation Phase for Function Execution Context

  - So the first phase is the memory creation phase. Remember memory creation phase. Okay in the memory creation phase now we are talking about this function invocation. Okay so we'll be concerned about this piece of code only when we are executing this square n. So we are only concerned about this piece of code. Remember so now let us see how the memory is allocated here in the first phase. The phase one. Okay.

    - So in the phase 1, first of all, don't forget that the memory is allocated to variables and functions inside this function. Okay, so and when I say variables and functions, it involves the parameters like the num and the other variables and we don't have a function, so no need.
    - So we will be allocating memory to num. Okay.
    - So here is num and we will also allocate memory to ans. Ans.
    - Okay. So now what will happen is, remember what will be stored in this, the special placeholder which we had? Yes, you are right. We will be storing undefined in the phase 1.
    - You know, you will understand this concept of undefined very better just following along in these upcoming videos. Okay. For now, just keep in mind that this.

  - Undefined is a very special keyword. We will be covering this in detail later on in the videos. Okay, so keep on so we'll be putting undefined over here and undefined is being allocated in the phase one.
  - Now comes the part of phase two. Okay, so the phase two is the code execution phase. Remember code execution in this we will be executing each line. Okay, we'll be executing each line here.
  - So what happens when you execute the code? So when this function is invoked, first of all this value of n over here which is 2 is passed to num.
  - So num over here is known as the parameter of the function.
  - n over here is the argument. So this is the argument and the value of n is 2 right now.
  - So remember over here the value of n is 2 which will come over here in place of undefined.
  - So let us put the value 2 in num and the code will then move to the next line. So now we have moved to this line, line number 3.

  - So in the line number 3, it will do the calculation and put the value of num into num inside ans.
  - It's like executing the code inside this code block. num into num and whatever the value will be there will now go to this and undefined will be replaced by num into num and the value.
  - So num into num which is 4, like 2 into 2 which is 4, will now replace this undefined and will take up place in this memory space.
  - So the ANS will now become 4. Got it? So that is how the code will be executed. And now this, let me just remove it.

### What happens while executing return statement

- So now after finishing line number three, the control goes to line number four. Here we encounter the special keyword return and ans.
- So whenever you see a return and ans, so this return keyword tells this function then you are done with your work now just return the whole control back to the execution context where the function was invoked.
- So remember this is very important. Okay so this return keyword states that

  - Now return the control of the program to the place where this function was invoked.
  - So where the function was invoked? Function was invoked here. So return the value of ans to the place where it was the control.
  - Now the control goes here. Okay to line number 6 again. How does that happen? Let me tell you.

- #### Execution of Return Statement

  - Now as soon as we encounter this return statement, we have this return of ANS So it finds the value of ANS inside this local memory So so this is known as the local memory.
  - So local memory has four so this return ANS now returns the control back over here and Okay in the line number six and this value of ANS which was here four is now Replace will now replace undefined of this square two
  - Got it? So this is how we are slowly executing the code.
  - So the value will become 4 now. Okay, so 4 will be stored over here.
  - Got it? One more thing which happens when the whole function is executed is that this whole execution context for that instance of that function will be deleted.
  - Okay, so that means that this whole execution context will now be completely deleted. So now there won't be the execution context as soon as we return the value. So this whole thing will be deleted.
  - and the control moves to line number 6. After this replacement, so now we will go to line number 7.

- #### Invocation of Another Function

  - So in line number 7, we are again invoking a function, and just the difference is we are now passing in 4 over here as an argument directly. That's it. Nothing will change.
  - Similarly, what will happen now? As soon as this function invocation happens, so again, a brand new execution context will be created. So let us create one.
  - Quickly and see how things are working. So the brand new execution context is created.
  - So here we create and apologies for this drawing. I'm not very good at drawing. So this execution context is created.
  - Again, it will have this memory. Again, it will have a code component. Remember?
  - and now it will again go through those two phases. Let's quickly do that, it will be fun.

- #### Memory Allocation Phase for Another Function Execution Context

  - So now again it goes back to this function here. So this function now remember what happens? The firstly the memory is allocated to num and num will store the value undefined. Remember?
  - So let me zoom it. Undefined. And one more thing happens is we allocate memory to ans. which is again undefined.
  - Right so so our first phase is done so now in the second phase so in the code execution phase now what will happen is num will get this argument from the invocation right here from the line number seven num will get this value four so num parameter will get the argument four so here the argument is four okay so what will happen is now
  - in the code execution this undefined will be replaced by in the code execution phase the undefined will be replaced by 4 right so it will be 4 right and what will happen after that it will go to line number 3 right so while invocation it will go to line number 3 it will execute num into num which is 4 into 4 16 and the 16 will now replace this undefined
  - value inside the ans right so we will now replace this with 16 got it so now it will store 16 and the control moves to line number four after three is done so now this return statement takes back the control to the line number seven where the function was actually invoked and now the value 16 will replace undefined in the square four variable okay so let us do that

- #### Deletion of Execution Context

  - Let us quickly do that. It will now get the value 16 over here. As soon as we are done with the function execution, this whole execution context is now deleted.
  - So this will be deleted. So now the line number 7 is also executed. Now there is nothing more. So JavaScript is done with all its work. So once JavaScript is done with all its work, now the program is finished.
  - So what will happen is the whole global execution context also deletes. It goes off. Okay, so that is how the whole code is executed.

### Recap of Code Execution synchronously

- I know this was all a lot and it will take some time to digest, but quickly just revise everything. Once again, it will be super fun.
- Okay, just quickly, very quickly I will revise everything. So as soon as the whole JavaScript program is run, so the execution context is created. Remember, the global execution context is created.
- It has two components memory code as you know and it is created in two phases. So the phase one remember what was it? The phase one was the memory creation phase.
- In the memory creation phase, we were allocating memory to all the variables and functions inside the global space. So inside this whole program. We are allocating this memory and what we allocated these variables with? We allocated these variables with undefined.
- And in case of functions, we just copied, literally it stores the whole function. The code of the whole function inside the memory space. So that is the first phase.
- Now in the second phase, the code execution phase, now the JavaScript program is executed line by line. It goes over here, it sees that 2 is here, so it replaces undefined with 2.
- and similarly it will now invoke the function, the control goes to line number 6 it will invoke the function and it will invoke the another function so when you invoke this function execution context is created again there are two phases, the memory allocation phase, num and ans are allocated memory and in the code execution phase

- #### Execution of Function and Return Statement

  - again this whole thing is run the ans num into num is executed and this num into num is now stored in ans and return statement is executed in the return statement we take back the control over here to square 2 and now the square 2 is populated with a new value which is coming from this function invocation which was the ans and ans was 4 so square 2 was 4.
  - So similarly it will again be it will again happen here in the in this function execution
  - So a new execution context is created and again the same thing cycle repeats and that's how this function returns 16 over here and square 4 is 16.

- #### Handling Nested Function Invocations

  - So that is how the whole thing works. But don't you think that all this is too much to manage for JavaScript engine? Like I mean execution context is created one by one inside one and all these things are very tough to manage right. And suppose if there was a function invocation inside the function.
  - So what would have happened is, so you would have created an execution context inside an execution context over here and maybe again an invocation. So it can go to any deep level right function invocation inside that again function invocation and all these things.

### Call Stack in JavaScript

- So it is very difficult for JavaScript engine to manage and it does it very beautifully. So let me tell you how it does it. This is the last part of this video. So.

  - It handles everything to manage this execution context, creation, deletion and the control. It manages a stack. So this is known as the call stack. This is the beautiful thing in JavaScript. It has its own call stack. So let me show you call stack. So what is a call stack now? Let me show you.
  - So the call stack is like a stack. So it is a stack.
  - we have our global execution context. That means whenever any JavaScript program is run, this call stack is populated with this global execution context. This whole execution context is pushed inside this stack. Okay, remember this?
  - And when a function is invoked, whenever a function is invoked or a new execution context is created, as in case here in line number six,

- #### Handling Function Execution in Call Stack

  - we created this execution context. So this execution context is put inside the stack. So let me just denote it by even which is the execution context one. Okay. So this is the this is this is how it happens. Once we are done with execution this function we returned the ANS.
  - So what happened now this even is moved out. Okay. So even is popped out of the stack and the control goes back to the global execution context where it left. So the control goes back over here in line number six.
  - got it? this is how it works so this will again literally just pop off even out of the stack so now even will be popped off the stack and then we moved on to line number 7 where the new function was invoked and a new execution context was created and similarly this E2 will move up to the stack this E2 was popped inside the stack
  - and once the whole function was executed, then E2 will also move out of stack and the control goes back to global execution context, something like this, okay?
  - So this is, so this stack, call stack is only for managing these execution contexts. So whenever an execution context is created, it is pushed into the stack and whenever an execution context is deleted, it will move out of the stack.
  - So that is how the whole control is being managed. This whole execution context creation, deletion, everything is managed by JavaScript. And finally, after this whole thing is executed, the call stack gets empty. The call stack, the global execution context also is gone from this call stack and we are done with our JavaScript program. So that is how the whole code inside the JavaScript engine is executed.

### Other names of the Call Stack in JS

- So with this, let me take you to another core concept, which is call stack maintains the order of execution of execution context.
- Now, I'll tell you one more interesting thing that call stack is also known by a very fancy names. Okay, there are a lot of fancy names which you will see on the web. That is why JavaScript is the most confusing language. Okay, it is the most misunderstood language.
- So call stack is also known as execution context stack sometimes. It is also known as program stack, control stack, runtime stack, machine stack.
- All various names are used for this call stack, but it is all the same thing. This beautiful call stack, which will just maintain the order of execution of the execution context.
