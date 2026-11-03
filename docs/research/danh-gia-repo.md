# Đánh giá repo mã nguồn mở: Web app học toán tư duy cho trẻ 5–6 tuổi

> Ngày thu thập dữ liệu: 2026-11-03 · Dữ liệu thô và lý do loại từng repo: [`candidates.json`](./candidates.json)

## 1. Tóm tắt

| Hạng | Repo | Điểm /100 | Vai trò phù hợp |
|---|---|---|---|
| 1 | [Sigmafier/ellaz-games](https://github.com/Sigmafier/ellaz-games) | **76** | **Nên fork làm nền**: đúng độ tuổi và có kiến trúc tốt nhất |
| 2 | [JesseRWeigel/battlemath](https://github.com/JesseRWeigel/battlemath) | **75** | Repo trưởng thành nhất, cộng đồng mạnh nhất; phương án thay thế nếu ưu tiên độ ổn định |
| 3 | [guyellis/learn](https://github.com/guyellis/learn) | **64** | Kỹ thuật chắc chắn, nhưng thiên về luyện tính hơn là chơi |

**Kết luận chính:** Không có repo nào vừa có cộng đồng lớn vừa đúng độ tuổi 5–6.
- Các repo có nhiều sao và người đóng góp (battlemath, learn) là game luyện tính cho trẻ từ 6 đến 10–12 tuổi.
- Các repo dạy đúng "tiền số học" cho 5–6 tuổi (đếm, nhận biết nhanh số lượng, ghép số với nhóm đồ vật, quy luật) đều mới và chỉ có 0–1 sao.

Vì anh/chị sẽ fork làm nền, chất lượng nội dung và kiến trúc quan trọng hơn số sao. Một khi đã fork, mã nguồn thuộc quyền kiểm soát của mình, nên việc tác giả gốc có tiếp tục duy trì hay không ít ảnh hưởng hơn. Vì vậy **ellaz-games** đứng hạng 1, dù chỉ hơn battlemath 1 điểm.

---

## 2. Phương pháp và mức độ xác minh

### Quy trình lọc

| Bước | Số lượng | Cách làm |
|---|---|---|
| Quét | 2.267 repo (không trùng) | 70 truy vấn GitHub Search (tiếng Anh, tiếng Việt, theo topic) và web search |
| Lọc cứng | 211 repo | Web thuần, license thoáng, liên quan trẻ em và toán |
| Lọc tay | khoảng 30 repo | Đọc README, LICENSE, lịch sử git |
| Đánh giá sâu | 6 repo | Đọc mã nguồn, cấu trúc, i18n, nguồn gốc hình ảnh/âm thanh, test |

### Trọng số chấm điểm (đã duyệt)

| Mã | Tiêu chí | Trọng số |
|---|---|---|
| A | Phù hợp độ tuổi và phương pháp dạy | 25 |
| B | Tính game và trải nghiệm cho trẻ | 20 |
| C | Kiến trúc dễ mở rộng | 20 |
| D | Độ tin cậy cộng đồng (sao, fork, số người đóng góp) | 15 |
| E | Còn được bảo trì | 10 |
| F | Dễ Việt hóa | 10 |

### Mức độ xác minh

| Thông tin | Trạng thái |
|---|---|
| Sao, fork, license SPDX, ngày push gần nhất | **Đã xác minh** qua GitHub API ngày 2026-11-03 |
| Số commit, số tác giả, ngày commit | **Đã xác minh** từ lịch sử git sau khi clone |
| Nội dung file LICENSE, cấu trúc code, nguồn gốc asset | **Đã xác minh** bằng cách đọc mã nguồn |
| Chạy thử, giao diện, độ mượt | **Chưa xác minh** (xem mục 8) |
| Điểm số A–F | **Đánh giá chuyên môn** dựa trên dữ liệu ở trên, không phải số đo khách quan |

---

## 3. Bảng điểm 6 repo đánh giá sâu

| Repo | A /25 | B /20 | C /20 | D /15 | E /10 | F /10 | **Tổng** |
|---|---|---|---|---|---|---|---|
| Sigmafier/ellaz-games | 23 | 18 | 16 | 3 | 7 | 9 | **76** |
| JesseRWeigel/battlemath | 14 | 17 | 12 | 14 | 9 | 9 | **75** |
| guyellis/learn | 12 | 9 | 17 | 12 | 9 | 5 | **64** |
| ShazMoghaddam/Math-Adventure | 22 | 18 | 6 | 2 | 6 | 4 | 58 |
| timmalich/edukiz | 12 | 13 | 13 | 8 | 8 | 4 | 58 |
| KorbinianP/BlitzCount | 17 | 14 | 10 | 1 | 5 | 8 | 55 |

### Số liệu nền

| Repo | Sao | Fork | License | Công nghệ | Commit | Tác giả | Hoạt động |
|---|---|---|---|---|---|---|---|
| ellaz-games | 1 | 2 | MIT | TS, Preact/React, Phaser 4, Vite, PWA | 61 | 2 | 09/2026 → 10/2026 |
| battlemath | 38 | 28 | MIT | TS, React 18, Vite, Vitest, Cypress, PWA | 272 | 18 | 03/2019 → 11/2026 |
| learn | 46 | 8 | MIT | TS strict, React 19, MUI 9, Vite | 979 (683 bot) | 5 | 10/2016 → 10/2026 |
| Math-Adventure | 0 | 0 | MIT | Vanilla JS, PWA | 17 | 2 | 03/2026 → 10/2026 |
| edukiz | 14 | 16 | MIT | Vue 3, Vite, PWA | 213 | 1 | 10/2020 → 10/2026 |
| BlitzCount | 0 | 0 | MIT | Vanilla JS, PWA | 13 | 1 | 09/2026 |

### Phân tích độ nhạy

ellaz và battlemath chỉ chênh nhau 1 điểm, nên thứ hạng phụ thuộc vào trọng số:
- Nếu tăng trọng số cộng đồng (D) từ 15 lên 25, battlemath lên hạng 1.
- Nếu tăng trọng số độ tuổi (A) lên 30, ellaz bỏ xa.

Với mục tiêu "đúng 5–6 tuổi, fork làm nền", trọng số hiện tại là hợp lý.

---

## 4. Chi tiết top 3

### Hạng 1 — Sigmafier/ellaz-games (76 điểm)

**Là gì:** Cổng game trình duyệt (ellaz.fun) có một nhóm game riêng cho trẻ nhỏ. Chạy offline, không quảng cáo, không cần tài khoản.

**Nội dung phù hợp 5–6 tuổi** (đã xác minh trong code):
- **Toán** (`src/games/math/logic.ts`): có 7 cấp, chia làm 2 nhóm.
  - Tiền số học cho 4–5 tuổi: đếm nhóm hình (1–10), ghép số với nhóm đồ vật (1–6), cộng/trừ bằng hình (1–10).
  - Số học cho 6 tuổi trở lên: cộng/trừ trong phạm vi 5, 10, 20, và phép nhân.
- **Quy luật "What comes next?"** (`sequence`): viết riêng cho 4–6 tuổi. Đáp án nhiễu được chọn có chủ đích sư phạm, không chọn ngẫu nhiên.
- **Ghép bóng với hình** (`shadows`), **xếp màu vào ống** (`sort`), **mê cung**, **trí nhớ**: đều rèn tư duy logic và không gian, không cần biết đọc, không giới hạn thời gian.
- Có hệ thống xu, sao và căn phòng để trẻ trang trí, tạo động lực chơi tiếp.

**Điểm mạnh:**
- Kiến trúc tốt nhất trong các repo đã xem. Mỗi game gồm một file `logic.ts` thuần (không dùng DOM hay framework, dùng bộ sinh số ngẫu nhiên có thể seed) và một renderer riêng. Có 338 file test, kể cả test tự động chặn việc file logic import DOM.
- Đã có sẵn 12 ngôn ngữ, mỗi ngôn ngữ một file trong `src/i18n/dict/`. Thêm tiếng Việt chỉ cần tạo thêm file `vi.ts`.
- Hình ảnh trong nhóm game trẻ em chủ yếu là emoji của hệ thống. Font dùng license SIL OFL. Danh sách từ thuộc public domain và có ghi chú nguồn gốc (`NOTICE.md`). Rủi ro license asset thấp.

**Điểm yếu và rủi ro:**

| Rủi ro | Mức | Cách xử lý |
|---|---|---|
| Repo mới 2 tháng, 1 sao, là mirror tự động từ repo private, không nhận PR | Trung bình | Fork rồi phát triển độc lập, không trông chờ upstream |
| Codebase lớn: khoảng 170 nghìn dòng TS, 49 game, trong đó 24 game cho mọi lứa tuổi (cờ vua, survivors…) và 25 game cho trẻ em; chỉ 6–8 game liên quan trực tiếp tới toán và tư duy | Trung bình | Bước đầu tiên là cắt xuống chỉ còn nhóm game toán và tư duy |
| Có PostHog analytics và sao lưu Firestore (ẩn danh, thiết kế theo COPPA) | Cao về pháp lý | Gỡ bỏ, hoặc thay bằng analytics tự host, để tuân thủ Nghị định 13/2023/NĐ-CP về dữ liệu cá nhân |
| Dùng song song Preact, React và Phaser | Thấp | Giữ nguyên lúc đầu; xem xét thống nhất sau |
| Giọng đọc dùng Web Speech API | Trung bình | Tiếng Việt trên thiết bị rẻ đọc kém, nên thu âm sẵn các câu nhắc quan trọng |

**Công sức Việt hóa** (ước tính): khoảng 156 khóa giao diện, cộng chữ trong từng game và các trang nội dung SEO. Khoảng 3–5 ngày công cho nhóm game trẻ em, chưa tính thu âm.

---

### Hạng 2 — JesseRWeigel/battlemath (75 điểm)

**Là gì:** Game luyện tính theo kiểu chiến đấu. Mỗi câu trả lời đúng là một đòn đánh vào quái vật. Có màn chơi, boss, thử thách hằng ngày, gợi ý từng bước, hướng dẫn chơi và bàn phím số trên màn hình.

**Nội dung so với độ tuổi 5–6:**
- Mức Easy (số 1–9) với phép cộng/trừ hợp với trẻ 6 tuổi. Không có phần tiền số học (đếm đồ vật, nhận biết nhanh số lượng, hình khối, quy luật).
- Mỗi câu có đồng hồ 30 giây (màn boss 20 giây), giá trị viết cứng trong `App.tsx:466`. Áp lực thời gian không phù hợp trẻ 5 tuổi.

**Điểm mạnh:**
- Trưởng thành nhất: 7 năm phát triển, 18 người đóng góp, 28 fork, vẫn commit đến tháng 11/2026.
- i18n có kiểu dữ liệu chặt (`src/i18n/types.ts`), đã có tiếng Anh, Tây Ban Nha, Pháp, khoảng 57 khóa. Thêm tiếng Việt khoảng 0,5 ngày (ước tính).
- Có CI, Vitest, Cypress E2E, CODE_OF_CONDUCT và CONTRIBUTING.

**Điểm yếu và rủi ro:**

| Rủi ro | Mức | Cách xử lý |
|---|---|---|
| **Âm thanh và nhạc nền tạo bằng MusicGen** (`scripts/generate_sounds.py`, commit #175). Trọng số MusicGen có license CC-BY-NC 4.0; việc dùng âm thanh do nó tạo ra để kinh doanh chưa rõ ràng | **Cao** | Thay toàn bộ 11 file âm thanh bằng nguồn CC0 hoặc tự sản xuất trước khi thương mại hóa |
| Hình nhân vật tạo bằng FLUX.1-schnell (Apache-2.0) | Thấp | Giữ lại được; nên tham vấn pháp chế về quyền với hình do AI tạo |
| Logic dồn vào `App.tsx` (1.748 dòng) và `AppReducer.ts` (924 dòng) | Trung bình | Tách thành module trước khi thêm game mới |
| Có dependency `react-native-web` không cần thiết | Thấp | Gỡ bỏ |

**Nếu chọn battlemath làm nền:** cần tự viết thêm toàn bộ phần tiền số học (đếm, so sánh nhiều/ít, ghép số với nhóm đồ vật, quy luật) và chế độ không tính giờ cho trẻ 5 tuổi. Đây là phần việc lớn nhất.

---

### Hạng 3 — guyellis/learn (64 điểm)

**Là gì:** App luyện tính cho trẻ 5–12 tuổi. Tác giả là phụ huynh, làm cho con mình dùng từ năm 2016.

**Điểm mạnh:**
- Kỹ thuật chắc chắn: TypeScript strict, ngưỡng coverage bắt buộc, lint không cho phép cảnh báo, quy tắc làm việc ghi rõ trong `AGENTS.md`.
- Trả lời bằng nút chọn đáp án lớn, dùng tốt trên màn hình cảm ứng. Có cấp độ từ A trở lên, huy hiệu và lịch sử điểm.

**Điểm yếu:**
- Giao diện kiểu bài tập, nhiều chữ (ví dụ "Time Left: 599 seconds"), không có nhân vật hay câu chuyện. Yếu tố game thấp nhất trong 6 repo (9/20).
- Không có cơ chế đa ngôn ngữ, chữ viết cứng trong code (F 5/10).
- Khoảng 70% commit là bot cập nhật dependency; hoạt động của người thật ít hơn số commit cho thấy.

**Vai trò hợp lý:** tham khảo bộ sinh bài toán theo cấp độ (`src/learn/math/drill/helper-problems.ts`) và cách tổ chức quy trình chất lượng. Không nên dùng làm nền cho sản phẩm game hóa.

---

## 5. Ngoài top 3 nhưng đáng tham khảo

| Repo | Lấy được gì | Vì sao không vào top 3 |
|---|---|---|
| [ShazMoghaddam/Math-Adventure](https://github.com/ShazMoghaddam/Math-Adventure) | **Lộ trình nội dung đúng 4–7 tuổi nhất**: thế giới dạy đếm và nhận biết nhanh số lượng, mặt xúc xắc, tia số, tìm số còn thiếu, nhân vật thỏ Benny bằng SVG, âm thanh Web Audio (không rủi ro license) | Toàn bộ logic trong một file `script.js` 1.209 dòng viết kiểu nén, biến toàn cục, không test, không i18n. Không mở rộng được |
| [KorbinianP/BlitzCount](https://github.com/KorbinianP/BlitzCount) | Mini-game nhận biết nhanh số lượng 0–12, bàn phím số rút gọn cho trẻ mẫu giáo, đã có i18n en/de | Chỉ dạy một kỹ năng, 1 tác giả, 13 commit |
| [timmalich/edukiz](https://github.com/timmalich/edukiz) | Game kéo thả, trí nhớ; kỷ luật test (coverage 95%) | Chủ yếu dạy chữ; 339 file giọng đọc tiếng Đức không rõ nguồn gốc |
| [brwang04-MAML/storm-chaser](https://github.com/brwang04-MAML/storm-chaser) | Mẫu **bài đánh giá đầu vào** cho 3–5 tuổi, bám theo khung chuẩn mầm non California (16 năng lực) | Là công cụ đánh giá, không phải game học |
| [paulmm/make-it-go](https://github.com/paulmm/make-it-go) | Tư duy tuần tự và logic cho 3–7 tuổi, không cần đọc hay gõ | Dạy tư duy lập trình, không phải toán |
| [phetsims/number-play](https://github.com/phetsims/number-play), [KDE/gcompris](https://github.com/KDE/gcompris) | Chuẩn mực sư phạm số học sớm | License GPL; GCompris không phải web |

## 6. Bị loại vì license (bài học khi thương mại hóa)

| Repo | Lý do |
|---|---|
| YasienDwieb/kids-games | License **PolyForm Shield**: cấm làm sản phẩm cạnh tranh với tác giả |
| binolgeorge/joju-learn | Code MIT nhưng **nội dung và hình ảnh CC BY-NC**, đúng loại bẫy đã cảnh báo trong kế hoạch |
| jkanev/educational-html-games | **CC BY-NC-ND**: cấm thương mại, cấm chỉnh sửa |
| kingsmath/web-games, vnglst/tafels.app, jaysavsani07/math-metrix | Cấm thương mại hoặc không có license |

Danh sách đầy đủ 25 repo bị loại kèm lý do nằm trong [`candidates.json`](./candidates.json).

---

## 7. Đề xuất

### Phương án chính: fork ellaz-games, cắt gọn rồi Việt hóa

| Ưu điểm | Nhược điểm |
|---|---|
| Nội dung tiền số học và tư duy logic đúng 5–6 tuổi đã có sẵn | Upstream chưa được kiểm chứng theo thời gian (2 tháng tuổi) |
| Kiến trúc tách logic khỏi giao diện, dễ thêm game mới, dễ test | Phải cắt bỏ phần lớn code không liên quan, cần một kỹ sư senior làm |
| i18n theo từng file ngôn ngữ, Việt hóa nhanh | Sẽ bỏ khoảng 40 trên 49 game; phải xử lý analytics cho đúng luật Việt Nam |
| Rủi ro license asset thấp | |

### Phương án thay thế: fork battlemath, viết thêm module tiền số học

Chọn phương án này nếu ưu tiên nền tảng có cộng đồng lâu năm. Đổi lại, phải tự viết phần nội dung quan trọng nhất cho 5–6 tuổi và phải thay toàn bộ âm thanh.

### Cách tận dụng tối đa

Lấy **ellaz-games** làm nền và lấy ý tưởng từ các repo khác:
- Từ Math-Adventure: cấu trúc các "thế giới" theo độ tuổi và các dạng câu hỏi (xúc xắc, tia số, tìm số còn thiếu).
- Từ battlemath: vòng lặp động lực (màn chơi, boss, thử thách hằng ngày).
- Từ storm-chaser: bài đánh giá đầu vào để xếp trình độ cho trẻ.

Code các repo này đều MIT nên có thể tham khảo, nhưng phải giữ thông báo bản quyền khi copy code.

---

## 8. Hạn chế của báo cáo

- **Chưa chạy thử app nào.** Môi trường làm việc đã chặn:
  - Cài đặt và build mã nguồn bên thứ ba (vì lý do bảo mật).
  - Truy cập các trang demo (`*.github.io`, `ellaz.fun`, `learn.headvert.com`…) qua network policy.
- Vì vậy điểm B (tính game và trải nghiệm) dựa trên code, README và ảnh chụp do tác giả đăng, chưa được kiểm chứng bằng trải nghiệm thật.
- **Đề xuất bổ sung:** trước khi chốt fork, anh/chị (hoặc một phụ huynh có con 5–6 tuổi) mở thử 3 demo sau trên tablet khoảng 15 phút mỗi app:
  - [ellaz.fun](https://ellaz.fun/), nhóm 🧸 "For kids"
  - [battlemath](https://jesserweigel.github.io/battlemath/)
  - [Math-Adventure](https://shazmoghaddam.github.io/Math-Adventure/)
- Số sao trong mảng này rất thấp (cao nhất 46), nên tiêu chí cộng đồng phân biệt kém.
- Phần nhận định pháp lý (MusicGen, PolyForm, CC BY-NC, Nghị định 13/2023) là thông tin kỹ thuật, không thay cho tư vấn pháp chế.

## 9. Bước tiếp theo (nếu duyệt phương án chính)

1. Fork `Sigmafier/ellaz-games` về `founderksm`, kiểm tra build và chạy toàn bộ test trên máy local hoặc trong CI.
2. Cắt gọn: chỉ giữ các game `ageBand: "kids"` liên quan toán và tư duy (math, sequence, shadows, sort, maze, memory). Gỡ PostHog và Firestore.
3. Việt hóa: thêm `src/i18n/dict/vi.ts`, đặt tiếng Việt làm mặc định, thu âm sẵn khoảng 50–100 câu nhắc chính.
4. Lên lộ trình nội dung theo chương trình mầm non 5–6 tuổi của Bộ GD&ĐT: số 1–10, so sánh, tách/gộp, hình học, định hướng không gian, quy luật.
5. Thêm bài đánh giá đầu vào và báo cáo cho phụ huynh, làm nền cho mô hình thu phí sau này.
