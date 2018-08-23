## Declaration

### final  
Use *final* on properties and methods when you know that a declaration does not need to be overridden. This allows the compiler to replace these dynamically dispatched calls with direct calls. You can even mark an entire class as final by attaching the attribute to the class itself. 

When properties do not need to be overrriden 
```swift 
class Blogpost {
	final var title: String?
	final var subTitle: String? 
	final var post: String?
}
```

When whole class does not need to be overrriden 
```swift 
final class Blogpost {
	var title: String?
	var subTitle: String? 
	var post: String?
}
```

Straight from Apple Documentation <br>
**Preventing Overrides**
_You can prevent a method, property, or subscript from being overridden by marking it as final. Do this by writing the final modifier before the method, property, or subscript’s introducer keyword (such as final var, final func, final class func, and final subscript)._

_Any attempt to override a final method, property, or subscript in a subclass is reported as a compile-time error. Methods, properties, or subscripts that you add to a class in an extension can also be marked as final within the extension’s definition._

_You can mark an entire class as final by writing the final modifier before the class keyword in its class definition (final class). Any attempt to subclass a final class is reported as a compile-time error._

[Apple Doc Inheritence](https://docs.swift.org/swift-book/LanguageGuide/Inheritance.html)