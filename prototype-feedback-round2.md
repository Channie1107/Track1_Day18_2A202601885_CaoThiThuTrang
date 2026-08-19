# Prototype Feedback — Vòng test bổ sung (3 tester khác, sau bản A/B/C gốc)

> File này ghi lại 1 vòng test riêng, với 3 tester khác Chặng 6 gốc. Xem [prototype-feedback-note.md](prototype-feedback-note.md) và [group-feedback-synthesis.md](group-feedback-synthesis.md) cho vòng test gốc (3 tester chọn 3 option khác nhau, nhóm chốt giữ B làm trục chính). Hai vòng test cho kết quả trái ngược nhau — xem phần "Đối chiếu với vòng test gốc" ở cuối file để biết cách nhóm xử lý mâu thuẫn này.

---

## 1. Feedback Note theo từng tester

### Tester 1 - Phạm Bá Huy (2A202601132)

**Context:** Sinh viên có thói quen thu thập tài liệu học tập đa dạng (chụp màn hình, note tay, mượn tài liệu của bạn).

**Observation:**
- **First action:** Quan sát sự khác biệt giữa cách AI xử lý tài liệu ở từng option (A, B, C).
- **Chỗ dừng/do dự:** Nghe kỹ phần giải thích về Option A (phê duyệt từng mục) và Option B (gom nhóm tài liệu).
- **Evidence đọc hay bỏ qua:** Bỏ qua hoàn toàn A và B — cho rằng bước phân loại thủ công tốn thời gian.
- **Cách lấy lại control:** Đề xuất có tham chiếu (reference) để sau khi AI tổng hợp xong vẫn tra ngược lại được tài liệu gốc.

**Option được chọn + lý do/trade-off:** Option C. *"Mình là người lười thì mình chỉ chọn C, cái auto luôn."* Trade-off: chấp nhận phó mặc cho AI phân tích để đổi lấy tốc độ.

**Evidence đi ngược kỳ vọng nhóm:** Nhóm từng kỳ vọng A/B (human-in-the-loop) sẽ giúp user an tâm hơn, nhưng tester đánh giá cả hai là "hơi thừa".

**Observed vs. Interpreted:**
- *Observed:* Tester nói thẳng mình lười, chê A/B thừa thãi, chốt C ngay.
- *Interpreted:* Với nhóm user bận rộn/ngại thao tác, giá trị lớn nhất của AI Notes là giảm tải thao tác đến mức tối đa (zero-click), không phải kiểm soát chi tiết từng bước.

---

### Tester 2 — Trương Ái Linh (2A202601496)

**Context:** Sinh viên cần hệ thống hóa ghi chú rải rác một cách nhanh chóng.

**Observation:**
- **First action:** Chú ý ngay đến số lượng thao tác cần để hoàn thành 1 bản ghi chú.
- **Chỗ dừng/do dự:** Đặt câu hỏi: nếu bản Option C tự sinh ra không chính xác hoặc thiếu ý thì xử lý thế nào?
- **Evidence đọc hay bỏ qua:** Nhận ra ngay Option C không có bước duyệt trung gian nào.
- **Cách lấy lại control:** Muốn kiểm soát ở *bước cuối* (sửa trực tiếp trên file kết quả), không phải ở *bước đầu vào*.

**Option được chọn + lý do/trade-off:** Option C. Ưu tiên tối ưu thời gian; đánh đổi độ chính xác ban đầu, bù lại bằng việc tự chỉnh sửa nội dung ở bản cuối.

**Evidence đi ngược kỳ vọng nhóm:** Tester không muốn tham gia vào bước AI gom nhóm/đọc hiểu — chỉ muốn nhận thẳng kết quả.

**Observed vs. Interpreted:**
- *Observed:* Chọn ngay "auto luôn", muốn sửa text sau khi bản đã hoàn thành.
- *Interpreted:* Sinh viên coi AI như người viết draft thô — họ muốn làm vai trò **Editor** (sửa lại), không phải **Reviewer** (duyệt từng bước).

---

### Giáp Quốc Anh (2A202601522)

**Context:** Sinh viên có nhu cầu lưu trữ tự động các dạng bài giảng, slide, ghi chú rời rạc.

**Observation:**
- **First action:** So sánh trực tiếp hiệu quả giữa luồng B (gom nhóm rồi duyệt) và C (tự động hoàn toàn).
- **Chỗ dừng/do dự:** Cân nhắc xem B có thực sự mang lại giá trị gì hơn C không.
- **Evidence đọc hay bỏ qua:** Bỏ qua Option A ngay lập tức vì thấy rườm rà (6 bước).
- **Cách lấy lại control:** Cần công cụ format linh hoạt và track được nội dung về đúng ảnh/slide gốc trong file cuối.

**Option được chọn + lý do/trade-off:** Option C. Tiện lợi, không tốn sức phân loại thủ công.

**Evidence đi ngược kỳ vọng nhóm:** Cơ chế kiểm soát ở Option B (gom nhóm tài liệu) vẫn chưa đủ nhanh gọn với user này.

**Observed vs. Interpreted:**
- *Observed:* Quyết định chọn C rất dứt khoát, gần như không cân nhắc.
- *Interpreted:* Thói quen học tập hiện tại của sinh viên ưu tiên kết quả "mì ăn liền" — muốn có ngay, chỉnh sau nếu cần, hơn là kiểm soát trước.

---

## 2. Group Feedback Synthesis

| | Tester 1 | Tester 2 | Tester 3 | Pattern / khác biệt |
|---|---|---|---|---|
| First action | Chú ý chức năng auto của C | Đếm số thao tác cần ở A/B | So sánh trực tiếp B vs. C | Cả 3 đều bỏ qua A rất nhanh, tập trung vào mức độ tự động của C |
| Breakdown chính | Ngại thao tác tay ở A/B | Sợ AI tổng hợp sót ý, nhưng vẫn không muốn duyệt từ đầu | Thấy A/B "hơi thừa" | Nỗi sợ mất thời gian duyệt lớn hơn nỗi sợ AI xử lý sai |
| Cách lấy lại control | Cần tham chiếu về nguồn | Muốn edit trực tiếp trên bản cuối | Muốn sửa format ở bản cuối | Cả 3 đều muốn kiểm soát ở **bước cuối** (sau khi có kết quả), không phải ở **quá trình** |
| Option được chọn | C | C | C | Đồng thuận 100% chọn C |
| Trade-off | Đổi độ chính xác lấy tốc độ | Chấp nhận note có lỗi, đổi lấy ít thao tác | Đổi sự minh bạch của quá trình lấy tốc độ | Cả 3 đều sẵn sàng bỏ qua tính minh bạch của thuật toán để lấy zero-click |

### Next Change nhóm chốt

**Bỏ Option A và B, dồn toàn bộ vào luồng Option C**, đồng thời bổ sung 2 tính năng ngay trên màn hình kết quả của C:
1. **Inline Editor** — cho phép sửa trực tiếp text AI vừa tạo.
2. **Source Reference** — gắn thẻ tham chiếu (link/highlight) trỏ ngược về đúng ảnh/tài liệu gốc tương ứng với từng đoạn text, để user tự đối chiếu khi cần.

**Evidence dẫn tới quyết định:** cả 3 tester đều nói A/B "thừa" hoặc tốn thời gian; câu quan trọng nhất là *"Mình là người lười thì chọn C cái auto luôn."* Mối quan tâm duy nhất còn lại của họ với C là làm sao sửa lại được nếu AI làm sai — không phải việc có nên tự động hay không.

### Still Unproven

Nếu tài liệu đầu vào lớn (hàng chục trang slide phức tạp) khiến C tổng hợp sai nhiều hơn, liệu thời gian bỏ ra để "Edit Inline" có vượt quá thời gian tự duyệt từng bước như Option B không? Khả năng chịu lỗi của C khi dữ liệu đầu vào lớn/phức tạp vẫn chưa được kiểm chứng thực tế.

---

## 3. Đối chiếu với vòng test gốc (Chặng 6)

Vòng test gốc (3 tester khác, xem [group-feedback-synthesis.md](group-feedback-synthesis.md)) cho kết quả **không đồng nhất** với vòng này: mỗi tester ở vòng gốc chọn 1 option khác nhau (B, A, C) và điểm chung là ai cũng muốn giữ nguồn gốc + đường phục hồi *trước khi* tin tưởng AI — nhóm gốc kết luận giữ B làm trục chính.

Vòng test này lại cho kết quả đồng thuận tuyệt đối vào C, với lý do chính là ngại thao tác chứ không phải vì tin tưởng AI hơn — và cách họ muốn lấy lại control là *sau khi* có kết quả (sửa bản cuối), không phải *trước khi* lưu (như tinh thần gate của B ở vòng gốc).

**Việc cần làm trước khi chốt hướng cuối cùng:** 2 vòng test nhỏ (3 người/vòng) cho 2 kết luận trái ngược nhau — mẫu quá nhỏ để khẳng định pattern nào đúng hơn. Trước khi quyết định bỏ hẳn A/B, nên: (1) xác nhận lại MSSV Tester 2 vòng này, (2) test thêm với cỡ mẫu lớn hơn hoặc đối tượng đồng nhất hơn giữa 2 vòng, và (3) làm rõ liệu sự khác biệt có đến từ cách 2 vòng test được dẫn dắt/giải thích khác nhau hay không — vì Tester 1 vòng này "nghe giải thích" về A/B trước khi chê, trong khi luật facilitation gốc yêu cầu không giải thích trước cơ chế của từng option.
