local-hostname : Nếu set trùng instance-id hoặc sử dụng meta-data trên cùng một máy thì khi khởi chạy lại cloud-init ,nó sẽ kiểm tra có trùng instance-id k , nếu tồn tại thì sẽ  bỏ qua các bước config 

```
# create guest VM 
virt-install --name centos \
  --connect qemu:///system \
  --virt-type qemu --memory 2048 --vcpus 2 \
  --boot hd,menu=on \
  --disk path=seed.qcow2,device=cdrom \
  --disk path=centos7.qcow2,device=disk \
  --graphics vnc \
  --os-type Linux --os-variant centos7.0[ubuntu18.04] \
  --network network:default \
  --noautoconsole
  ```
  
  
  
  
