# Prototype: Vườn Số Của Bông

Bản mẫu để duyệt giao diện và lộ trình học trước khi fork `Sigmafier/ellaz-games` (xem `docs/research/danh-gia-repo.md`).

Mở `index.html` bằng trình duyệt. Cần có mạng để tải font Google và Three.js 0.160.0 từ jsDelivr. Nếu không tải được Three.js, phòng 3D tự chuyển sang chế độ 2D.

## Quyết định đã chốt

| Hạng mục | Quyết định |
|---|---|
| Nhân vật | Tự thiết kế nhân vật riêng trước, xin license Sanrio sau khi có người dùng. **Không dùng Kuromi** khi chưa có license |
| 3D | Kết hợp 2D và 3D: 3D cho phòng thưởng, bản đồ thế giới và bài học hình khối; 2D cho đếm và tính toán |
| Theme | Hồng là mặc định; có thể đổi sang Bạc hà hoặc Oải hương. Theme chỉ đổi nền và môi trường; **Bông luôn giữ màu hồng** để nhận diện thương hiệu. Mọi màu lấy từ token CSS |
| Cấu trúc | Một hành trình 7 cấp. Mở cấp tiếp theo khi đúng ngay lần đầu 4/5 câu. Sao chỉ thưởng cho câu đúng ngay lần đầu, để bé không đoán bừa |
| Cách trả lời | Cấp 1–4 chọn đáp án; cấp 5–7 dùng bàn phím số, xếp que tính và tia số |
| Thời gian | Không tính giờ. Phụ huynh có thể bật "Thử thách tốc độ": trả lời đúng trước khi hết giờ được thêm sao, không trừ điểm |
| Xếp cấp | Bài kiểm tra đầu vào 8 câu: đúng 2 câu liên tiếp thì lên cấp, sai 1 câu thì xuống. Cấp xếp vào là cấp thấp nhất mà bé sai nhiều hơn đúng. Không báo đúng sai, không tặng sao |

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

## Trò chơi ngoài hành trình

| Trò | Cách chơi | Ghi chú thiết kế |
|---|---|---|
| **Đàn số** | Đàn 8 phím (Đô đến Đô). Mỗi câu, Bông đố một phép tính. Đáp án đúng nằm trên phím của nốt tiếp theo trong câu đầu bài "Ngôi sao lấp lánh", nên bấm đúng là đàn đúng giai điệu. Có 8 ô nhịp, tương ứng 8 phép tính. Bấm sai thì phím đó vẫn kêu theo cao độ của nó, Bông gợi ý; sai lần 2 thì phím đúng nhấp nháy | Giai điệu lấy từ bài dân gian Pháp thế kỷ 18 *Ah! vous dirai-je, maman*, thuộc phạm vi công cộng. Âm thanh tổng hợp bằng Web Audio. Chơi xong có thể nghe lại cả bài hoặc đàn tự do |
| **Bông phiêu lưu** | Bông tự chạy trên đường. Mỗi lượt có 2 cổng số, một trên một dưới. Bé chạm vào cổng có số đúng (hoặc bấm nút "Cổng trên"/"Cổng dưới"). Chọn cổng trên thì Bông bay lên mây. Chạm chỗ khác để Bông nhảy chơi. Mỗi lượt có 6 cổng | Bông dừng lại chờ bé chọn nên không có áp lực thời gian và không có thua. Chọn sai thì Bông chỉ lắc nhẹ và chỉ ra cổng đúng. Vẽ bằng canvas 2D, màu lấy từ token theme. Bàn phím: ↑, ↓, phím cách |

Độ khó của 2 trò đi theo cấp cao nhất bé đã mở: cấp 1–2 cộng trừ trong 10; cấp 3–4 trong 20, có qua 10; từ cấp 5 thêm tìm số còn thiếu. Riêng Bông phiêu lưu có thêm câu số liền trước, liền sau đến 200.

## Rà soát

Biên bản rà soát lỗi logic và giao diện ngày 2026-11-05: `docs/review/ra-soat-2026-11-05.md`.

## Giới hạn đã biết

- Chưa test trên thiết bị thật. Mới kiểm tra bằng Chromium headless ở khổ 1180×820 và 400×860.
- Giọng đọc dùng Web Speech API, chỉ đọc khi thiết bị có giọng tiếng Việt.
- Bông chỉ là nhân vật tạm, không dùng làm nhận diện thương hiệu. Brief đặt hàng họa sĩ nằm trong Claude Docs: "Brief thiết kế nhân vật Bông".
- Tiến độ chỉ lưu trong `localStorage` của trình duyệt.
- Môi trường test headless chỉ đạt khoảng 16 khung hình/giây. Bông phiêu lưu đã được chỉnh để máy yếu vẫn chạy đúng tốc độ, nhưng cần đo lại trên tablet thật.
- Bản chính nên viết lại Bông phiêu lưu bằng Phaser, cùng engine mà ellaz-games đang dùng.
