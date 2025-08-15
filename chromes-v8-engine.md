# JavaScript Engine
1. JavaScript code we write cannot be understood by the computer.
2. A JavaScript engine is a program that converts javascript code that developers write into machine code that allows a computer to perform specific tasks.
3. JavaScript engines are typically developed by web browser vendors:
    - V8 — Open-source JavaScript Engine developed by Google for Chrome
    - SpiderMonkey — The JavaScript Engine powering Mozilla Firefox
    - JavaScriptCore — Open-source JavaScript Engine developed by Apple for Safari
    - Chakra — A JavaScript Engine for the original Microsoft Edge (The latest version of edge uses V8).

# V8 JavaScript Engine
1. V8 is Google's open source JavaScript engine.
2. V8 implements ECMAScript as specified in ECMA-262.
3. V8 is written in C++ and is used in Google Chrome, the open source browser from Google.
4. V8 can run standalone, or can be embedded into any C++ application.
5. V8 Project page: https://v8.dev/docs

# Chrome's V8 Engine & Node.js
1. Chrome's V8 engine by Google sits at the core of Node.js
2. By embedding V8 into your own C++ application, you can write C++ code that gets executed when a user writes JavaScript code
3. You can add new features to JavaScript itself Since C++ is great for lower level operations like file handling, database connections and network operations, by embedding V8 into your own C++ program, you have the power to add all of that functionality in JavaScript.
4. The C++ program we're talking about is Node.js*

( * Node.js is a lot more than just a C++ program)
