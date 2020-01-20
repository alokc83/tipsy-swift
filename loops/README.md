## Loops
```swift
    let ironman = (name: "Tony", password: "M#n")
    let spiderman = (name: "Peter", password: "Spid3r")
    let deadpool = (name: "Wade", password: "w1lls0n")
    let users = [ironman, spiderman, deadpool]

//simply printing name
for user in users {
   print(user.name)
} 
```

**Just like _switch_, we can user case  with a tuple to match specific values inside the tuples.** 
```swift
    for case("Wade", "w1lls0n") in users {
        print("user Wade’s pass is w1lls0n")
    }
```

**You can also bind local constants to values of each tuple:** 
```swift
    for case  (let name, let pass) in users {
    print("User \(name) ’s pass is \(pass)")
    }
```

**You can also rearrange it in tuple format as below:**
```swift
    for case let (name, pass) in users {
     print("User \(name) ’s pass is \(pass)")
    }
```

**You can also mix and match above mentioned techniques**
```swift
    for case let (name, "Spid3r") in users {
     print("User \(name) ’s pass is Spid3r")
    }
```

Above technique filters out the array for pass phrase. 

It’s very easy to get confused when see this weird syntax for first time as three different keywords (_for case let_) are being massed first time.  It’s not at all obvious at the first glance. 

----------------------------------
[return to home](../README.md)
