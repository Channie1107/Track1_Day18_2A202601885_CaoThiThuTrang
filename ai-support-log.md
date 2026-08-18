# AI Support Log

Mỗi thành viên viết ngắn phần của mình, dựa trên đúng phiên làm việc AI của bản thân — không copy phần của người khác, không để AI viết thay.

---

## Cao Thị Thu Trang — MSSV 2A202601885 (Trưởng nhóm · Option A)

**AI đã giúp tôi ở đâu?**
- Tổ chức lại 3 Solution Option (A/B/C) + Human–AI Decision Table dựa trên evidence Day 17 có sẵn (Hypothesis Problem, Practice Note thật, Solution Parking Lot).
- Viết code micro-prototype (`day18-prototype.html`, sau đó phiên bản đầy đủ `nootee-ai.html`): HTML/CSS/JS, dựng nội dung fixture giả lập (ảnh slide, ghi chú, công thức) đúng tình huống buổi học Kinh tế vi mô đã phỏng vấn được.
- Vẽ minh hoạ SVG (sơ đồ cung–cầu, mock ảnh slide) và rà soát kỹ thuật (kiểm tra id trùng, logic JS, HTML hợp lệ) nhiều lượt trong lúc build.

**AI sai, hời hợt hoặc làm các options giống nhau ở đâu?**
- Ở bản dựng đầu tiên, phương án B khi bấm "Lưu" luôn hiện ra **một bài học cố định**, bất kể tôi đã sửa nội dung gì trước đó — tức 3 phương án tuy khác giao diện/thao tác nhưng kết quả cuối lại giống hệt nhau, không thực sự phản ánh khác biệt về cơ chế. Đây đúng lỗi "làm các option giống nhau" mà lab cảnh báo, phải yêu cầu sửa lại.
- AI từng dựng 1 phiên bản giao diện dùng nguyên gradient thương hiệu Gemini của Google cho hiệu ứng AI — hời hợt, không tự kiểm tra nguồn gốc màu sắc trước khi dùng, phải yêu cầu đổi sang hướng thị giác riêng.
- Modal "Tạo sổ mới" từng bị lỗi logic: tiêu đề ghi "Tạo sổ mới" nhưng lại điền sẵn dữ liệu của sổ đã tồn tại (do chỉnh sửa/copy state giữa các phiên bản không cẩn thận).
- Ảnh minh hoạ ban đầu cho ghi chú thô không rõ là "ảnh chụp slide" (trông giống hệt nền giấy ghi chú) — hời hợt về hình ảnh, phải yêu cầu làm lại cho đúng tình huống.

**Tôi đã tự sửa hoặc quyết định lại điều gì?**
- Yêu cầu sửa để nội dung tổng hợp cuối của A và B phải **thay đổi thật** theo hành động Chấp nhận/Sửa/Bỏ qua của người dùng, thay vì AI bịa sẵn 1 bản cố định.
- Quyết định gộp nút chuyển A/B/C vào **bên trong từng sổ tay** thay vì để AI làm toggle chuyển cả ứng dụng — vì mục tiêu thật là giúp so sánh trực tiếp 3 phương án trên cùng nội dung, không phải chuyển qua 2 app riêng biệt.
- Khôi phục lại file `day18-prototype.html` khi phát hiện nó bị chỉnh sửa/lỗi ngoài ý muốn (mất 1 nút do sửa nhầm), để không ảnh hưởng bài nộp gốc.
- Bỏ cách "thêm tài liệu" kiểu giả lập (chọn xoay vòng từ danh sách có sẵn), yêu cầu đổi sang chọn file thật từ máy — vì cách giả không đúng tình huống thật của một bài kiểm thử.
- Chủ động rà soát và xoá bớt các file không còn liên quan (bản thiết kế nháp cũ, ảnh minh hoạ không dùng tới, quyển sổ mẫu không liên quan case đang test) trước khi nộp.

---

## Nguyễn Thị Trà My — MSSV 2A202601026 (Option B)

**AI đã giúp tôi ở đâu?**
- Rà lại cách đặt trọng tâm cho Option B: AI giúp tôi viết lại luồng "AI gom nhóm -> người dùng sửa -> mới lưu" cho rõ hơn.
- Gợi ý microcopy cho các trạng thái cần nhìn thấy trước khi lưu, đặc biệt là chỗ nào đang là đề xuất của AI chứ chưa phải nội dung cuối.
- So sánh Option B với A và C để bảo đảm B thật sự nằm giữa hai đầu cực đoan, không bị giống một bản rút gọn của Option A.

**AI sai, hời hợt hoặc làm các options giống nhau ở đâu?**
- AI có xu hướng mô tả Option B quá giống Option A ở chỗ "người dùng phải sửa từng chỗ", trong khi điểm khác biệt chính của B là AI đã tự gom nhóm trước.
- Một số câu chữ AI viết khá chung chung, khiến Option B mất cảm giác "có khung đề xuất sẵn" và nhìn giống một form trống.
- AI cũng hay đẩy quá nhiều chi tiết vào phần lưu, làm người đọc khó thấy rõ đâu là bước review, đâu là bước chốt.

**Tôi đã tự sửa hoặc quyết định lại điều gì?**
- Tôi tự chốt rằng Option B phải luôn có một bản đề xuất ban đầu rõ ràng để người dùng sửa, thay vì bắt người dùng tự dựng lại từ đầu.
- Tôi giữ nút "Xem lại & Lưu" như một gate bắt buộc để tránh lưu nhầm khi còn đang chỉnh.
- Tôi lược bớt các mô tả thừa để B khác A ở chỗ AI đã làm phần gom nhóm, còn người dùng tập trung vào kiểm tra và tinh chỉnh.

---

## Bùi Thị Như Ngọc — MSSV 2A202601882 (Option C)

**AI đã giúp tôi ở đâu?**
- Dựng luồng tự động hoá cho Option C: AI tổng hợp ngay, nhưng vẫn phải cho người dùng thấy bản ghi thô và nguồn gốc.
- Gợi ý các trạng thái phục hồi như "Xem ảnh gốc", "Sửa", "Khôi phục bản ghi thô" để tránh cảm giác AI làm xong là không còn đường quay lại.
- Viết lại microcopy để Option C nghe rõ là AI-led nhưng không biến thành "AI tự làm mọi thứ, người dùng bị bỏ rơi".

**AI sai, hời hợt hoặc làm các options giống nhau ở đâu?**
- AI rất dễ biến Option C thành một phiên bản "tự động lưu" nhưng không có hồi cứu, khiến nó giống một shortcut hơn là một cơ chế riêng.
- Nếu không kiểm soát chặt, AI sẽ dùng lại nhiều câu từ của Option B, làm C chỉ khác ở tốc độ chứ không khác ở quyền quyết định.
- Có lúc AI viết phần raw/source quá ít, làm option này mất đi điểm an toàn quan trọng nhất.

**Tôi đã tự sửa hoặc quyết định lại điều gì?**
- Tôi chốt rằng Option C phải giữ được ít nhất ba đường kiểm soát: sửa, xem nguồn gốc và khôi phục bản thô.
- Tôi ưu tiên làm rõ sự khác nhau giữa "tự động tổng hợp" và "tự động áp đặt".
- Tôi tách lại các mô tả để C là option nhanh nhất, nhưng cũng là option cần cảnh báo và phục hồi rõ nhất.
