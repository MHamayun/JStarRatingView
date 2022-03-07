# JStarRatingView

JStarRatingView is a simple Star Rating View for displaying star ratings and entering them (by touching the stars). It's written for iOS, in Swift 5.1 (UIKit, not SwiftUI). It also works with Interface Builder

![imgpsh_fullsize_anim-38](https://user-images.githubusercontent.com/16849127/157054211-57a0608f-15cc-426b-9f34-f8441c3c8904.png)

<img width="643" alt="starRatingViewInIntefaceBuilder" src="https://user-images.githubusercontent.com/16849127/156575103-4250e43a-6920-4625-84e1-b44805d10074.png">


## Installation
Copy the 3 files to your XCode projects

## Usage
### Interface Builder
1. Add a UIView to your interface
2. In the Identiy Inspector, change Class to `JStarRatingView`
3. In the Attributes Inspector you can now set:
 * the **rating** (Float between 0 and 5)
 * the **star color**
 * the **Star Rounding** Raw Value - *IBInspectable can't handle enums, hence the raw value, see ENUM code below*
4. By checking **User Interaction Enabled** users can touch the view to enter a star rating. The rating stars updates while touching.

### Code
1. Create an instance of JStarRatingView  
`let starRatingView = JStarRatingView(frame: CGRect(origin: .zero, size: CGSize(width: 250, height: 50)), rating: 3.5, color: UIColor.systemOrange, starRounding: .roundToHalfStar)`  
Natural aspect ratio is 5 width to 1 height. 
2. Add the view as a subview
3. Properties (set and get)
 * `starRatingView.rating` (type: `Float`)
 * `starRatingView.starColor` (type: `UIColor`)
 * `starRatingView.starRounding` (type: `StarRounding`)
 * `starRatingView.isUserInteractionEnabled` (type: `Bool`)

## The StarRounding ENUM
`public enum StarRounding: Int {`  
`  case roundToHalfStar = 0`  
`  case ceilToHalfStar = 1`  
`  case floorToHalfStar = 2`  
`  case roundToFullStar = 3`  
`  case ceilToFullStar = 4`  
`  case floorToFullStar = 5`  
`}`

## Comments
* The stars are SF Symbols and as such resize automatically without loosing image quality
* Feel free to use in your projects. A mention would be appreciated. 
* Feel free to clone, download, create pull requests etc. I'm open to expanding functionality and improving where necessary 

