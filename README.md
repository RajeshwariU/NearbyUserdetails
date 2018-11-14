# NearbyUserdetails

[![CI Status](https://img.shields.io/travis/RajeshwariU/NearbyUserdetails.svg?style=flat)](https://travis-ci.org/RajeshwariU/NearbyUserdetails)
[![Version](https://img.shields.io/cocoapods/v/NearbyUserdetails.svg?style=flat)](https://cocoapods.org/pods/NearbyUserdetails)
[![License](https://img.shields.io/cocoapods/l/NearbyUserdetails.svg?style=flat)](https://cocoapods.org/pods/NearbyUserdetails)
[![Platform](https://img.shields.io/cocoapods/p/NearbyUserdetails.svg?style=flat)](https://cocoapods.org/pods/NearbyUserdetails)

This library is used to find nearby user from your current location with respect to your radius.

## Example

To run the example project, clone the repo, and run `pod install` from the Example directory first.

## Requirements

Xcode 6 or later
iOS 8 or later

## Installation

NearbyUser is available via CocoaPods. 

## CocoaPods

To install NearbyUser using CocoaPods, add the following line to your Podfile:

```ruby
pod 'NearbyUserdetails'
```
## Usage

`import NearbyUser`

1.Create object for mapManagers class[which is in pod]__   
Example:__  
var mapObject = mapManagers() 

2.mapManagers class has below method with returntype of GMSMapView__
public func initLocationManagerWithRadiusAndMap(getRadius: String, googleMapView: GMSMapView) -> GMSMapView__
{__
    return GMSMapView__
}__
usage of the above method is:__
`gMap = mapObject.initLocationManagerWithRadiusAndMap(getRadius: "yourradiusvalue", googleMapView: gMap)`__
(in viewDidLoad or wherever based on your preference)

3.mapManagers class has following variables:__
/// This variable is used to store all user informatiom from json/api__
public var userInformation: [[String: String]] = []__
/// This variable is used set custom marker image__
public var pinImage = UIImage()__
/// This variable is used for placeholder image inside the pin image__ 
public var userPlaceholderImage = UIImage()

usage of the above variables is:__
`mapObject.userInformation = "yourData from api/json"`__
`mapObject.pinImage = UIImage(named: "yourImage")!`__
`mapObject.userPlaceholderImage = UIImage(named: "yourImage")!`

Note:__
gMap - outlet of your GMSMapView[used in your project]__
mapObject - instance of mapManagers class

## Author

RajeshwariU, rajeshwari.u@contus.in

## License

NearbyUserdetails is available under the MIT license. See the LICENSE file for more info.
