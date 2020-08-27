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
  
  
 https://docs.openstack.org/image-guide/modify-images.html
  

Create  encrypted password : openssl passwd -1 "password"
[link](https://www.cloudkb.net/change-root-password-kvm-qcow2-image/)

Shadow file format 
[link](https://www.2daygeek.com/understanding-linux-etc-shadow-file-format/#:~:text=The%20%2Fetc%2Fshadow%20file%20stores,less%20of%20a%20security%20risk)


Merge a disk and a qcow2 into one 
[link](https://stackoverflow.com/questions/22913384/transforming-qcows2-snapshot-plus-backing-file-into-standalone-image-file)

