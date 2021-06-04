| RegEx Pattern | Description
| ----- | ----- |
| (\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d) | Match Date format MM/dd/yyyy HH:mm:SS
| [0-9a-zA-Z]\([-.\w]*[0-9a-zA-Z_+])*@([0-9a-zA-Z]\[-\w]*[0-9a-zA-Z]\.)+[a-zA-Z]{2,9} | Email address
| #([a-fA-F0-9]){3}(([a-fA-F0-9]){3})? | HTML HEX code (e.g. "#0000")
| (https?):\/\/([0-9a-zA-Z][-\w]*[0-9a-zA-Z]\.)+[a-zA-Z]{2,9})(:\d{1,4})?([-\w\/#~:.?+=&%@~]*) | HTTP URL
| /^\d{1,5}$/ | Match any nubmers from 0 to 99999
| ([0-9a-fA-F]{2}:){5}[0-9a-fA-F]{2} | MAC Address
| (\d{3}-\d{2}-\d{4}) | Social Security Number (SSN)
| (\b\d{3}-\d{2}-\d{4}\b) | Social Security Number (SSN) with word boundaries. This has less false-positives when the SSN isn't delimited in the dataset. This will filter out something like 23987-65-4322, but still match 987-65-4322 as long as there are no other characters next to the SSN.
| s/^\s+// | Trim leading and trailing whitespace
| VID_([0-9a-fA-F]{4}) | USB Vendor ID "VID_064B"
| PID_([0-9a-fA-F]{4}) | USB Product ID "PID_0F64"
| (\S+\\\S+\\\S+). | Windows Symbolic Name/Device Path "USB\VID_04E8&PID_6860&MS_COMP_MTP&SAMSUNG_ANDROID\6&1DEB1FB4&0&0000"
| /^\$\(d{1,3}(\,\d{3})*\|\d+)(\.\d{2})?$/ | U.S. Dollars (e.g. $1,000,000)
| (\d{5}(-\d{4})?) | U.S. Zip Code
| /^.*\// | Linux leading path (e.g. /etc/passwd)
