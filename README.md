# SwiftUIVolumeButtonsHandler

SwiftUIVolumeButtonsHandler is simple way to handling clicks on hardware volume buttons on iPhone or iPad. 

## Usage

### Step 1: Declare the handler
```
let volumeButtonHandler = VolumeButtonHandler(containerView: UIView())
```

### Step 2: Automatically start the handler by adding the overlay
```
.overlay(
    VolumeButtonHandlerView(volumeButtonHandler: volumeButtonHandler)
)
```

### Step 3: Listen for button presses
```
.onAppear {
    volumeButtonHandler.buttonClosure = { button in
        switch button {
        case .up:
            print("Volume up button pressed")
            // execute your code for volume up button press here
        case .down:
            print("Volume down button pressed")
            // execute your code for volume down button press here
        }
    }
}
```

## Requirements

iOS 11 and newer.

## Installation

To install SwiftUIVolumeButtonsHandler, download the code as a zip file, then drag `Log.swift` and `VolumeButtonHandler.swift` into your project.

## References

This project based on Objective-C code [JPSVolumeButtonHandler](https://github.com/jpsim/JPSVolumeButtonHandler)  
