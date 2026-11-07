# IELTS Practice

Web app cá nhân luyện IELTS: Reading, Listening (chấm tự động, AI giải thích câu sai), Writing và Speaking (Gemini chấm). Một file `index.html`, không cần build.

## Deploy lên GitHub Pages

1. Tạo repo mới, upload `index.html` và `README.md` lên nhánh `main`.
2. Settings → Pages → Source: *Deploy from a branch*, Branch `main`, thư mục `/ (root)`, Save.
3. Chờ 1-2 phút, app chạy tại `https://<tên-github>.github.io/<tên-repo>/`.

Không có key hay dữ liệu cá nhân trong code. Đề và audio chỉ lưu trong trình duyệt của bạn, đừng đưa file đề có bản quyền vào repo.

## Thiết lập một lần

1. **Cài đặt:** dán Gemini API key (https://aistudio.google.com/apikey), bấm "Thử kết nối". Mỗi thiết bị nhập một lần.
2. **Nhập sách:** vào mục *Nhập sách*, chọn PDF nguyên cuốn, bấm "+ 4 Listening, 4 Reading, 4 Writing, 4 Speaking", điền khoảng trang cho từng dòng (số trang theo trình xem PDF, ví dụ `14-27`; đáp án và audioscript thường ở cuối sách), rồi bấm "Nhập tất cả". Có thể nhập dần từng đợt, dòng nào để trống "Trang đề" sẽ bị bỏ qua.
3. **Rà đáp án:** đề mới nhập có nhãn "cần rà đáp án". Mở Reading hoặc Listening, bấm nút "Đáp án", so với sách và sửa nếu AI đọc sai, rồi lưu.
4. **Audio Listening:** ở danh sách đề Listening, bấm "Audio", chọn các file hoặc cả folder audio của sách, chỉnh Part cho đúng (app tự đoán theo tên file/folder), bấm "Lưu audio". App lưu audio trong trình duyệt nên không phải chọn lại.
5. **Sao lưu:** Cài đặt → Xuất file định kỳ. File xuất gồm đề và lịch sử, không gồm API key và audio.

## Lưu ý

- Cần mạng khi dùng lần đầu vì thư viện cắt PDF (pdf-lib) tải từ CDN.
- Writing Task 1 từ sách: app lưu các trang chứa biểu đồ và gửi kèm khi chấm.
- Speaking từ sách dùng thẳng câu hỏi trong sách, không tốn lượt gọi AI để tạo câu.
- Điểm AI chỉ mang tính tham khảo, có thể lệch khoảng 0.5 band. Pronunciation chỉ là ước lượng từ transcript.
- Bảng quy đổi band Reading/Listening theo bảng Academic phổ biến; đề không đủ 40 câu sẽ được scale về 40.
