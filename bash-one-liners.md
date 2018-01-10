# Get Battery Status
```bash
acpi -b |sed -e 's@.*\\([0-9]:\\) [^,]*,@\\1@' -e 's@remaining@@' | sed -e :a -e '$!N;s@\\n@| @;ta'
```
