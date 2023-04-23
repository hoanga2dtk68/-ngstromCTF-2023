# Admiral Shark
thực hiện mở file đã cho bằng wireshark và follow TCP stream để lấy thêm thông tin
![image](https://user-images.githubusercontent.com/110059218/233825995-40919488-6cea-4a7c-b85a-a162b795c60d.png)
luồng stream 1 đã cho thông tin mở luồng stream quan trọng ở dạng raw
![image](https://user-images.githubusercontent.com/110059218/233826026-2efd18eb-3e75-4245-bd35-5a7fbe4c28f7.png)
ở luồng stream 2 thấy có đuôi .xml
![image](https://user-images.githubusercontent.com/110059218/233826261-18a36431-b115-490e-9723-746f9d862209.png)
đổi sang dạng raw thấy có hex dạng 50 4b 03 04 thì chắc chắn đây là file excel + thêm .xml ở đằng trước, lưu về và thêm header ở đầu mờ file excel sẽ lấy được flag
![image](https://user-images.githubusercontent.com/110059218/233826383-032fedc4-2b2c-402e-a09d-b4a263d475e7.png)
flag: actf{wireshark_in_space}
