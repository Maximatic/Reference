| RegEx Pattern | Description
| ----- | ----- |
| (\d{3}-\d{2}-\d{4}) | Social Security Number (SSN)
| (\b\d{3}-\d{2}-\d{4}\b) | Social Security Number (SSN) with word boundaries. This has less false-positives when the SSN isn't delimited in the dataset. This will filter out something like 23987-65-4322, but still match 987-65-4322 as long as there are no other characters next to the SSN.
| VID_([0-9a-fA-F]{4}) | USB Vendor ID "VID_064B"
| PID_([0-9a-fA-F]{4}) | USB Product ID "PID_0F64"
| (\S+\\\S+\\\S+). | Windows Symbolic Name/Device Path "USB\VID_04E8&PID_6860&MS_COMP_MTP&SAMSUNG_ANDROID\6&1DEB1FB4&0&0000"
