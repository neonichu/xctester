# xctester

Commandline test runner for Swift.

## Usage

Having to create those pesky Xcode projects just to run your tests is
annoying. With `xctester`, you don't have to anymore.

Consider this test case:

```swift
import XCTest

class MyTests : XCTestCase {
  func testAdd() {
    let result = add(3, 5)
    XCTAssertEqual(result, 8, "")
  }

  func testAddFail() {
    XCTAssertTrue(false, "lol")
  }
}
```

Simply running `xctester` will execute the tests and give you the results:

```
MyTests

✅  -[MyTests testAdd]
❌  -[MyTests testAddFail]
	XCTAssertTrue failed - lol

 Executed 2 tests, with 1 failures (1 unexpected) in 0.001 seconds
```

## License

xctester is licensed under the MIT license. See [LICENSE](LICENSE) for
more information.