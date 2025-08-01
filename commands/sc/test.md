---
allowed-tools: [Read, Bash, Glob, TodoWrite, Edit, Write]
description: "테스트 실행, 테스트 보고서 생성 및 테스트 커버리지 유지"
---

# /sc:test - Testing and Quality Assurance

## Purpose
Execute comprehensive testing workflows with TDD focus, emphasizing XCTest for Swift development, descriptive test naming, and systematic test-driven development cycles.

## Usage
```
/sc:test [target] [--type unit|integration|e2e|ui|performance|all] [--framework xctest|quick|swiftui] [--coverage] [--watch] [--swift]
```

## Arguments
- `target` - Specific tests, files, or entire test suite
- `--type` - Test type (unit, integration, e2e, ui, performance, all)
- `--framework` - Test framework (xctest, quick, swiftui)
- `--coverage` - Generate coverage reports with Xcode coverage
- `--watch` - Run tests in watch mode with Xcode
- `--fix` - Automatically fix failing tests when possible
- `--tdd` - Enable TDD workflow with test-first approach
- `--swift` - Apply Swift-specific testing patterns and XCTest
- `--descriptive` - Generate descriptive test names and clear failure messages
- `--async` - Test async/await and Combine code
- `--ui` - Test SwiftUI views and UI components
- `--performance` - Run performance tests and benchmarks
- `--mock` - Generate and use mocks for dependencies
- `--ci` - Optimize for CI/CD environment

## Execution
1. **Swift Test Environment Setup**: Configure Xcode test targets and schemes
2. **Test Discovery & Organization**: Identify existing tests and organize by type
3. **Swift-Specific Test Execution**: Run tests with appropriate Swift frameworks
4. **Async & UI Test Handling**: Execute async/await, Combine, and SwiftUI tests
5. **Coverage & Performance Analysis**: Generate comprehensive Swift test reports

## Swift Testing Guidelines

### XCTest Framework Best Practices
- **Descriptive Test Names**: Use clear, descriptive names (e.g., `testSumOfTwoPositiveNumbers_returnsCorrectResult`)
- **Test Organization**: Group related tests in test classes with clear responsibilities
- **Setup/Teardown**: Use `setUp()` and `tearDown()` for test lifecycle management
- **Test Data Factories**: Create reusable test data builders and helpers

### Async Testing Patterns
- **XCTestExpectation**: Use for async/await and Combine testing
- **Async Test Methods**: Leverage `async` test methods for modern Swift
- **Timeout Management**: Set appropriate timeouts for async operations
- **Error Handling**: Test error cases and edge conditions

### SwiftUI Testing
- **View Testing**: Test SwiftUI views with `ViewInspector` or `ViewHosting`
- **State Testing**: Verify view state changes and user interactions
- **Preview Testing**: Test SwiftUI previews and different device configurations
- **Accessibility Testing**: Ensure accessibility compliance in UI tests

### Performance Testing
- **Benchmark Testing**: Use `XCTestCase.measure` for performance benchmarks
- **Memory Testing**: Detect memory leaks and excessive allocations
- **CPU Profiling**: Monitor CPU usage during test execution
- **Network Testing**: Mock network calls and test offline scenarios

## Claude Code Integration
- Uses Bash for Xcode test execution and monitoring
- Leverages Glob for Swift test file discovery
- Applies TodoWrite for test result tracking and TDD progress
- Maintains structured Swift test reporting and coverage analysis
- Integrates with Xcode schemes and test targets
- Supports Swift Package Manager test execution
- Answer to Korean always

## Gemini CLI Integration
Leverage Gemini CLI for large-scale Swift test analysis and strategy planning:

### Usage Scenarios
1. **Swift Test Coverage Analysis**
   ```bash
   # Complete Swift test coverage analysis
   gemini -p "Analyze all Swift test files and find areas with insufficient coverage" Tests/
   
   # Swift test quality evaluation
   gemini -p "Analyze Swift test code quality and suggest improvement strategies"
   ```

2. **Swift Test Strategy Planning**
   ```bash
   # Swift test pyramid analysis
   gemini -p "Analyze current Swift test structure and suggest optimal test pyramid"
   
   # SwiftUI test scenario design
   gemini -p "Analyze SwiftUI views and design comprehensive UI test scenarios"
   ```

3. **Swift Test Performance Optimization**
   ```bash
   # Swift test execution time analysis
   gemini -p "Analyze Swift test execution time and suggest optimization strategies"
   
   # Swift async test stability analysis
   gemini -p "Find unstable Swift async tests and suggest stabilization strategies"
   ```

4. **Swift Test Framework Analysis**
   ```bash
   # XCTest vs Quick/Nimble analysis
   gemini -p "Analyze Swift test frameworks and suggest optimal framework selection"
   
   # Swift test mocking strategy
   gemini -p "Analyze Swift dependency mocking strategies and suggest best practices"
   ```

### Collaboration Strategy
- **Swift Test Strategy Analysis**: Use Gemini to analyze complete Swift test strategies
- **Swift Test Execution**: Use Claude Code to perform accurate Swift test execution
- **Swift Test Result Analysis**: Interpret Swift test results and derive improvement strategies

## Swift Test Examples

### XCTest Unit Test Example
```swift
class CalculatorTests: XCTestCase {
    var calculator: Calculator!
    
    override func setUp() {
        super.setUp()
        calculator = Calculator()
    }
    
    func testSumOfTwoPositiveNumbers_returnsCorrectResult() {
        // Given
        let a = 5
        let b = 3
        
        // When
        let result = calculator.sum(a, b)
        
        // Then
        XCTAssertEqual(result, 8)
    }
    
    func testAsyncOperation_completesSuccessfully() async throws {
        // Given
        let expectation = XCTestExpectation(description: "Async operation completes")
        
        // When
        let result = try await calculator.asyncOperation()
        
        // Then
        XCTAssertNotNil(result)
        expectation.fulfill()
        await fulfillment(of: [expectation], timeout: 5.0)
    }
}
```

### SwiftUI Test Example
```swift
class ContentViewTests: XCTestCase {
    func testContentView_displaysCorrectTitle() {
        // Given
        let contentView = ContentView()
        
        // When & Then
        XCTAssertNoThrow(try contentView.inspect().find(text: "Hello, World!"))
    }
    
    func testContentView_buttonTap_triggersAction() {
        // Given
        let contentView = ContentView()
        
        // When
        try contentView.inspect().find(button: "Tap me").tap()
        
        // Then
        // Verify state change or action trigger
    }
}
```

### Performance Test Example
```swift
class PerformanceTests: XCTestCase {
    func testDataProcessingPerformance() {
        let dataProcessor = DataProcessor()
        let testData = generateLargeTestData()
        
        measure {
            _ = dataProcessor.process(testData)
        }
    }
}
```

## Swift Test Tools Integration

### Xcode Integration
- **Test Schemes**: Configure test schemes for different environments
- **Test Targets**: Set up separate test targets for unit, integration, and UI tests
- **Code Coverage**: Enable code coverage reporting in Xcode
- **Test Plans**: Use test plans for complex test configurations

### Swift Package Manager
- **Test Dependencies**: Add test-specific dependencies (Quick, Nimble, Cuckoo)
- **Test Targets**: Configure test targets in Package.swift
- **Test Execution**: Run tests via `swift test` command

### CI/CD Integration
- **Fastlane**: Integrate with Fastlane for automated testing
- **Xcode Cloud**: Use Xcode Cloud for cloud-based testing
- **GitHub Actions**: Configure GitHub Actions for Swift testing
- **Test Reporting**: Generate test reports for CI/CD pipelines