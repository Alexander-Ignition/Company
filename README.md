#  Company

Mac app

Example application building in UI with cocoa binding and Core Data

## Create mac app

- [x] Select your Team
- [  ]  Use storiboard
- [x] Create Document-Based Application
- [x] Use Core Data 

## Project File
- Targets / Company / Capabilities / App Sandbox / File Access / User Selected File : Read/Write

## Models

- Open Document.xcdatamodeld
- Add Entity
- Rename new `Entitiy` to `Person`
- Add Attributes
    - `fisrName` String
    - `lastName` String
    - `birthday`: Date
    - `photo`: Binary Data
    
## Interface Building

- Open `Document.xib`
- Add table view

## Cocoa Bindings

- Add Array Controller
    - Attributes inspector / Object Controller
        - Mode: `Entity Name`
        - Entity Name: `Person`
    - Bindings inspector / Parameters / Managed Object Context
        - [x] Bind to: `File's Owner`
        - Model Key Path: `self.managedObjectContext`
    - Connections inspector / Received Actions
        - Connect `add:` with button
        - Connect `remove:` with button
- Table View
    -  Bindings inspector / Table Content / Content
        - [x] Bind to: `Array Controller`
        - Controller Key: `arrangedObjects`