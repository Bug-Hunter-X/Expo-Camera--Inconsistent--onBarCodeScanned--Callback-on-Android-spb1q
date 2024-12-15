# Expo Camera: Inconsistent `onBarCodeScanned` Callback on Android

This repository demonstrates an uncommon bug related to the Expo Camera API's `onBarCodeScanned` prop.  Specifically, the callback function may not fire reliably on Android devices, particularly when barcodes are scanned rapidly or multiple times in quick succession.  This issue is less pronounced on iOS.

The `bug.js` file contains the problematic implementation, illustrating the inconsistent behavior.  The solution, found in `bugSolution.js`, addresses the issue by implementing debouncing to control the rate at which the `onBarCodeScanned` callback is executed.