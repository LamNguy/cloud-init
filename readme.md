Note : Tại sao cloud-init không chạy khi boot máy?\
local-hostname: Nếu set trùng instance-id hoặc sử dụng meta-data trên cùng một máy thì khi khởi chạy lại cloud-init ,nó sẽ kiểm tra có trùng instance-id k , nếu tồn tại thì sẽ  bỏ qua các bước config 


  
 https://docs.openstack.org/image-guide/modify-images.html
  

Create  encrypted password : openssl passwd -1 "password"
[link](https://www.cloudkb.net/change-root-password-kvm-qcow2-image/)

Shadow file format 
[link](https://www.2daygeek.com/understanding-linux-etc-shadow-file-format/#:~:text=The%20%2Fetc%2Fshadow%20file%20stores,less%20of%20a%20security%20risk)

Merge a disk and a qcow2 into one 
[link](https://stackoverflow.com/questions/22913384/transforming-qcows2-snapshot-plus-backing-file-into-standalone-image-file)

