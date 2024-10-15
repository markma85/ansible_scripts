# ansible_scripts

## node_info
```console
$ ansible-playbook node_info.yml
```
<details><summary>Output</summary>
>PLAY [Gather node information] >- *********************************************>- *****************************************
>- TASK [Gathering Facts] >- *********************************************>- *********************************************>- ****ok: [master]
>- ok: [node1]
>- ok: [node2]
>- 
>- TASK [Gather Hostname and IP Address] >- *********************************************>- **********************************ok: >- [master] => {
>-     "msg": "master - Hostname: master, IP >- Address: 10.0.0.101"
>- }
>- ok: [node1] => {
>-     "msg": "node1 - Hostname: node1, IP >- Address: 10.0.0.102"
>- }
>- ok: [node2] => {
>-     "msg": "node2 - Hostname: node2, IP >- Address: 10.0.0.103"
>- }
>- 
>- TASK [Gather Operating System Information] >- *********************************************>- *****************************ok: [master] => >- {
>-     "msg": "master - OS: Ubuntu 24.04 >- (x86_64)"
>- }
>- ok: [node1] => {
>-     "msg": "node1 - OS: Ubuntu 24.04 (x86_64)>- "
>- }
>- ok: [node2] => {
>-     "msg": "node2 - OS: Ubuntu 24.04 (x86_64)>- "
>- }
>- 
>- TASK [Gather CPU Information] >- *********************************************>- ******************************************ok:>-  [master] => {
>-     "msg": "master - CPU Cores: 6"
>- }
>- ok: [node1] => {
>-     "msg": "node1 - CPU Cores: 2"
>- }
>- ok: [node2] => {
>-     "msg": "node2 - CPU Cores: 2"
>- }
>- 
>- TASK [Gather Memory Information] >- *********************************************>- ***************************************ok: >- [master] => {
>-     "msg": "master - Total Memory: 64003 MB"
>- }
>- ok: [node1] => {
>-     "msg": "node1 - Total Memory: 7525 MB"
>- }
>- ok: [node2] => {
>-     "msg": "node2 - Total Memory: 7637 MB"
>- }
>- 
>- TASK [Gather Disk Information] >- *********************************************>- *****************************************chan>- ged: [master]
>- changed: [node2]
>- changed: [node1]
>- 
>- TASK [Display Disk Information] >- *********************************************>- ****************************************ok: >- [master] => {
>-     "disk_info.stdout_lines": [
>-         "Filesystem      Size  Used Avail >- Use% Mounted on",
>-         "tmpfs           6.3G  3.3M  6.3G   >- 1% /run",
>-         "/dev/nvme0n1p2  468G   20G  424G   >- 5% /",
>-         "tmpfs            32G  188K   32G   >- 1% /dev/shm",
>-         "tmpfs           5.0M  8.0K  5.0M   >- 1% /run/lock",
>-         "efivarfs        192K   69K  119K  >- 37% /sys/firmware/efi/efivars",
>-         "/dev/nvme0n1p1  1.1G  6.2M  1.1G   >- 1% /boot/efi",
>-         "/dev/sda1       932G  103G  829G  >- 12% /data",
>-         "tmpfs           6.3G  112K  6.3G   >- 1% /run/user/120",
>-         "tmpfs           6.3G   88K  6.3G   >- 1% /run/user/1000",
>-         "overlay         468G   20G  424G   >- 5% /var/lib/docker/overlay2/>- 75b172666847687c917f543507cf4e3f48dc5>- 4ec1712d07cf4018bcc73fa9b28/merged",
>-         "overlay         468G   20G  424G   >- 5% /var/lib/docker/overlay2/>- 6f4039e06ed98aaa179afb0ac4dd8d85f2b8a>- 0e68561297f0f1fb12e439c9cdf/merged",
>-         "overlay         468G   20G  424G   >- 5% /var/lib/docker/overlay2/>- cfde55b8ad310aeded1e31df95bbb86f4e2da>- 44a3062021be8c26ae7af8d3656/merged",
>-         "shm              64M     0   64M   >- 0% /var/lib/docker/containers/>- 8242c3f3b636841b4649e95bd4573de99fcde>- 3cdcfbd41fd53d71c775f62e70d/mounts/>- shm",
>-         "shm              64M     0   64M   >- 0% /var/lib/docker/containers/>- c4989dd9599987b05733301c7fc5105565894>- 3259d2572859351628d1aeb9533/mounts/>- shm",
>-         "shm              64M     0   64M   >- 0% /var/lib/docker/containers/>- dfa4a08a922a2e5deac537675ac710ee74b16>- 7621e2554380ec0905cff6c7690/mounts/>- shm",
>-         "overlay         468G   20G  424G   >- 5% /var/lib/docker/overlay2/>- 4882283a967a845f17ae1a0331c17fc786f34>- 8a72589e42495282ab70b44ceef/merged",
>-         "overlay         468G   20G  424G   >- 5% /var/lib/docker/overlay2/>- a18419079de7a9067b367cc41e8c4ee89c44d>- 1f764fb6b603738ba294913e383/merged",
>-         "overlay         468G   20G  424G   >- 5% /var/lib/docker/overlay2/>- 809c7225a326b8a3c1296f73096a368765b8a>- 869f3847bb0e5adc55dd4496b95/merged",
>-         "overlay         468G   20G  424G   >- 5% /var/lib/docker/overlay2/>- 1335a3abc52166c2f2780954134588bc54b11>- fd0f646d114990f96fffa188508/merged",
>-         "overlay         468G   20G  424G   >- 5% /var/lib/docker/overlay2/>- 3a3774c28ca39d971344a94dcf524beef92da>- 120537d7c5ad06fc145d6084638/merged",
>-         "shm              64M     0   64M   >- 0% /var/lib/docker/containers/>- 280caef1049bb1b2935f6a2399582e0c62e55>- 3526ea53e8274a0697e4847eb7a/mounts/>- shm",
>-         "shm              64M     0   64M   >- 0% /var/lib/docker/containers/>- 3adb6b31b8087262a17d59a6e684746905952>- 29687bb38ba132079d7c4c46052/mounts/>- shm",
>-         "overlay         468G   20G  424G   >- 5% /var/lib/docker/overlay2/>- 6332402330ac5d437e07d1e365f041064cd94>- 89ce873bb281b0534e2c8a94c7b/merged",
>-         "overlay         468G   20G  424G   >- 5% /var/lib/docker/overlay2/>- 841206317f516fe3584c23117517fb05beebb>- 99efd0182262669899606304d55/merged",
>-         "overlay         468G   20G  424G   >- 5% /var/lib/docker/overlay2/>- a097a6c2d9a73a4c2a82a091e96b1cf19a0df>- 2ec8ba9bb364b8b2218c7e940b4/merged",
>-         "shm              64M     0   64M   >- 0% /var/lib/docker/containers/>- f9545a071ea0a60f54b0a22d54354bb12cc97>- b2cf9b67801b2c42fdc95f820ff/mounts/>- shm",
>-         "overlay         468G   20G  424G   >- 5% /var/lib/docker/overlay2/>- 9fce4b766386a3b78811c6500c34f88bcb6a1>- afc670831f8507426b11326923c/merged",
>-         "total           6.9T  360G  6.3T   >- 6% -"
>-     ]
>- }
>- ok: [node1] => {
>-     "disk_info.stdout_lines": [
>-         "Filesystem      Size  Used Avail >- Use% Mounted on",
>-         "tmpfs           753M  2.7M  750M   >- 1% /run",
>-         "/dev/sda2       109G   12G   92G  >- 11% /",
>-         "tmpfs           3.7G     0  3.7G   >- 0% /dev/shm",
>-         "tmpfs           5.0M  8.0K  5.0M   >- 1% /run/lock",
>-         "efivarfs        128K   97K   27K  >- 79% /sys/firmware/efi/efivars",
>-         "/dev/sda1       1.1G  6.2M  1.1G   >- 1% /boot/efi",
>-         "tmpfs           753M   92K  753M   >- 1% /run/user/120",
>-         "overlay         109G   12G   92G  >- 11% /var/lib/docker/overlay2/>- cc101ccfeee0dac3f6c8190be8ea859c03362>- 89116e059480062b242c3fd65f2/merged",
>-         "shm              64M     0   64M   >- 0% /var/lib/docker/containers/>- 35a1adb64a0fe62b0ec74343c94f7352edae2>- 92f0cdb5cda7c5c84c575431c20/mounts/>- shm",
>-         "overlay         109G   12G   92G  >- 11% /var/lib/docker/overlay2/>- 212584c54e2125a4ed6bdcef0bfacb2526a03>- fb02c538f48b3c65b885474ea02/merged",
>-         "shm              64M     0   64M   >- 0% /var/lib/docker/containers/>- 880cce1c32a03b5bc1a41f1d26f19b250945a>- dab7e28a53aecc6358c2d3135ed/mounts/>- shm",
>-         "overlay         109G   12G   92G  >- 11% /var/lib/docker/overlay2/>- cbec89cd9ac3704bb1eb90c7819c21688534b>- eba1d4cbbe82745d119622d8fd0/merged",
>-         "overlay         109G   12G   92G  >- 11% /var/lib/docker/overlay2/>- 6fcf23b715eb078428f3fb766884312027a6a>- c09c3fe8b3af8d25d43deee0f2f/merged",
>-         "overlay         109G   12G   92G  >- 11% /var/lib/docker/overlay2/>- a0bd14abc2e33a1ed4d3066c910cb9ff511d9>- caf5354d48e06988f50af89f3c0/merged",
>-         "shm              64M     0   64M   >- 0% /var/lib/docker/containers/>- 90d9fee3e0c50d3e98f05a25c1faf33d2cbf1>- 51c006fb525e946d7ba1d21d65e/mounts/>- shm",
>-         "overlay         109G   12G   92G  >- 11% /var/lib/docker/overlay2/>- 64fff73ec1ef613766355de20ab9fc2333a6e>- 8577a811922d072e56815a19909/merged",
>-         "overlay         109G   12G   92G  >- 11% /var/lib/docker/overlay2/>- 2d1c7bf6184ffd7cba34041110f8eba0fd6e8>- 9cb01834de3d56a3752a1d91eb7/merged",
>-         "shm              64M     0   64M   >- 0% /var/lib/docker/containers/>- 8e531f6f847c5d572fcde1dc19582f185b128>- 870af4c67ae741b6140489a0ea3/mounts/>- shm",
>-         "overlay         109G   12G   92G  >- 11% /var/lib/docker/overlay2/>- 6b5d5e50f2b3c5e5e898c05f0da0477fcb8b1>- 63412b1ad3a1e929085593e9c01/merged",
>-         "tmpfs           753M   80K  753M   >- 1% /run/user/1000",
>-         "total           984G  102G  832G  >- 11% -"
>-     ]
>- }
>- ok: [node2] => {
>-     "disk_info.stdout_lines": [
>-         "Filesystem      Size  Used Avail >- Use% Mounted on",
>-         "tmpfs           764M  3.2M  761M   >- 1% /run",
>-         "/dev/sda2       229G   12G  206G   >- 6% /",
>-         "tmpfs           3.8G     0  3.8G   >- 0% /dev/shm",
>-         "tmpfs           5.0M   12K  5.0M   >- 1% /run/lock",
>-         "tmpfs           764M   92K  764M   >- 1% /run/user/120",
>-         "overlay         229G   12G  206G   >- 6% /var/lib/docker/overlay2/>- c410a394da1281e55720a36d117582cfe5e89>- efa67435524b6137ce51478f292/merged",
>-         "overlay         229G   12G  206G   >- 6% /var/lib/docker/overlay2/>- 419b99ed0c90de33b6259bbbdd73bcb87a5e5>- 7be770f7ab48cd6f85d0d49ea9e/merged",
>-         "overlay         229G   12G  206G   >- 6% /var/lib/docker/overlay2/>- e6a408de02f787f43fc98e68ad3b7b5fc85a2>- 4138389eaf5d852e644d0e10407/merged",
>-         "shm              64M     0   64M   >- 0% /var/lib/docker/containers/>- 6a540a0df3c61057d458ecda2bd0f140940b0>- e757eaf401135fb03f46e9dfe23/mounts/>- shm",
>-         "shm              64M     0   64M   >- 0% /var/lib/docker/containers/>- 2d1c9c91968b6ea95fe22b6e62fd9f4ccd8ad>- 2b7340f8542b95b04cbb2bc4cc8/mounts/>- shm",
>-         "shm              64M     0   64M   >- 0% /var/lib/docker/containers/>- d9dc2ca5e520591c0173945e2e61a5a12267f>- 8b1a916de4f1d4072be2a8e5350/mounts/>- shm",
>-         "overlay         229G   12G  206G   >- 6% /var/lib/docker/overlay2/>- cb672f1d078b5af44276beec1bd0ffe82e8cb>- 79e21875f4cee49b5d03b7fb914/merged",
>-         "overlay         229G   12G  206G   >- 6% /var/lib/docker/overlay2/>- f4b4cd1688ab5514a162775e3a62f5d87e71f>- b4b8f99c102f637cb033cd1cfb0/merged",
>-         "overlay         229G   12G  206G   >- 6% /var/lib/docker/overlay2/>- 6f149f940db195a38e22b7ad4a389c039f33d>- f61e010fb17046a3bdad77ee75b/merged",
>-         "overlay         229G   12G  206G   >- 6% /var/lib/docker/overlay2/>- ab595094bcc552c6e30db96d6315118ae85b3>- 98981783ce3c7e0a75d40cea0ae/merged",
>-         "overlay         229G   12G  206G   >- 6% /var/lib/docker/overlay2/>- 028725873a40e3f03f018927d5671885fa0ad>- d9df4661a32abb2377475d077ee/merged",
>-         "overlay         229G   12G  206G   >- 6% /var/lib/docker/overlay2/>- 16c146f65e61522a9c68fdff5aa1073908eca>- 8803aa22a074cd148abf4a49b3a/merged",
>-         "overlay         229G   12G  206G   >- 6% /var/lib/docker/overlay2/>- 250784deb8d1fac726ccf2cb6f742a260201f>- 351a6b0994435cd18a642a65c8f/merged",
>-         "shm              64M     0   64M   >- 0% /var/lib/docker/containers/>- 3d2bf70d2611d6bb03dc5026a209470ac56b4>- 9e475a35254e765b38628defc19/mounts/>- shm",
>-         "shm              64M     0   64M   >- 0% /var/lib/docker/containers/>- 22f10cfc0665d26b466ab6c5b2ce43f403d08>- 99c327d93476e28eee1368789f3/mounts/>- shm",
>-         "shm              64M     0   64M   >- 0% /var/lib/docker/containers/>- b53357a9e205d8c0d2e7366e8e42819582c00>- d4bf5b009634718c5e38912152c/mounts/>- shm",
>-         "shm              64M     0   64M   >- 0% /var/lib/docker/containers/>- 48eebfdd99fc8f129e8149e2dd52ff86409a7>- 15e4033288ec4d4b476d37b701b/mounts/>- shm",
>-         "overlay         229G   12G  206G   >- 6% /var/lib/docker/overlay2/>- 2f860ccee4228b12d2a057e35a2bbc2ab7be6>- 26998ec6af9bd943b32eb86a2a3/merged",
>-         "overlay         229G   12G  206G   >- 6% /var/lib/docker/overlay2/>- 846e8c50018d32557328f3fd289fd9faf3725>- 635fbd5dcde3a3f4a4df3e3fc4c/merged",
>-         "overlay         229G   12G  206G   >- 6% /var/lib/docker/overlay2/>- 5c4d01922f1f60efec4e078d014a02fd8ddea>- 9da31d3d012e7c71dd7edf90f8c/merged",
>-         "overlay         229G   12G  206G   >- 6% /var/lib/docker/overlay2/>- fceaa0045f2023e91baa4735da73cd199ffe2>- 4c6141848e0c3bf9ddd0aad9583/merged",
>-         "tmpfs           764M   80K  764M   >- 1% /run/user/1000",
>-         "total           3.4T  173G  3.1T   >- 6% -"
>-     ]
>- }
>- 
>- PLAY RECAP >- *********************************************>- *********************************************>- ****************master                     : >- ok=7
>-   changed=1    unreachable=0    failed=0    >- skipped=0    rescued=0    ignored=0
>- node1                      : ok=7    >- changed=1    unreachable=0    failed=0    >- skipped=0    rescued=0    ignored=0
>- node2                      : ok=7    >- changed=1    unreachable=0    failed=0    >- skipped=0    rescued=0    ignored=0
</details>


## ufw_status
```console
$ ansible-playbook ufw_status.yml
```

## update_upgrade
```console
$ ansible-playbook update_upgrade
```

## systemctl_status
```console
$ ansible-playbook systemctl_status \
  ---extra-vars "service_name=ssh"
```