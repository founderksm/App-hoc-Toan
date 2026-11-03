# Prototype: Vườn Số Của Bông

Bản mẫu giao diện để duyệt cảm giác hình ảnh trước khi fork `Sigmafier/ellaz-games` (xem `docs/research/danh-gia-repo.md`).

Mở `index.html` bằng trình duyệt. Cần có mạng để tải font Google và Three.js 0.160.0 từ jsDelivr. Nếu không tải được Three.js, phòng 3D tự chuyển sang chế độ 2D.

## Quyết định đã chốt

| Hạng mục | Quyết định |
|---|---|
| Nhân vật | Tự thiết kế nhân vật riêng trước, xin license Sanrio sau khi có người dùng. **Không dùng Kuromi** khi chưa có license |
| 3D | Kết hợp 2D và 3D: 3D cho phòng thưởng, bản đồ thế giới và bài học hình khối; 2D cho đếm và cộng trừ |
| Theme | Hồng là mặc định; có thể đổi sang Bạc hà hoặc Oải hương. Mọi màu lấy từ token CSS |

## Bản mẫu thể hiện

- **Bông**: nhân vật tạm, vẽ bằng SVG cho bản 2D và bằng khối cầu Three.js cho bản 3D. Bản chính sẽ thuê họa sĩ thiết kế và ký hợp đồng chuyển nhượng quyền tác giả.
- **Đếm dâu**: trẻ chạm từng đồ vật để đếm 1–1, rồi chọn chữ số đúng. Độ khó tự điều chỉnh theo phạm vi 5 → 7 → 10. Trả lời sai không bị trừ điểm, chỉ được gợi ý đếm lại.
- **Phòng của Bông**: dùng sao để mua đồ trang trí. Kéo để xoay phòng, chạm vào Bông để Bông nhảy. Giới hạn 30 khung hình/giây, độ phân giải hiển thị tối đa 1,5x, chỉ chạy khi đang mở màn hình phòng.
- **Âm thanh**: tổng hợp bằng Web Audio nên không có rủi ro license. Giọng đọc dùng Web Speech API, chỉ đọc khi thiết bị có giọng tiếng Việt.

## Giới hạn đã biết

- Chưa test trên thiết bị thật. Mới kiểm tra bằng Chromium headless ở khổ 1180×820 và 400×860.
- Bông chỉ là nhân vật tạm, không dùng làm nhận diện thương hiệu.
- Sao và đồ trong phòng chỉ lưu trong `localStorage` của trình duyệt.
