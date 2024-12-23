# React Native Dimensions.get('window') Inconsistency

This repository demonstrates a bug related to inconsistent screen dimension values returned by `Dimensions.get('window')` in React Native.  The issue is that this API doesn't always reflect the actual screen dimensions accurately, leading to layout problems. This is particularly noticeable in certain situations, such as after device rotation.

## Bug Description

The `Dimensions.get('window')` method provides screen dimensions, but these may not accurately reflect the current screen size, particularly in dynamic situations. This inconsistency causes UI elements to misalign or have incorrect sizes.

## Solution

The solution uses `Dimensions.addEventListener` to listen for changes and updates state accordingly.  This is more robust than solely relying on the initial `Dimensions.get` call.