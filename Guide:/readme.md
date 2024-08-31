# Guide:
https://ubuntu.com/server/docs/how-to-enable-nested-virtualization

```
test(){
  cpu_make=intel #amd
  cat /sys/module/kvm_${cpu_make}/parameters/nested
  # or
  cat /sys/module/kvm_${cpu_make}/parameters/nested
```
