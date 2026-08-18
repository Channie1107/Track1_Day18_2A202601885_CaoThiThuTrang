# Ba Solution Options — Design Sheet (Day 18)

## 0. Chuẩn bị

**Case giữ nguyên Day 17:** Case B — AI Notes: Personal Learning Notes.

**Nhóm (3 thành viên):**

| MSSV | Họ tên | Vai trò |
|---|---|---|
| 2A202601885 | Cao Thị Thu Trang | Trưởng nhóm · phụ trách Option A |
| 2A202601026 | Nguyễn Thị Trà My | Phụ trách Option B |
| 2A202601882 | Bùi Thị Như Ngọc | Phụ trách Option C |

Mỗi thành viên vẫn tự test đủ cả ba option ở Chặng 6 theo đúng luật "không mang riêng option mình làm đi test".

**4 artifact Day 17 tham chiếu (đặt cạnh nhau):**
- Hypothesis Problem đã chốt → [day17-context.md § 2](day17-context.md)
- Practice Note (phỏng vấn Tạ Thị Nga, do Trang thực hiện) → [interview/notes.md](interview/notes.md)
- Solution Parking Lot (5 hướng) → [day17-context.md § 2](day17-context.md)
- Conversation Guide → [day17-context.md § 3](day17-context.md)

---

## Chặng 1 — Tổng hợp evidence (0:00–0:15)

**Observed vs. Interpreted (từ Practice Note):**

| Observed (user thực sự làm/nói) | Interpreted (nhóm diễn giải) |
|---|---|
| Chụp ảnh slide bằng điện thoại; ghi tay vào vở phần thầy giảng thêm; gõ thêm vào app Note khi không mang vở | User đang dùng nhiều kênh ghi chú song song vì không kênh nào đủ nhanh/đủ đầy một mình |
| "Nhiều lúc tìm xong nhưng không nhớ nổi cái ảnh đó là ý gì luôn." | Vấn đề không chỉ là *tìm lại* mà còn là *mất ngữ cảnh* — ảnh tách rời khỏi phần thầy giảng miệng lúc chụp |
| Từng gộp hết vào 1 file Word, bỏ sau 1 buổi vì mất công | Giải pháp thủ công đòi hỏi effort đều đặn sẽ không duy trì được — cần tự động hoá |
| Tốn 30–40 phút mỗi buổi ôn để tìm/gom ghi chú | Chi phí đủ lớn và lặp lại (không phải sự cố 1 lần) |

**Trả lời 3 câu hỏi:**
- *Situation/behavior/workaround lặp lại >1 lần?* Chụp ảnh slide + ghi tay/app song song (lặp lại mỗi buổi học); việc "chờ đến lúc ôn thi mới lục lại" cũng là hành vi lặp lại, không phải cá biệt.
- *Evidence nào mâu thuẫn/bất ngờ?* Giả thuyết ban đầu (Pain A) tập trung vào "ghi chú rời rạc, khó tổng hợp". Evidence thật cho thấy vấn đề sâu hơn: **mất ngữ cảnh** (context retention) — có ảnh nhưng không hiểu lại được ý nghĩa, chứ không đơn thuần là "khó tìm file".
- *Điều gì vẫn chỉ là suy đoán?* Chưa rõ mức độ phổ biến của việc "bỏ cuộc" với công cụ tổng hợp thủ công (mới quan sát ở 1 người); chưa biết user có sẵn sàng để AI tự động xử lý dữ liệu ghi chú của họ hay không.

**Hypothesis Problem (chốt lại sau Day 17, có bổ sung phát hiện mới):**

> Khi **ôn tập lại kiến thức đã học trên lớp**, **learner (sinh viên)** gặp khó khăn trong việc **tìm lại và hiểu đúng ngữ cảnh của những ghi chú/ảnh chụp slide đã lưu**, vì **ghi chú bị phân tán trên nhiều nền tảng (vở, app Note, thư viện ảnh) và tách rời khỏi phần diễn giải nghe được lúc học**, dẫn đến **mất 30–40 phút mỗi buổi ôn để dò lại, phải đoán lại nội dung từ ảnh mờ/thiếu ngữ cảnh, và có nguy cơ bỏ sót hoặc phải học lại từ đầu**.

- **Evidence ban đầu hỗ trợ:** Quote "Nhiều lúc tìm xong nhưng không nhớ nổi cái ảnh đó là ý gì luôn"; 3 kênh ghi chú song song (ảnh, vở, app); workaround gộp file Word thất bại sau 1 buổi; chi phí thời gian cụ thể (30–40 phút/buổi).
- **Điều vẫn chưa được chứng minh:** Mức độ phổ biến ở nhiều user khác (mới có 1 practice note trong repo này); user có tin tưởng để AI tự sắp xếp ghi chú học tập của mình không, hay muốn tự kiểm soát.

**Gate 1 (tự kiểm):** ✅ Đủ user (learner) + situation (ôn tập) + job (tìm lại/hiểu lại ghi chú) + barrier (phân tán + mất ngữ cảnh) + consequence (tốn thời gian, đoán sai, bỏ sót) + 1 observation Day 17 (quote) + 1 điều chưa biết.

---

## Chặng 2 — Chọn 3 Solution Options (0:15–0:35)

**Rà lại Solution Parking Lot (5 hướng Day 17):** 1) AI tự tổng hợp cuối bài, 2) Template điền tay, 3) AI gợi ý highlight real-time, 4) Nút bookmark 1-chạm, 5) Flashcard tự sinh. Pool hiện có cả AI-led (1,3,5) và non-AI thủ công (2,4) nhưng **thiếu trục rõ ràng về "ai giữ quyền quyết định tổng hợp"** — nên nhóm tổ chức lại thành 3 option cùng giải 1 problem, khác nhau ở mechanism/quyền quyết định (không thêm hướng mới ngoài parking lot).

**Phần giữ nguyên cho cả A/B/C:**
- **Target user:** Learner (sinh viên) ghi chú trong giờ học lý thuyết qua slide
- **Situation:** Đang học trên lớp, ghi chú xen kẽ chụp ảnh slide + note tay/app; sau đó ôn tập lại
- **Task:** Biến các mảnh ghi chú rời rạc (ảnh, text, highlight) thành 1 bản ghi có cấu trúc, **giữ được ngữ cảnh**, dễ tìm lại khi ôn thi
- **Desired outcome:** Trong vài phút, learner tìm lại đúng nội dung cần ôn và **hiểu được ý nghĩa** của nó, không phải đoán lại
- **Content/data fixture (dùng chung):** Buổi học "Kinh tế vi mô" — 3 ảnh chụp slide (đường cung–cầu, công thức độ co giãn, đồ thị thặng dư — 1 ảnh mờ/thiếu góc), 2 ghi chú gõ tay, 1 flag "Chưa hiểu: thặng dư sản xuất"

**Phần khác nhau cho từng option:**

| | **A — User-led** (Trang) | **B — Co-create** (Trà My) | **C — AI-led** (Ngọc) |
|---|---|---|---|
| Mechanism | Learner tự chọn từng mục cần AI xử lý | AI tự nhóm & đề xuất outline, learner review trước khi lưu | AI tự động tổng hợp & lưu toàn bộ ngay khi buổi học kết thúc |
| User làm gì | Duyệt từng ảnh/note, chọn mục, bấm "Xử lý mục này", rồi Chấp nhận/Sửa/Bỏ qua từng mục | Đọc outline AI đề xuất, sửa caption sai, bấm "Xem lại & Lưu" | Không cần làm gì lúc đó; mở lại khi cần, có thể sửa/xoá/khôi phục sau |
| AI làm gì | Với đúng mục được chọn: đọc ảnh + note liền kề, sinh tóm tắt + nguồn trích dẫn | Tự nhóm mục theo thời gian/nội dung, sinh caption nối ảnh với ý note, gắn cờ chỗ không chắc chắn | Toàn quyền tổng hợp, liên kết ngữ cảnh, đặt tên/tag, lưu thẳng |
| Trigger | Click thủ công, từng mục (explicit) | Tự động sau khi learner dừng ở màn hình đó, nhưng **chờ xác nhận** mới lưu | Tự động hoàn toàn, không cần hành động của user |
| Trade-off chính | Kiểm soát cao, không sợ AI hiểu sai — nhưng đòi hỏi effort lặp lại đúng lúc user đã mệt (khớp barrier "không đủ động lực sau giờ học") | Giảm effort đáng kể, có gate review — nhưng nếu learner lười đọc kỹ, caption sai vẫn có thể lọt qua | Zero-effort, giải đúng pain "không sắp xếp nổi sau giờ học" — nhưng rủi ro cao nhất nếu AI đoán sai ảnh mờ mà không ai kiểm tra |

**Distance-check:**
- **A khác B** vì A đòi hỏi learner tự bấm chọn từng mục cần xử lý (per-item, explicit), còn B để AI tự động gom nhóm & đề xuất trước, learner chỉ review — khác nhau ở **ai khởi tạo hành động tổng hợp**.
- **B khác C** vì B luôn dừng lại chờ learner xác nhận trước khi lưu, còn C lưu thẳng không chờ xác nhận — khác nhau ở **có hay không có gate quyết định** trước khi ghi vào hệ thống.
- **A khác C** vì A không tạo ra kết quả nào nếu learner không chủ động thao tác từng mục, còn C luôn tạo ra kết quả kể cả khi learner không tương tác gì — khác nhau ở **ai là actor bắt buộc phải hành động** để bản ghi tồn tại.

**Gate 2 (tự kiểm):** ✅ Cùng user/situation/task/outcome; khác nhau có ý nghĩa ở mechanism và phân chia quyền quyết định (không phải chỉ khác UI/màu/wording).

---

## Chặng 3 — Human–AI Design pass (0:35–1:05)

### Human–AI Decision Table

| | **A — User-led** | **B — Co-create** | **C — AI-led** |
|---|---|---|---|
| **Expectation** | Cần nói rõ: AI **chỉ** xử lý đúng mục được chọn, không tự ý gộp/sửa mục khác | Cần nói rõ: AI tự động đề xuất outline nhưng **chưa lưu** cho tới khi learner xác nhận; có thể nhóm sai nếu 2 chủ đề gần nhau về thời gian | Cần thông báo rõ "AI đã tự tổng hợp & lưu bản ghi mới — nên xem lại", tránh để learner tưởng đây là bản ghi tự tay làm |
| **Role & Agency** | User Ask từng mục, AI chỉ Act sau khi được yêu cầu trực tiếp. Nếu sai, chỉ mất đúng 1 mục, dễ phát hiện vì vừa xử lý xong còn nhớ ngữ cảnh | AI Act (nhóm & sinh caption) ở mức "đề xuất", có gate Ask trước khi lưu. Rủi ro trung bình: nếu learner review qua loa (do mệt), sai sót vẫn có thể lọt | AI Act hoàn toàn, không Ask trước tại thời điểm lưu (critical moment). Nếu sai, learner mất đúng phần quan trọng nhất (nội dung ôn thi) và **khó phát hiện** vì không có bước review bắt buộc — agency rủi ro cao nhất |
| **Evidence & Uncertainty** | Hiển thị tóm tắt dựa trên ảnh + note liền kề nào (nguồn, bấm vào xem lại được); nhãn "AI có thể đọc sai nếu ảnh mờ" | Mỗi caption gắn "độ tự tin"; ảnh mờ/note thiếu ngữ cảnh được gắn cờ rõ ("AI đoán — vui lòng kiểm tra") | Bắt buộc gắn nhãn "tự động, chưa review"; đoạn không chắc chắn phải để trống/đánh dấu [cần xác nhận] thay vì bịa — tránh lặp lại đúng lỗi đã thấy ở interview (ảnh mờ → đoán sai) |
| **Control & Recovery** | Preview trước khi chèn, chấp nhận/sửa/bỏ qua ngay tại chỗ; mỗi mục có trạng thái riêng, không ảnh hưởng mục khác | Sửa trực tiếp trên outline trước khi lưu; bỏ đề xuất quay lại ghi chú thô; sau khi lưu vẫn sửa lại được | Có nút "Sửa" và "Xem nội dung gốc" dễ tìm (không chỉ trong settings); có đường "Khôi phục bản ghi thô ban đầu" — bắt buộc vì đây là option rủi ro cao nhất khi sai |

**Dữ liệu nhạy cảm:** Đây là ghi chú học tập cá nhân, không phải dữ liệu huấn luyện liên tục. Nội dung chỉ ảnh hưởng đến đúng bản ghi/phiên đó, không dùng để "nhớ" sang note khác. Learner có thể xoá ảnh gốc/note gốc, hoặc bỏ tài liệu nguồn, bất cứ lúc nào (rút quyền dữ liệu).

**Gate 3 (tự kiểm):** ✅ Mỗi option nói rõ user/AI làm gì; agency tăng dần theo rủi ro khi sai (A thấp → B trung bình có gate → C cao không gate); mỗi option có ít nhất 1 đường kiểm soát/phục hồi cụ thể.

---

## Chặng 5 — Chuẩn bị test (2:25–2:40)

**Relevant context question (≤2 phút lúc test):**
> "Gần đây bạn có từng chụp ảnh slide hoặc ghi chú trong lúc học, rồi sau đó phải quay lại tìm/đọc lại không?"

**Outcome task (nói kết quả, không nói nút bấm):**
> "Đây là ghi chú thô từ một buổi học Kinh tế vi mô. Trong tình huống này, hãy dùng từng phương án để **biến các ghi chú rời rạc này thành một bản ghi mà bạn có thể mở lại và hiểu ngay, không cần đoán**."

**5 observation focus đã chọn:** first action · hesitation (do dự ở đâu) · evidence read hoặc ignored (có đọc phần "AI đoán/độ tự tin" không) · correction-recovery (khi thấy AI sai thì làm gì) · option chọn & trade-off (chọn option nào, vì sao).

**6 luật facilitation + 3 câu cứu hộ (cả nhóm đã thuộc):**
- "Bạn cứ nói to suy nghĩ của mình nhé."
- "Bạn sẽ làm gì tiếp theo?"
- "Theo bạn, nó nên hoạt động như thế nào?"

Xem [prototype-link.md](prototype-link.md) cho mô tả prototype + annotation Chặng 4, và [prototype-feedback-note.md](prototype-feedback-note.md) cho template quan sát Chặng 6.
