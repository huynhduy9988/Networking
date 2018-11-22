# Static root & Dynamic root

## Mục lục
[I. Static root](#staticroot)

[II. Dynamic root](#dynamicroot)

<a name="staticroot"></a>
## I. Static root

### 1. Static root

**- Khái niệm:**

Static root là khai báo thủ công các tuyến đường trên bảng định tuyến

**- Ưu điểm:**

Tăng tính bảo mật do mọi thông tin định tuyến do người quản lý cấu hình
Tiết kiệm tài nguyên RAM, CPU do không phải tính toán nhiều

**- Nhược điểm:**

Không có khả năng mở rộng với Topo lớn.

**- Command:**

`iproute networkdestination netmask nexthop/exitinterface`

**- AD**

Nexthop AD=1

Exit AD=0

=> Chỉnh AD dự phòng trong định tuyến động

### 2. Default root

**- Khái niệm**

Default root là 1 dạng đặc biệt của static root. Default root thông thường được sử dụng trong mạng LAN nhằm đi ra Internet, bởi vì Internet vó rất nhiều ROUTE và Router không thể học hết được tất cả các ROUTE đó nên phải cần 1 Default root để Router biết chuyển gói tín có Destination không có trong bảng định tuyến của nó đi đâu (Ở đây sẽ đi ra Internet)

**- Commmand**

`iproute 0.0.0.0 0.0.0.0 nexthop/exitinterface`

<a name="dynamicroot"></a>
## II. Dynamic root
