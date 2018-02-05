## VNC là gì 

Virtual Network Computing (VNC) là hệ thống chia sẻ giao diện màn hình qua giao thức  [Remote Frame Buffer protocol (RFB)](https://en.wikipedia.org/wiki/RFB_protocol) để điều khiển từ xa một máy tính khác. 
Nó truyền các sự kiện bàn phím, chuột từ một máy tính sang máy tính khác và cập nhật sự thay đổi của màn hình. 


## Hoạt động 
VNC là một nền tảng độc lập, sử dụng mô hình client/server. Nhiều client có thể kết nối tới một server trong cùng một thời điểm. 

3 thành phần : 
- VNC server : là chương trình chia sẻ màn hình và cho phép client điều khiển nó 
- VNC client (hoặc viewer) : là chương trình hiển thị dữ liệu từ màn hình máy remote 
- VNC protocol (RFB protocol) : giao thức rất đơn giản, dựa trên truyền một hình ảnh từ server sang client và thông báo sự kiện từ client sang server. 
 
VNC Client (view) sẽ chia sẻ input (bàn phím, di chuyển chuột, click chuột, ...) với VNC Server. VNC Server ghi lại nội dung hiển thị và chia sẻ cho VNC Client. 

## Ưu nhược điểm 

### Ưu điểm 
- Kết nối máy tính từ xa
- Sử dụng được trên laptop, smart phone 

### Nhược điểm 
- Cần băng thông đủ lớn 
- Thao tác đôi lúc hơi chậm 
- Kém bảo mật 

## Sản phẩm 

Một số chương trình ứng dụng giao thức VNC : UltraVNC, RealVNC, TightVNC, ...

Chương trình hoạt động tương tự Windows Remote Desktop của M$ sử dụng giao thức Remote Desktop Protocol (RDP) 

## NoVNC 

NoVNC là VNC Client, sử dụng HTML5 ([Websocket](https://en.wikipedia.org/wiki/WebSocket), [Canvas](https://dev.w3.org/html5/2dcontext-LC/)) hỗ trợ mã hóa. NoVNC chạy tốt trên các trình duyệt phổ biến hiện nay bao gồm cả trình duyệt trên mobile (iOS và Android) 

Github : https://github.com/novnc/noVNC

Các công ty đang sử dụng :  OpenStack, OpenNebula, LibVNCServer, ThinLinc, ...

Tính năng : 
- Hỗ trợ tất cả các trình duyệt phổ biến bao gồm cả mobile 
- Hỗ trợ mã hóa VNC : raw, copyrect, rre, hextile, tight, tightPNG
- Hỗ trợ scaling, clipping và resizing desktop
- Hiển thị con trỏ máy remote 
- Clipboard copy/paste 
- Giấy phép [MPL 2.0](https://www.mozilla.org/en-US/MPL/2.0/)




