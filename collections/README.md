## Collection

If you’re transforming a collection, but you don’t need to access all the elements right away (or at all), you may be able to save cycles and allocations by using the lazy family of collection types: 

```swift
let userCellsData = users.**lazy**.map { user in
   UserCellData(username: user.username, bioAttributedString:
formatBioString(user.bio))
}
```

----------------------------------
[return to home](../README.md)