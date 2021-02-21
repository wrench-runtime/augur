# Augur
A jasmine inspired unit testing framework for wren

## Getting started

```wren
import "augur" for Assert, Augur
import "shapes" for Rectangle

// Create a test suite
Augur.describe(Rectangle){
  
  // Add a unit test
  Augur.it("reports correct size"){
    var r = Rectangle.new(10, 20, 30, 40)
    Assert.equal(r.x, 10)
    Assert.equal(r.y, 20)
    Assert.equal(r.w, 30)
    Assert.equal(r.h, 40)
    Assert.equal(r.right, 40)
    Assert.equal(r.bottom, 60)
  }

  // Add another unit test
  Augur.it("reports if inside"){
    var r = Rectangle.new(10, 20, 30, 40)
    Assert.isTrue(r.isInside(10,20))
    Assert.isTrue(r.isInside(30,30))
    Assert.isFalse(r.isInside(40,60))
  }
}

// Run all test suites
Augur.run()
```
