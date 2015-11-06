/etc/sudoers.d/README

這個並不是/etc/sudoers.d/的說明，而是真的文件。

這份檔案裡面仔細說明sudo的危險，另外也表示這份檔案用來記錄使用sudo的名單，可以用include使用。

檔案裡面有一行(前面是縮排)：
 >--#includedir /etc/sudoers.d
在他的下一行加上：
test	ALL=(ALL:ALL) ALL

之後test就如同直接加在/etc/sudoers一樣，擁有管理員權限了。



檔案權限是：
-r--r-----

和/etc/sudoers一樣