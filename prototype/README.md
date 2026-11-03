# Prototype: Vườn Số Của Bông

Bản mẫu để duyệt giao diện và lộ trình học trước khi fork `Sigmafier/ellaz-games` (xem `docs/research/danh-gia-repo.md`).

Mở `index.html` bằng trình duyệt. Cần có mạng để tải font Google và Three.js 0.160.0 từ jsDelivr. Nếu không tải được Three.js, phòng 3D tự chuyển sang chế độ 2D.

## Quyết định đã chốt

| Hạng mục | Quyết định |
|---|---|
| Nhân vật | Tự thiết kế nhân vật riêng trước, xin license Sanrio sau khi có người dùng. **Không dùng Kuromi** khi chưa có license |
| 3D | Kết hợp 2D và 3D: 3D cho phòng thưởng, bản đồ thế giới và bài học hình khối; 2D cho đếm và tính toán |
| Theme | Hồng là mặc định; có thể đổi sang Bạc hà hoặc Oải hương. Mọi màu lấy từ token CSS |
| Cấu trúc | Một hành trình 7 cấp. Mở cấp tiếp theo khi đúng ngay lần đầu 4/5 câu |
| Cách trả lời | Cấp 1–4 chọn đáp án; cấp 5–7 dùng bàn phím số, xếp que tính và tia số |
| Thời gian | Không tính giờ. Phụ huynh có thể bật "Thử thách tốc độ": trả lời đúng trước khi hết giờ được thêm sao, không trừ điểm |
| Xếp cấp | Bài kiểm tra đầu vào 6 câu theo kiểu bậc thang: đúng thì câu sau khó hơn, sai thì dễ hơn. Không báo đúng sai |

## Thang cấp độ

| Cấp | Nội dung | Hình hỗ trợ (giảm dần trong mỗi lượt) |
|---|---|---|
| 1 | Số đến 20: đếm, nhận biết | Đồ vật chạm để đếm |
| 2 | Cộng trừ trong 10 | Chấm tròn, sau đó chỉ còn chữ số |
| 3 | Cộng trừ trong 20, không qua 10 | Khung 10 ô kép, sau đó chỉ còn chữ số |
| 4 | Làm tròn chục (qua 10) | Bé tự chuyển hoặc bớt chấm trong khung 10 ô, rồi xem cách tách số, cuối cùng tính nhẩm |
| 5 | Số đến 100 | Bó chục và que lẻ, so sánh, số liền trước, liền sau |
| 6 | Số đến 200 | Bó trăm, bó chục, que lẻ, tia số (Bông nhảy tới đúng số), so sánh |
| 7 | Số còn thiếu, toán có lời văn | Bông đọc đề, bé nhập bằng bàn phím số |

Bông đọc số theo quy tắc tiếng Việt: mười lăm, hai mươi mốt, hai mươi tư. Số 105 đọc "một trăm linh năm" hoặc "một trăm lẻ năm", phụ huynh chọn trong phần cài đặt.

## Giới hạn đã biết

- Chưa test trên thiết bị thật. Mới kiểm tra bằng Chromium headless ở khổ 1180×820 và 400×860.
- Giọng đọc dùng Web Speech API, chỉ đọc khi thiết bị có giọng tiếng Việt.
- Bông chỉ là nhân vật tạm, không dùng làm nhận diện thương hiệu.
- Tiến độ chỉ lưu trong `localStorage` của trình duyệt.
- "Đàn số" và "Bông phiêu lưu" mới có ô "Sắp có" trên trang chính, chờ chốt thiết kế.
