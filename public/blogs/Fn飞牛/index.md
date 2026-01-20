# Fn飞牛

## 开启iommu
```
sudo -i
```
```
nano /etc/default/grub #GRUB_CMDLINE_LINUX_DEFAULT="quiet i915.force_probe=7d55 intel_iommu=on iommu=pt"
如果是amd处理器的话,将intel改成amd;修改完成以后,ctrl+s保存,ctrl+x退出即可
```
```
cd /lib/firmware/rtl_nic/
sudo wget https://git.kernel.org/pub/scm/linux/kernel/git/firmware/linux-firmware.git/tree/rtl_nic/rtl8126a-2.fw
```
```
cd /lib/firmware/rtl_nic/
sudo wget https://git.kernel.org/pub/scm/linux/kernel/git/firmware/linux-firmware.git/tree/rtl_nic/rtl8126a-3.fw
```
```
cd /lib/firmware/i915/
sudo wget https://git.kernel.org/pub/scm/linux/kernel/git/firmware/linux-firmware.git/tree/i915/bmg_dmc.bin
```
```
cd /lib/firmware/i915/
sudo wget https://git.kernel.org/pub/scm/linux/kernel/git/firmware/linux-firmware.git/tree/i915/xe2lpd_dmc.bin
```
```
echo -e "vfio\nvfio_iommu_type1\nvfio_pci\nvfio_virqfd" >> /etc/modules

```
```
update-grub
```
```
update-initramfs -u -k all
```
