---
Layout:
Title: " Quality and Assurance"
Date: "2022 11 08"
---

# Introduction
Today I was busy with quality assurance and testing with chai.

# Body
Test if a Value is of a Specific Data Structure Type -- typeOf asserts that value's type is the given string, as determined by Object.prototype.toString.

e.g test('#typeOf, #notTypeOf', function () {

      assert.typeOf(myCar, 'object');

      assert.typeOf(myCar.model, 'string');

      assert.notTypeOf(airlinePlane.wings, 'string');

      assert.typeOf(airlinePlane.engines, 'array');

      assert.typeOf(myCar.wheels, 'number');

    });


Test if an object is an instance of a constructor -- instanceOf() asserts that an object is an instance of a constructor

e.g test('#instanceOf, #notInstanceOf', function () {

      assert.notInstanceOf(myCar, Plane);

      assert.instanceOf(airlinePlane, Plane);

      assert.instanceOf(airlinePlane, Object);

      assert.notInstanceOf(myCar.wheels, String);

    });

Run Functional Tests on API Endpoints using Chai-HTTP -- Mocha allows you to test asynchronous operations like calls to API endpoints with a plugin called chai-http.Here is an example of testing using chai-http for a suite called 'GET /hello?name=[name] => "hello [name]"':

suite('GET /hello?name=[name] => "hello [name]"', function () {

  test('?name=John', function (done) {

    chai

      .request(server)

      .get('/hello?name=John')

      .end(function (err, res) {

        assert.equal(res.status, 200, 'Response status 
        
        should be 200');

        assert.equal(res.text, 'hello John', 'Response 
        
        should be "hello John"');

        done();

      });

  });

});

The test sends a GET request to the server with a name as a URL query string (?name=John). In the end method's callback function, the response object (res) is received and contains the status property.
The first assert.equal checks if the status is equal to 200. The second assert.equal checks that the response string (res.text) is equal to "hello John".
Also, notice the done parameter in the test's callback function. Calling it without an argument at the end of a test is necessary to signal that the asynchronous operation is complete.

e.g Within tests/2_functional-tests.js, alter the 'Test GET /hello with no name' test (// #1) to assert the status and the text of the response to make the test pass. Do not alter the arguments passed to the asserts.There should be no URL query. Without a name URL query, the endpoint responds with hello Guest:

 test('Test GET /hello with no name', function (done) {

      chai

        .request(server)

        .get('/hello')

        .end(function (err, res) {

          assert.equal(res.status, 200);

          assert.equal(res.text, 'hello Guest');

          done();

        });

    });


# Conclusion
I am going to continue with quality assurance .