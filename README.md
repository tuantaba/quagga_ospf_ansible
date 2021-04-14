# quagga_ospf_ansible
Setup software Router using Quagga

#Nguyên tắc hoạt động của OSPF
Hoạt động theo 5 phần tách biệt, 

- Thiệt lập quan hệ láng giềng với các Router lân cận.
- Chọn lựa DR và BDR nếu cần thiết. (với kiểu mạng PTP trong OSPF thì không cần quan tâm tới DR và BDR).
- Khám phá các tuyến đường.
- Lựa chọn các tuyến tối ưu để sử dụng.
- Duy trì thông tin định tuyến.


Dùng mô hình mạng Pont-to-Point
Dùng PTP vì:
- Tính đơn giản. (đơn giản cấu hình, đơn giản xử lý lỗi.
- Không cần mở rộng thành các miền OSPF (OSPF Area).
- Lượng Router ít nên ít routes.
- Không cần chú ý tới trạng thái bầu chọn DR, BDR trên Router, vì khi đó các Router trong mạng là ngang hàng nhau.
