# fuzzy-octo-funicular
											TESTING IN ANGULAR(to prevent software defects)
											
-> writing test cases in Jasmine and run it using Karma
-> Protractor does this both the things

=> Jasmine :  is a behavior-driven development framework for testing JavaScript code.
             It does not depend on any other JavaScript frameworks. It does not require a DOM. 
             And it has a clean, obvious syntax so that you can easily write tests.
			 Jasmine, and BDD in general, attempts to describe tests in a human readable format 
			 so that non-technical people can understand what is being tested. However even if you are
			 technical reading tests in BDD format makes it a lot easier to understand what’s going on.
			 
		Example:
					For example if we wanted to test this function: 

							TypeScript
							function helloWorld() {
							  return 'Hello world!';
							}
							We would write a jasmine test spec like so:

							TypeScript
							describe('Hello world', () => { (1)
							  it('says hello', () => { (2)
								expect(helloWorld()) (3)
									.toEqual('Hello world!'); (4)
							  });
							}); 
							
			The describe(string, function) function defines what we call a Test Suite, a collection of individual Test Specs.
			The it(string, function) function defines an individual Test Spec, this contains one or more Test Expectations.
			The expect(actual) expression is what we call an Expectation. In conjunction with a Matcher it describes an expected piece of behaviour in the application.
			The matcher(expected) expression is what we call a Matcher. It does a boolean comparison with the expected value passed in vs. the actual value passed to the
			expect function, if they are false the spec fails.
			
	=> Karma : Manually running Jasmine tests by refreshing a browser tab repeatedly in different browsers every-time we edit some code can become tiresome.
               Karma is a tool which lets us spawn browsers and run jasmine tests inside of them all from the command line. The results of the tests are also
			   displayed on the command line.
               Karma can also watch your development files for changes and re-run the tests automatically.
               Karma lets us run jasmine tests as part of a development tool chain which requires tests to be runnable and results inspectable via the command line.
			   Karma is essentially a tool for testing which spawns(Spawn in computing refers to a function that loads and executes a new child process.) a web server
			   that executes source code against test code for each of the browsers connected.