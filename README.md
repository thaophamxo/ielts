# IELTS Practice

Web app cá nhân luyện IELTS: Reading, Listening (chấm tự động, AI giải thích câu sai), Writing và Speaking (Gemini chấm). Một file `index.html`, không cần build.

## Deploy lên GitHub Pages

1. Tạo repo mới, upload `index.html` và `README.md` lên nhánh `main`.
2. Settings → Pages → Source: *Deploy from a branch*, Branch `main`, thư mục `/ (root)`, Save.
3. Chờ 1-2 phút, app chạy tại `https://<tên-github>.github.io/<tên-repo>/`.

Không có key hay dữ liệu cá nhân trong code. Không nên đưa file đề có bản quyền vào repo; đề được nhập trực tiếp trong app và chỉ lưu trong trình duyệt của bạn.

## Thiết lập một lần

1. **Cài đặt:** dán Gemini API key (https://aistudio.google.com/apikey), bấm "Thử kết nối". Mỗi thiết bị nhập một lần.
2. **Nhập đề:** vào Reading hoặc Listening, mục "Thêm đề bằng AI": upload PDF/ảnh đề và đáp án (hoặc dán text), bấm "Chuyển đổi bằng AI", rà lại đáp án ở bản xem trước, rồi "Lưu vào thư viện". Mỗi đề chỉ làm một lần.
3. **Audio Listening:** chọn file audio một lần trong màn hình làm bài (hoặc lúc nhập đề), app lưu trong trình duyệt cho lần sau.
4. **Sao lưu:** Cài đặt → Xuất file định kỳ. File xuất không chứa API key và audio.

## Mẹo nhập đề

- Nhập từng test một, hoặc dùng ô ghi chú, ví dụ "chỉ lấy Test 2".
- Nếu PDF quá lớn (&gt;14MB), tách thành từng test rồi upload.
- Luôn rà đáp án ở bản xem trước, vì AI có thể đọc sai ở ảnh mờ.
- Với Listening, nếu file có audioscript thì AI giữ lại để giải thích câu sai chính xác hơn.

## Lưu ý

- Điểm AI chỉ mang tính tham khảo, có thể lệch khoảng 0.5 band.
- Speaking dùng nhận giọng nói của trình duyệt (Chrome/Edge); Pronunciation chỉ là ước lượng từ transcript.
- Bảng quy đổi band Reading/Listening theo bảng Academic phổ biến; đề không đủ 40 câu sẽ được scale về 40.
