# AI Speaking Partner

Prototype giao diện mobile cho tính năng luyện nói tiếng Anh cùng AI dành cho học sinh.

## Thông tin bài làm

- Học viên: Võ Tấn Trung
- Mã học viên: 2A202600642
- Track: Product - Day 18
- Prototype: `ai-speaking-prototype.html`

## Vấn đề

Học sinh thường thiếu môi trường an toàn để luyện nói, dễ bị bí ý hoặc ngại mắc lỗi. AI Speaking Partner tạo một buổi hội thoại theo chủ đề, hỗ trợ vừa đủ trong lúc nói và đưa ra phản hồi có bằng chứng sau buổi học.

## Phạm vi prototype

Prototype tập trung vào một lát cắt chính:

> Học sinh chọn chủ đề, trò chuyện với AI, nhận đánh giá sau buổi nói và có thể phản hồi khi đánh giá hoặc độ khó chưa phù hợp.

Onboarding và nhận diện tâm trạng chưa nằm trong phạm vi phiên bản này.

## Luồng demo

1. Chọn một chủ đề và bắt đầu luyện nói.
2. Trò chuyện với AI bằng giọng nói.
3. Khi học sinh dừng lâu hoặc yêu cầu hỗ trợ, AI đề nghị gợi ý.
4. Kết thúc buổi nói và xem thời lượng, số lần dùng gợi ý cùng transcript.
5. Xem nhận xét về fluency, vocabulary, grammar và pronunciation.
6. Kiểm tra bằng chứng trong transcript và mức độ tự tin của AI.
7. Báo phản hồi chưa chính xác, câu hỏi quá khó hoặc yêu cầu thử lại.
8. AI xác nhận điều chỉnh và hỏi trước khi lưu lựa chọn cho các buổi sau.

## Các kịch bản chính

### 1. Hội thoại bình thường

Học sinh chọn chủ đề, trả lời câu hỏi và kết thúc buổi luyện nói. AI hiển thị trạng thái đang nghe, transcript trực tiếp và tiến trình buổi học.

### 2. Học sinh bị bí

AI phát hiện khoảng dừng dài nhưng không tự trả lời thay. Hệ thống hỏi học sinh muốn nhận gợi ý hay cần thêm thời gian, sau đó cung cấp từ vựng hoặc câu mở đầu.

### 3. Phản hồi của AI chưa chính xác

Học sinh có thể đánh dấu nhận xét chưa đúng. AI hiển thị đoạn transcript liên quan, mức độ tự tin và cho phép học sinh sửa hoặc yêu cầu đánh giá lại.

### 4. Câu hỏi quá khó

Học sinh chọn “The question was too hard”. AI xác nhận vấn đề, giảm độ khó trong phiên hiện tại và đưa ra một câu hỏi đơn giản hơn.

## Quyền kiểm soát của người dùng

- **Act:** AI tổng hợp các tín hiệu trong phiên hiện tại và đưa ra phản hồi sau buổi nói.
- **Ask:** AI hỏi trước khi lưu độ khó hoặc sở thích để cá nhân hóa các phiên sau.
- **Don't Act:** AI không tự động chia sẻ audio, transcript hay kết quả với giáo viên/phụ huynh và không đưa ra đánh giá năng lực vĩnh viễn.

## Feedback 2x2

| Hướng phản hồi | Explicit | Implicit |
| --- | --- | --- |
| User → System | Học sinh yêu cầu gợi ý, bỏ qua, thử lại, báo câu hỏi quá khó hoặc phản hồi chưa chính xác. | Thời lượng hội thoại, khoảng dừng dài, số lần dùng gợi ý, bỏ qua và thử lại. |
| System → User | AI giải thích nhận xét, chỉ ra bằng chứng, hiển thị độ tự tin và đề xuất bước tiếp theo. | Trạng thái đang nghe/đang xử lý, tiến trình, transcript được đánh dấu và mức nhấn của hành động. |

## Explainability và recovery

AI liên kết nhận xét với câu nói cụ thể trong transcript, ví dụ:

> “Yesterday I go...” → “Yesterday I went...”

Mỗi nhận xét có mức độ tự tin để học sinh biết AI có thể chưa chắc chắn. Vòng lặp phục hồi:

`AI feedback → Học sinh báo vấn đề → Chọn lý do → AI xác nhận → Đề xuất điều chỉnh → Tiếp tục luyện nói`

## Cách xem prototype

Mở file `ai-speaking-prototype.html` bằng trình duyệt có kết nối Internet. Prototype sử dụng Tailwind CSS, Google Fonts và Material Symbols qua CDN.

Thiết kế được tối ưu theo khung màn hình mobile portrait. Đây là mockup trực quan được xuất từ Stitch AI; các màn hình được trình bày trong cùng một file HTML để phục vụ việc review và demo luồng.

## Công cụ

- Stitch AI
- HTML
- Tailwind CSS CDN
- Material Symbols
