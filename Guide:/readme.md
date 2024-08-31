# Guide:
https://ubuntu.com/server/docs/how-to-enable-nested-virtualization

```
enable(){
  echo "options kvm_amd nested=1" | sudo tee /etc/modprobe.d/kvm.conf
}

test(){
  cpu_make=intel #amd
  cat /sys/module/kvm_${cpu_make}/parameters/nested
  # or
  cat /sys/module/kvm_${cpu_make}/parameters/nested
```

https://docs.fedoraproject.org/en-US/quick-docs/using-nested-virtualization-in-kvm/
