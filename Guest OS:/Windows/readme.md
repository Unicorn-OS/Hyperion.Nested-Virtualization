sch:
- https://www.google.com/search?q=kvm+nested+virtualization+WSL
- https://www.google.com/search?q=nested+virtualization+WSL+Windows+on+KVM

# Discuss:
https://www.reddit.com/r/kvm/comments/14qku51/running_wsl2_and_docker_in_a_windows_guest/


>In order to suppress the flag, you have to edit your guest's XML. Find the line that looks like this:
```
<cpu mode="host-passthrough" check="none" migratable="on"/>
```
>And change it so that it looks like this:
```
<cpu mode="host-passthrough" check="none" migratable="on">

<feature policy="disable" name="hypervisor"/>

</cpu>
```
