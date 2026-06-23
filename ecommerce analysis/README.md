# Olist E-Commerce Dashboard

Dashboard Power BI phân tích bộ dữ liệu thương mại điện tử Olist của Brazil, tập trung vào tăng trưởng doanh thu, hiệu quả giao hàng, trải nghiệm khách hàng, danh mục sản phẩm và rủi ro theo người bán.

## Tổng Quan Dữ Liệu

Bộ dữ liệu Olist ghi nhận quy trình giao dịch trên nền tảng marketplace từ lúc khách hàng đặt hàng, thanh toán, nhận hàng đến khi đánh giá đơn hàng. Dữ liệu bao gồm thông tin về đơn hàng, khách hàng, người bán, sản phẩm, thanh toán, vận chuyển và đánh giá.

Phạm vi dữ liệu: giai đoạn 2017-2018, khoảng 100 nghìn đơn hàng từ nhiều khu vực tại Brazil.

## Mục Tiêu Phân Tích

- Theo dõi tăng trưởng doanh thu và số lượng đơn hàng.
- Đánh giá mức độ hài lòng của khách hàng qua review.
- Xác định ảnh hưởng của giao hàng trễ đến đánh giá tiêu cực.
- Khoanh vùng rủi ro theo khu vực, danh mục sản phẩm và seller.
- Đề xuất hướng cải thiện vận hành và trải nghiệm khách hàng.

## Chỉ Số Chính

| Nhóm phân tích | Chỉ số |
|---|---|
| Kinh doanh | Total Sales, Total Orders, Total Customers |
| Trải nghiệm khách hàng | Avg Review Score, % 1-Star Reviews, % 5-Star Reviews |
| Giao hàng | Delay Rate, On-time %, Avg Delivery Days, Avg Delivery Promise |
| Sản phẩm | Product Category Orders, Delay Rate by Category, % 1-Star by Category |
| Seller | Seller Delay Rate, Seller % 1-Star Reviews, Priority Level |
| Rủi ro | Critical Sellers, At-risk Sellers, Cancellation Rate |

## Insight Chính

### 1. Tăng trưởng tốt nhưng trải nghiệm khách hàng có dấu hiệu suy giảm

Marketplace đạt 13.18M BRL doanh số với khoảng 96K đơn hàng. Doanh số tăng rõ rệt từ đầu năm 2017 và ổn định quanh mức 0.9M-1.1M BRL từ giữa năm 2018.

Tuy nhiên, dù 62.32% review là 5 sao, tỷ lệ đánh giá 1 sao vẫn ở mức đáng kể 15.63%. Tỷ lệ 1 sao có xu hướng tăng trong các giai đoạn đơn hàng tăng mạnh, cho thấy tăng trưởng quy mô đang đi kèm áp lực lên chất lượng trải nghiệm.

### 2. Giao hàng trễ là nguyên nhân quan trọng gây review tiêu cực

Delay Rate trung bình toàn kỳ là 8.13% và có xu hướng tăng. Đơn hàng giao trễ có tỷ lệ 1 sao là 49.21%, cao khoảng 4.5 lần so với đơn giao đúng hạn. Đồng thời, tỷ lệ 5 sao giảm từ 66.85% ở nhóm giao đúng hạn xuống còn 28.28% ở nhóm giao trễ.

Một điểm đáng chú ý là đánh giá tiêu cực tăng mạnh khi thời gian giao hàng vượt mốc 21 ngày, trong khi Avg Delivery Promise hiện tại là 24.28 ngày. Điều này cho thấy cam kết giao hàng trung bình đang nằm trong vùng rủi ro cao đối với trải nghiệm khách hàng.

### 3. Vấn đề giao hàng tập trung ở một số khu vực

Các bang AL, MA, PI, CE, SE và BA có delay rate cao bất thường, dao động khoảng 14%-24%. Điều này cho thấy vấn đề giao hàng không phân bổ đều toàn hệ thống mà tập trung ở một số khu vực cụ thể.

### 4. Một số danh mục sản phẩm có tỷ lệ review xấu cao

Các category cần chú ý gồm:

- `bed_bath_table`
- `computers_accessories`
- `construction_tools_construction`
- `furniture_decor`
- `office_furniture`

Trong đó, `office_furniture` và `construction_tools_construction` có liên hệ rõ với giao hàng trễ. Ngược lại, `bed_bath_table`, `computers_accessories` và `furniture_decor` vẫn có tỷ lệ 1 sao cao dù delay rate không quá lớn, gợi ý rằng vấn đề có thể đến từ chất lượng sản phẩm hoặc seller.

### 5. Rủi ro seller tập trung ở nhóm At-risk

Trong khoảng 3K seller, chỉ 27 seller đạt nhóm Star Seller, 21 seller thuộc nhóm Critical và khoảng 1K seller thuộc nhóm At-risk. Nhóm At-risk chiếm tỷ trọng lớn hơn nhiều so với nhóm Critical, vì vậy cần cơ chế theo dõi và cảnh báo sớm thay vì chỉ xử lý các trường hợp nghiêm trọng nhất.

Rủi ro seller tập trung mạnh tại bang SP, đồng thời một phần seller at-risk đang bán các category problematic như `furniture_decor` và `computers_accessories`.

## Kết Luận Và Đề Xuất

Nền tảng đang tăng trưởng tốt về doanh số và số lượng đơn hàng, nhưng trải nghiệm khách hàng đang chịu áp lực từ giao hàng trễ, một số danh mục sản phẩm có review xấu và nhóm seller at-risk.

Đề xuất ưu tiên:

- Rút ngắn Avg Delivery Promise xuống dưới 21 ngày.
- Ưu tiên cải thiện logistics tại AL, MA, PI, CE, SE và BA.
- Theo dõi cảnh báo khi delay rate vượt mức trung bình 8.13%.
- Rà soát `office_furniture` và `construction_tools_construction` về giao hàng.
- Rà soát chất lượng sản phẩm/seller với `bed_bath_table`, `computers_accessories` và `furniture_decor`.
- Xây dựng cơ chế theo dõi riêng cho nhóm seller At-risk, đặc biệt tại SP.

## File

```text
ecommerce analysis/
├── ecom.pbix
├── first page.png
└── README.md
```
