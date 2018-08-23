
### Home > Switch Tips
------------------

**Simpletest switch**
```swift
let name = “Ironman”
switch name {
case “Spiderman”:  print(“Hello Perter Parker”)
case “Ironman”: print(“Hello Tony Stark”)
```

**Comparing More than one value** 
```swift
let name = “Ironman”
let pass = “jarvis”
switch (name, pass)  {
case (“Spiderman”,  “park3r”):  print(“Hello Perter Parker”)
case (“Ironman”, “m#n”): print(“Hello Tony Stark”)
default: print(“who are you?”)
```

**Using tuple to make above code look pretty** 
```swift
let authentication = (name: “Ironman”, pass: “jarvis”)
switch authentication  {
case (“Spiderman”,  “park3r”):  print(“Hello Perter Parker”)
case (“Ironman”, “m#n”): print(“Hello Tony Stark”)
default: print(“who are you?”)
```

**Partial matching with tuple**
```swift
let authentication = (name: “Ironman”, pass: “jarvis”, hostIp: 227.89.94.62)
switch authentication  {
case (“Spiderman”,  “park3r”, _):  print(“Hello Perter Parker”)
case (“Ironman”, “m#n”, _): print(“Hello Tony Stark”)
default: print(“who are you?”)
```

_Always remember swift picks up the first match not better match. 
If case (_, _, _) are in above example  at the top. It would be picked._ 

**If you like to know other parts of tuple but keep them out of matching. You should use let syntax** 
```swift
switch authentication  {
case (“Spiderman”,  “park3r”, _):  print(“Hello Perter Parker”)
case (“Ironman”, let pass, _): print(“Hello Tony Stark,: pass was \(pass)!”)
default: print(“who are you?”)
```

