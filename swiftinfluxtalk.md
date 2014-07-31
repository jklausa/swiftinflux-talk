![original](http://swiftwarsaw.com/stylesheets/img/bg.jpg)

# [fit] Swift in Flux

# [fit] 31.07.2014 / Swift Warsaw #1

#### Jan Klausa / @klausa_qwpx / klausa.pl

---

# [fit] So, Swift.

---

# [fit] New.

---

# [fit] In progress.

---

# [fit] one might say...

# [fit] In flux.

___

# [fit] Swift InFlux

##  "An attempt to gather all that is in flux in Swift."

#### github.com/ksm/swiftinflux

#### @karolsmazur

___

# [fit] born at a SwiftCrunch.

# [fit] over 800 stars on GitHub.

# [fit] featured in iOS Dev Weekly.

^ only five most interesting


___

# [fit] #1 - Reflection.

* Undocumented.
* Half-baked.
* Could disappear before 1.0.

___

```swift
class Test {
    var title: String? = ""
    var count: Int = 0
}

let testReflect = reflect(Test())
var properties: [String] = []

for index in 0 ..< testReflect.count {
    let (propertyName, _) = testReflect[index]
    properties.append(propertyName)
}
// properties is now ["title", "count"]
```

___

# [fit] #2 IBOutlet

* was implicitly `weak`.
 
* was implicitly unwrapped optional (`!`).

# [fit] super confusing.

___

# #2 IBOutlet

* IBOutlet won't have any implicit behaviour in future Beta.

# [fit] yay!

___

# [fit] #3 Optionals in ObjC imports

* everything is imported as implicitly unwrapped optional (`!`).

* harder to distinguish types that can or can't be nil.
	
___

# [fit] #3 Optionals in ObjC imports

>"Any plans to audit the Frameworks and mark where it actually can return nil?" 

"Look for details in subsequent betas."

>*-- Chris Lattner*

___

# [fit] #4 Optional Bool is confusing

```swift
var foo: Bool? = false
if foo {
    println("bar")
}
else {
	println("baz")
}
```

___ 

# [fit] #4 Optional Bool is confusing

### Confusing for everything conforming to `LogicValue`.

"We have a fix for "optional bool confusion" (...) in the next beta (along with a few other improvements to optional semantics)."

>*-- Chris Lattner*

___

# [fit] #5 Implicit conversions

```swift
extension Int {
   func __conversion() -> CGFloat {
        return CGFloat(self)
   }
}
let x: CGFloat = 3.5
let y: Int = 2
let z = x * y // z is CGFloat and equals 7.0
```

___

# [fit] #5 Implicit conversions

"It has never been documented, and we are planning to remove it for the final release."

>*-- Chris Lattner*

___

# [fit] Apple Forums.

# [fit] Popular blogs.

# [fit] ???

___

##  Found something? 

#  Contribute!

## Fork.

##  Submit a Pull Request.

___

# [fit] Freenode IRC channels:

# [fit] #swift-lang

# [fit] #iphonedev

___

# [fit] ...and that's all, folks!

# [fit] github.com/jklausa/swiftinflux-talk

### @klausa_qwpx
