# IELTS Practice

Web app cá nhân luyện IELTS: Reading, Listening (chấm tự động, AI giải thích câu sai), Writing và Speaking (Gemini chấm). Một file `index.html`, không cần build.

## Deploy lên GitHub Pages

1. Tạo repo mới, upload `index.html` và `README.md` lên nhánh `main`.
2. Settings → Pages → Source: *Deploy from a branch*, Branch `main`, thư mục `/ (root)`, Save.
3. Chờ 1-2 phút, app chạy tại `https://<tên-github>.github.io/<tên-repo>/`.

Không có key hay dữ liệu cá nhân trong code. Đề và audio chỉ lưu trong trình duyệt của bạn, đừng đưa file đề có bản quyền vào repo.

## Thiết lập một lần

1. **Cài đặt:** dán Gemini API key (https://aistudio.google.com/apikey), bấm "Thử kết nối". Mỗi thiết bị nhập một lần.
2. **Nhập sách:** vào mục *Nhập sách*, chọn PDF nguyên cuốn, chọn folder audio, bấm **Tự động nhập cả sách**. AI tự tìm trang của từng đề (Listening, Reading, Writing, Speaking), trang đáp án và audioscript, nhập toàn bộ rồi gán audio. Không phải điền số trang. Quá trình mất khoảng 15–30 phút, để tab mở.
3. **Rà đáp án:** đề Reading/Listening mới nhập có nhãn "cần rà đáp án". Bấm nút "Đáp án", so với sách, sửa nếu AI đọc sai rồi lưu.
4. **Kiểm tra audio:** mở thử một đề Listening, xem Part 1–4 đã đúng chưa. Đề nào chưa khớp thì bấm nút "Audio" của đề đó để chọn tay.
5. **Sao lưu:** Cài đặt → Xuất file định kỳ. File xuất gồm đề và lịch sử, không gồm API key và audio.

## Khi quét sai

Mục "Nâng cấp" trong *Nhập sách* hiện số trang AI tìm được cho từng đề. Có thể sửa tay rồi bấm "Nhập các dòng chưa xong". Nút "Chỉ quét" cho phép xem trước số trang mà chưa nhập.

## Lưu ý

- Cần mạng khi dùng lần đầu vì thư viện cắt PDF (pdf-lib) tải từ CDN.
- Writing Task 1 từ sách: app lưu các trang chứa biểu đồ và gửi kèm khi chấm.
- Speaking từ sách dùng thẳng câu hỏi trong sách, không tốn lượt gọi AI để tạo câu.
- Audio tự khớp theo tên file/folder (Test 1, Part 2...). Nếu file chỉ tên "Track 01...", app chỉ tự gán khi số file đúng bằng 4 lần số đề.
- Điểm AI chỉ mang tính tham khảo, có thể lệch khoảng 0.5 band. Pronunciation chỉ là ước lượng từ transcript.
