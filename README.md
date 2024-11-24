# Hướng dẫn Bài Lab PRTG

## **Mục tiêu**
- Thiết lập mạng và sử dụng PRTG để giám sát lưu lượng.

---

## **Yêu cầu**
- **Thiết bị**:
  - Router (R1)
  - Máy tính (PC1, PC2)
- **Phần mềm**:
  - PRTG Network Monitor

---

## **Hướng dẫn thực hiện**

### **1. Thiết lập Topo mạng**
- Kết nối các thiết bị theo sơ đồ:
  - **Router R1** nối với **PC1** và **PC2**.
- Cấu hình các thiết bị để đảm bảo có thể giao tiếp qua mạng.
  1. **Router R1**:
    conf t
    int f0/0
    ip add dhcp
    no shut
    exit
    int f1/0
    ip add 10.10.10.1 255.255.255.0
    no shut
    exit
  2. **PC1**
    ip 10.10.10.3 255.255.255.0 10.10.10.1
  3. **PC2**
    ip 10.10.10.7 255.255.255.0 10.10.10.1 

### **2. Kết nối với Router và PC**
- Mở **Console** trên Router R1.
- Thiết lập thông số mạng trên **PC1** và **PC2** để đảm bảo chúng có thể giao tiếp với Router.

### **3. Thêm thiết bị vào PRTG**
- Truy cập giao diện quản lý của PRTG.
- Thực hiện các bước sau:
  1. Thêm thiết bị (**Add Device**) tương ứng với Router R1 và các PC.
  2. Đảm bảo các thiết bị được cấu hình chính xác để giao tiếp với PRTG.

### **4. Thêm Sensor giám sát**
- Chọn một thiết bị đã được thêm vào PRTG.
- Thực hiện:
  1. Nhấn **Add Sensor**.
  2. Chọn **SNMP Traffic** để giám sát lưu lượng mạng.

### **5. Theo dõi mạng**
- Sau khi thêm thành công Sensor:
  - Theo dõi các biểu đồ và thông tin mạng trực tiếp trên giao diện của PRTG.
  - Kiểm tra lưu lượng, trạng thái thiết bị, và các thông số khác.

---

## **Kết quả mong đợi**
- Hệ thống mạng được giám sát hiệu quả thông qua PRTG.
- Các biểu đồ lưu lượng và thông tin mạng hiển thị rõ ràng.

---

## **Ghi chú**
- Đảm bảo các thiết bị được cấu hình đúng chuẩn.
- Kiểm tra kết nối mạng trước khi thêm thiết bị vào PRTG.

