# InfiniteScroller

[![Swift Version][swift-image]][swift-url]
[![License][license-image]][license-url]
[![SwiftPM compatible](https://img.shields.io/badge/SwiftPM-compatible-4BC51D.svg?style=flat)](https://github.com/Carthage/Carthage)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
<table cellspacing="0" cellpadding="0" style="border-collapse: collapse; border: none;">
<tr>
    <td><img src="https://github.com/cointowitcher/InfiniteScroller/blob/master/docs/time_picker_example.gif" width="412">
</td>
    <td><img src="https://github.com/cointowitcher/InfiniteScroller/blob/master/docs/example.gif" width="600"></td>
    </tr>
    </table>


## Example

```swift
struct ContentView: View {
    @State var selected: Int = 1
    var body: some View {
        InfiniteScroller(direction: .vertical(height: 50), items: [1,2,3,4], 
        selectedItem: $selected, visibleCells: 3, cellSpacing: 0) { Text("\($0)") }
    }
}
```
and you good to go.
But if something doesn't go well, you can always clone the repo and check 'Example' folder

### Updating

If you need to update cells which has already been loaded, you can enable this feature by passing
'updating' argument to the constructor of InfiniteScroller and setting it to true. Recommended to be disabled if you
don't need this feature

### How it works?

It uses InfiniteLayout library(https://github.com/arnauddorgans/InfiniteLayout) underneath, so you can extend its functionality

## Installation

### [Swift Package Manager](https://github.com/apple/swift-package-manager)
Select File > Swift Packages > Add Package Dependency and enter https://github.com/cointowitcher/InfiniteScroller.git 

## Known issues

- Items aren't displayed correctly if the amount of the items is less or equal to visibleCells parameter. So, make sure to pass more items than visible cells

## Contribute

We would love you to contribute to this project, the project is opened for modifications. 

## License

InfiniteScroller is available under the MIT license. See the LICENSE file for more info.

[swift-image]:https://img.shields.io/badge/swift-5.2-orange.svg
[swift-url]: https://swift.org/
[license-image]: https://img.shields.io/badge/License-MIT-blue.svg
[license-url]: LICENSE
[codebeat-image]: https://codebeat.co/badges/c19b47ea-2f9d-45df-8458-b2d952fe9dad
[codebeat-url]: https://codebeat.co/projects/github-com-vsouza-awesomeios-com
