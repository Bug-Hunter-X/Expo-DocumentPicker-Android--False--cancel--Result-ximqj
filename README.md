# Expo DocumentPicker Android: False 'cancel' Result

This repository demonstrates a bug in Expo's DocumentPicker API on Android.  The `DocumentPicker.getDocumentAsync` method sometimes returns a `type` of `"cancel"` even when a file has been selected by the user.  This can lead to unexpected application behavior if not properly handled.

## Steps to Reproduce

1. Run the provided example on an Android device or emulator.
2. Open the file picker and select a file.
3. Observe that the app sometimes incorrectly reports a cancellation, even with a file selected.

## Solution

The provided solution employs a more robust error handling mechanism. Instead of simply checking for `type === 'cancel'`, it performs additional checks to ensure the file URI is valid before processing it.  Further investigation into the root cause is recommended, but this workaround addresses the immediate issue.

## Contributing

Contributions are welcome. Please open an issue or submit a pull request if you have any suggestions or improvements.