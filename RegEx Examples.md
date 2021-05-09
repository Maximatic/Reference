| RegEx Pattern | Description
| ----- | ----- |
| (\d{3}-\d{2}-\d{4}) | Social Security Number (SSN)
| (\b\d{3}-\d{2}-\d{4}\b) | Social Security Number (SSN) with word boundaries. Has less false-positives. Will filter out something like 23111-22-1234, but still catch 111-22-1234 as long as there are no other characters next to the SSN.
| VID_([0-9a-fA-F]{4}) | USB Vendor ID "VID_064B"
| PID_([0-9a-fA-F]{4}) | USB Product ID "PID_0F64"
| (\S+\\\S+\\\S+). | Windows Symbolic Name/Device Path "USB\VID_04E8&PID_6860&MS_COMP_MTP&SAMSUNG_ANDROID\6&1DEB1FB4&0&0000"
