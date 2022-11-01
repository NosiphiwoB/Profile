---
Layout:
Title: " Quality Assurance "
Date: "2022 10 31"
---

# Introduction
Today I started with Quality Assurance.In quality assurance we learn how to write tests with Chai to ensure your applications work the way you expect them to.Then you'll build a chat application to learn advanced Node and Express concepts. You'll also use Pug as a template engine, Passport for authentication, and Socket.io for real-time communication between the server and connected clients.

# Body
Quality Assurance and Testing with Chai -- Chai is a JavaScript testing library that helps you confirm that your program still behaves the way you expect it to after you make changes to your code.Using Chai, you can write tests that describe your program's requirements and see if your program meets them.


Use Assert.isOK and Assert.isNotOK -- isOk() will test for a truthy value, and isNotOk() will test for a falsy value.

e.g test('#isOk, #isNotOk', function () {

      assert.isNotOk(null, 'null is falsey');

      assert.isOk("I'm truthy", 'A string is truthy');

      assert.isOk(true, 'true is truthy');

    });


Test for Truthiness -- isTrue() will test for the boolean value true and isNotTrue() will pass when given anything but the boolean value of true.

e.g assert.isTrue(true, 'This will pass with the boolean value true');

    assert.isTrue('true', 'This will NOT pass with the string value "true"');

    assert.isTrue(1, 'This will NOT pass with the number value 1');


isFalse() and isNotFalse() also exist, and behave similarly to their true counterparts except they look for the boolean value of false.

e.g test('#isTrue, #isNotTrue', function () {

      assert.isTrue(true, 'true is true');

      assert.isTrue(!!'double negation', 'Double negation of a truthy value is true');

      assert.isNotTrue({ value: 'truthy' }, 'Objects are truthy, but are not boolean values');

    });


Use the Double Equals to Assert Equality -- equal() compares objects using == .

e.g test('#equal, #notEqual', function () {

      assert.equal(12, '12', 'Numbers are coerced into strings with ==');

      assert.notEqual({ value: 1 }, { value: 1 }, '== compares object references');

      assert.equal(6 * '2', '12');

      assert.notEqual(6 + '2', '12');

    });


Use the Triple Equals to Assert Strict Equality -- strictEqual() compares objects using === .

e.g test('#strictEqual, #notStrictEqual', function () {

      assert.notStrictEqual(6, '6');

      assert.strictEqual(6, 3 * 2);

      assert.strictEqual(6 * '2', 12);

      assert.notStrictEqual([1, 'a', {}], [1, 'a', {}]);

    });


Assert Deep Equality with .deepEqual and .notDeepEqual -- deepEqual() asserts that two objects are deep equal.

e.g test('#deepEqual, #notDeepEqual', function () {

      assert.deepEqual({ a: '1', b: 5 }, { b: 5, a: '1' }, "The order of keys doesn't matter");

      assert.notDeepEqual({ a: [5, 6] }, { a: [6, 5] }, 'The order of array elements does matter');

    });


Compare the Properties of Two Elements -- We compare the Properties of two elements with isAbove() and isAtMost() 

e.g  test('#isAbove, #isAtMost', function () {

      assert.isAtMost('hello'.length, 5);

      assert.isAbove(1, 0);

      assert.isAbove(Math.PI, 3);

      assert.isAtMost(1 - Math.random(), 1);

    });


Test if One Value is Below or At Least as Large as Another -- we can test that using isBelow() and isAtLeast() .

e.g  test('#isBelow, #isAtLeast', function () {

      assert.isAtLeast('world'.length, 5);

      assert.isAtLeast(2 * Math.random(), 0);

      assert.isBelow(5 % 2, 2);

      assert.isBelow(2 / 3, 1);

    });


Test if a Value Falls within a Specific Range -- We use approximately()

e.g  test('#approximately', function () {

      assert.approximately(weirdNumbers(0.5), 1, 0.5);

      assert.approximately(weirdNumbers(0.2), 1, 0.8);

    });
    

# Conclusion
So far I don't have any issues ,I am going to continue with Quality Assurance.