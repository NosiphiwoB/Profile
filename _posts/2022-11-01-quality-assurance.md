---
Layout:
Title: " Quality Assurance "
Date: "2022 11 01"
---

# Introduction
Today I was busy with Quality Assurance.

# Body
Test if a value is an Array -- we test if a value is an array using isArray() and isNotArray() 

e.g test('#isArray, #isNotArray', function () {

      assert.isArray('isThisAnArray?'.split(''), 'String.prototype.split() returns an array');

      assert.isNotArray([1, 2, 3].indexOf(2), 'indexOf returns a number');

    });


Test if an Array contains an item -- We test using include() and notInclude() 

e.g test('Array #include, #notInclude', function () {

      assert.notInclude(winterMonths, 'jul', "It's summer in july...");

      assert.include(backendLanguages, 'javascript', 'JS is a backend language');

    });


Test if a value is a string -- isString() or isNotString() asserts that the actual value is a string.

e.g test('#isString, #isNotString', function () {

      assert.isNotString(Math.sin(Math.PI / 4), 'A float is not a string');

      assert.isString(process.env.PATH, 'An env variable is a string (or undefined)');

      assert.isString(JSON.stringify({ type: 'object' }), 'JSON is a string');

    });


Test if a string contains a substring -- include() and notInclude() works for strings too.include() asserts that the actual string contains the expected substring.

e.g test('String #include, #notInclude', function () {

      assert.include('Arrow', 'row', "'Arrow' contains 'row'");

      assert.notInclude('dart', 'queue', "But 'dart' doesn't contain 'queue'");

    });
    
    
Use regular expression to test a string -- match asserts that the actual value matches the second argument regular expression .

e.g test('#match, #notMatch', function () {

      const regex = /^#\sname\:\s[\w\s]+,\sage\:\s\d+\s?$/;

      assert.match(formatPeople('John Doe', 35), regex);

      assert.notMatch(formatPeople('Paul Smith III', 'twenty-four'), regex);

    });
    
    
Test if an object has a property -- property asserts that the actual object has a given property.

e.g test('#property, #notProperty', function () {

      assert.notProperty(myCar, 'wings', "Cars don't have wings");

      assert.property(airlinePlane, 'engines', 'Planes have engines');

      assert.property(myCar, 'wheels', 'Cars have wheels');

    });

# Conclusion
I am going to continue with Quality assurance and do some mongodb and mongoose projects .