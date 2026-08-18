# Micro-prototype — link chung của nhóm (Chặng 4)

Xem [three-option-design-sheet.md](three-option-design-sheet.md) cho phần thiết kế đứng sau prototype này.

## Link để test

- **Bản khuyến nghị dùng để test — `prototype/nootee-ai.html`:** dashboard sổ tay "Nootee", mở sổ **Kinh tế vi mô** để vào thẳng phần so sánh A/B/C. Mở trực tiếp file này bằng trình duyệt (hoặc Live Server) từ máy đã clone repo.
- **Bản gốc trung lập — `prototype/day18-prototype.html`:** công cụ test A/B/C thuần tuý theo đúng khung Day 18 gốc (không có giao diện sổ tay). Mở trực tiếp file local này để kiểm tra luồng tương tác gốc của ba phương án.

## Cấu trúc chung (dùng chung ~70% giữa 3 option)

Một màn "Ghi chú thô" chung (danh sách ghi chú thô — ảnh + note + flag "chưa hiểu", cùng khu vực quản lý tài liệu nguồn: xem/thêm/bỏ tài liệu) dùng làm điểm xuất phát/điểm quay lại cho cả 3 option; mỗi option A/B/C xoay quanh đúng 1 critical interaction (khác nhau theo Chặng 2–3 của design sheet), dùng chung fixture/style/nội dung. Nút chuyển đổi nhỏ (Thô / A / B / C) đặt cố định ở góc dưới bên phải màn hình khi đang mở sổ Kinh tế vi mô.

## Annotation ngoài frame (facilitator-only, ẩn khi test)

- **Option A:** *Expect tester:* chọn 1 mục và bấm nút xử lý riêng cho mục đó, rồi Chấp nhận/Sửa/Bỏ qua từng mục. *Watch for:* có thử xử lý nhiều mục cùng lúc không, có nhận ra các mục khác vẫn "thô" không, có bấm vào "Nguồn" để xem lại ảnh/ghi chú gốc không. *Do not explain:* không nói trước rằng phải xử lý từng mục một, và bài học cuối chỉ gồm những mục đã chấp nhận.
- **Option B:** *Expect tester:* đọc outline AI đề xuất, sửa 1 chỗ sai rồi mới bấm "Xem lại & Lưu". *Watch for:* có đọc kỹ mục được gắn cờ "AI đoán" không, hay bấm Lưu ngay. *Do not explain:* không nói trước có mục nào bị AI đoán sai.
- **Option C:** *Expect tester:* nhận ra bản ghi đã tự động xuất hiện mà mình chưa làm gì. *Watch for:* có chủ động tìm nút Sửa/Xem nội dung gốc không, hay chấp nhận luôn bản AI tạo. *Do not explain:* không nói trước rằng có phần AI đoán sai/không chắc.

## Gate 4 (tự kiểm)

Trước khi nộp, một người **không thuộc nhóm build** nên tự mở prototype, thao tác hết A/B/C và quay lại "Ghi chú thô" mà không cần giải thích thêm. Nếu họ bị kẹt ở bất kỳ option nào, cần sửa lại annotation hoặc microcopy trước khi test thật.
