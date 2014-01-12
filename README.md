# Micro

### Description

A tiny template engine, with javascript execution isolation.

### Purpose

Just for fun.

### Usage API

#### Calling the module

  - var micro = require('micro');

#### Definition

  - var content = micro('{{ message }}');

#### Compile

  - content.compile({ message: 'Hello World!' });
  - // Hello World!

#### Run

  - var content = micro('{{ var result = firstValue + secondValue; }}');
  - content.run({ 
  -   firstValue: 2, 
  -   secondValue: 3 
  - });

  - // { 
  - //    firstValue: 2, 
  - //    secondValue: 3, 
  - //    result: 5, 
  - //    _compiled: "var result = 2 + 3;" 
  - // } 

#### Render

  - var content = micro('{{ var result = firstValue + secondValue; }}');
  - content.render({ 
  -   firstValue: 2, 
  -   secondValue: 3 
  - }, '{{result, firstValue, secondValue}}');

  - //5, 2, 3

### License

Under BSD
