# Generate unit tests for the provided function or class method.

## 1. Write Clear and Concise Tests

- Each unit test should focus on a single functionality or behavior.
  - Clear, concise unit tests are easier to understand, maintain, and debug.
  - Use descriptive test names that clearly indicate the purpose of the test.
  - This helps other developers quickly understand what the test is verifying.
  - Follow a consistent naming convention for tests starting with `should`.

## 2. Follow the AAA Pattern (Arrange, Act, Assert)

- The "AAA Pattern" approach increases maintainability and clarity in your tests and includes breaking each test into organized parts:
  1. **Arrange:** Set up the necessary preconditions and inputs.
  2. **Act:** Execute the code under test.
  3. **Assert:** Verify that the outcome matches the expected result.
- Don't add "Arrange", "Act", or "Assert" comments that break up the sections because this is obvious and unnecessary.

## 3. Isolate Your Tests

- Use mocking frameworks to simulate the behavior of external dependencies.
- This ensures that your tests focus solely on the functionality of the unit being tested.

## 4. Test Edge Cases and Error Conditions

- Do not just test the "happy path."
- Consider edge cases and potential error conditions.
  - This ensures that your code handles unexpected inputs gracefully and robustly.
  - If it is allowed by the type system, cover scenarios such as empty inputs, null values, and boundary conditions.

## 5. Keep Tests Fast

- Unit tests should run quickly to provide immediate feedback.
- Slow tests can hinder productivity and discourage developers from running tests frequently.
- Optimize test setup and teardown processes to minimize execution time.

## 6. Do Not Write Overly Complex Tests

- Complex tests are harder to understand and maintain.
- Keep your tests simple and focused on a single behavior.
- Do not test multiple functionalities in a single test.
- Break them down into smaller, manageable tests.

## 7. Do Not Rely Too Much on Mocks

- While mocking is useful, over-reliance on mocks can lead to tests that do not accurately represent real-world scenarios.
- Strike a balance between using real objects and mocks.
- Ensure that tests still provide meaningful validation of the behavior of the code.

## 8. Aim for Full Test Coverage

- Strive to cover all possible code paths with your tests.
- This does not mean that your code should be tested in all scenarios.
- Mindless test coverage does not guarantee bug-free code, so think critically about what should be tested making sure all tests are valuable and not pointless.

## 9. Follow Our Opinionated Testing Guidelines

- Group related test cases within a describe block encapsulating related tests.
- Use `beforeEach` and `afterEach` hooks to set up and tear down common test conditions to make tests more DRY, but without coupling tests too tightly and making them brittle.
- Use the Jest library unless otherwise stated.
- Prefer leveraging one of the many built-in Jest test matchers over custom assertions.
- Prefer spying and mocking specific functions or methods used in the workflow instead of entire files, libraries, or modules.
- Define mocks consistently by reaching for `jest.spyOn`, `jest.mockReturnValue` and `jest.mockImplementation` before reaching for other mocking patterns.
- If an existing test suite is provided, then re-use as much scaffolding as possible without tightly coupling the tests.

## 10. Pay attention to common Angular testing quirks

- We use Jasmine instead of Jest in our Angular monorepo so make sure to make any necessary adjustments.
- Use `TestBed` to test Angular components, paying close attention to any imports or providers that need to be defined.
- Ensure the proper handling of async observables, and leverage built-in utilities like `fakeAsync` and `tick` to test async workflows.
- Pay attention to whether a component is "standalone", and if so then put it in the "imports" array in the `TestBed` setup (not the "declares" array).
