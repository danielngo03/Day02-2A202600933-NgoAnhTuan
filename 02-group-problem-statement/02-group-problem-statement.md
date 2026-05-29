# Bản nộp bài — AI Inbox Operator

Case: **Tối ưu phễu chốt đơn Social Commerce tại Việt Nam**

Nhân vật / Actor: Nhân viên trực chat chốt đơn tại các shop Social Commerce quy mô SMB tại Việt Nam (lượng tin nhắn dao động từ 200 - 1000 tin/ngày).

## Vì sao chọn đề tài này?

- Quy trình trước/sau cực kỳ rõ ràng, dễ đo lường bằng thời gian phản hồi (giây) và tỷ lệ chốt đơn thành công.
- Nỗi đau của các chủ shop online rất lớn và có bằng chứng thực tế rõ ràng từ khảo sát 30 shop đa kênh.
- Thiết lập được ranh giới kiểm soát an toàn (Human Boundary) cực kỳ rõ nét: Con người là người kiểm duyệt và bấm nút gửi cuối cùng, tránh rủi ro AI báo sai giá/tồn kho gây thiệt hại tài chính.

---

# 02 — Group Problem Statement

## Group convergence

Nhóm chúng tôi gồm 3 thành viên đã tiến hành chia sẻ và phân tích danh sách đề tài cá nhân nhằm mục đích gom cụm và chọn lựa một bài toán có tính khả thi tốt nhất cho buổi học thực hành:

| Cluster | Candidate examples | Pattern chung |
|---|---|---|
| Báo cáo / tổng hợp thông tin | Báo cáo tuần, tổng hợp tiến độ học tập | Gom thông tin từ nhiều nguồn và tổng hợp lại cho người khác đọc |
| Chăm sóc khách hàng / chốt đơn | Inbox đa kênh bị trôi, trả lời câu hỏi lặp lại (FAQ), bám đuổi (follow-up) khách | Giải quyết tốc độ giao tiếp và tối ưu hóa phễu chuyển đổi khách nóng |
| Soạn thảo nội dung | Viết bài PR, soạn thảo spec mô tả sản phẩm | Sáng tạo nội dung dựa trên bộ khung yêu cầu có sẵn |

## Shortlist và score

Chúng tôi đã lọc ra 3 đề tài tiềm năng nhất để đưa lên bàn cân chấm điểm đồng thuận (thang điểm từ 1-5):

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A được | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Review PRD tự động | 4 | 5 | 3 | 3 | 4 | 4 | 4 | 27 |
| Tìm kiếm nội dung Slack | 4 | 4 | 4 | 4 | 3 | 4 | 4 | 27 |
| **AI Inbox Operator (Chốt đơn)** | 5 | 5 | 5 | 5 | 5 | 5 | 5 | **35** |

Nhóm chọn: **AI Inbox Operator (Tối ưu phễu chốt đơn Social Commerce)**

Vì sao chọn:

- Có quy trình trước/sau cực kỳ rõ ràng, dễ đo lường bằng thời gian (giây) và hiệu suất chốt đơn.
- Nỗi đau của chủ shop rất lớn và có bằng chứng thực tế rõ ràng từ khảo sát.
- Thiết lập được ranh giới kiểm soát an toàn (Human Boundary) cực kỳ rõ nét: Con người bấm nút gửi cuối cùng để kiểm duyệt AI.

Vì sao không chọn các bài khác:

- Tìm kiếm nội dung Slack: Rào cản quyền truy cập dữ liệu nội bộ của Slack doanh nghiệp rất phức tạp, dễ trượt sang thiết kế hệ thống quá lớn.
- Review PRD tự động: Quy trình rõ nhưng khó thống nhất được metric đo lường chất lượng review trong thời gian lab.

## Quick validation

Chúng tôi đã tiến hành khảo sát và phỏng vấn nhanh với 30 chủ shop online đa kênh tại Việt Nam:

| Nguồn | Số người | Tín hiệu xác nhận | Tín hiệu phản bác | Nhóm sửa problem thế nào |
|---|---:|---|---|---|
| Quick interview | 10 | 8/10 shop thừa nhận nhân viên trực chat bị quá tải và hay báo sai giá/tồn kho do tra Excel chậm. | 2/10 nói đã mua các tool tự động trả lời tự động. | Tập trung vào giải pháp trợ lý soạn nháp (drafting) thay vì tự động trả lời 100% để giữ trải nghiệm tự nhiên. |
| Mini poll trong lớp | 20 | 17/20 cho biết có tình trạng trôi tin nhắn và khách bỏ đi nếu phản hồi trễ quá 5 phút. | 3/20 cho biết lượng inbox ít nên tự quản lý được. | Định vị tập khách hàng mục tiêu là shop có lượng inbox dao động từ 200 - 1000 tin/ngày. |

Insight sau validation:

```text
Pain thật của shop không nằm ở việc "thiếu công cụ gom chat" (vì họ đã dùng Pancake), mà nằm ở khâu biến đống dữ liệu thô (kho hàng, giá ship) thành câu trả lời chốt đơn cá nhân hóa cực nhanh để giữ chân khách nóng.
```

## Research giải pháp

Chúng tôi đã nghiên cứu các hướng giải pháp sẵn có trên thị trường:

| Nguồn / tool / case | Link | Họ giải quyết phần nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| Pancake / Haravan | https://pancake.vn | Gom chat đa kênh, quản lý kho hàng | Đồng bộ ổn định, thị phần lớn tại Việt Nam | Hoàn toàn thủ công, nhân viên vẫn phải gõ phím 100% | Tích hợp Chrome Extension lên Pancake thay vì tự xây Hub chat mới |
| Chatbot tự động cũ | https://chatfuel.com | Tự động trả lời theo kịch bản | Hoạt động 24/7 không cần người | Trả lời ngô nghê, khách ghét robot; dễ bị platform quét spam khóa page | AI chỉ soạn draft trên màn hình, con người là người duyệt và bấm nút gửi (Hybrid) |
| Slack AI / Gemini | https://slack.com | Tóm tắt cuộc hội thoại | Tóm tắt nhanh và chính xác | Chỉ hoạt động nội bộ, không kết nối kho/giá và không hiểu tiếng lóng Việt Nam | AI phải kết nối RAG với Database sản phẩm thực tế để lấy giá và tồn kho chính xác |

Research takeaway:

```text
Không nên tự xây dựng một công cụ gom chat mới từ đầu do CAC rất cao và đối đầu trực diện với Pancake. Cách tiếp cận tốt nhất là làm một Chrome Extension overlay trực tiếp lên Pancake để hỗ trợ soạn thảo.
```

## Workflow before/after

File nhóm nộp kèm:

```text
mermaid-diagram_truoc.png
mermaid-diagram_sau.png
```

Nội dung workflow:

```text
CURRENT STATE — Quy trình cũ:
Nhân viên trực chat nhảy app liên tục -> tự đọc lọc -> tra cứu Excel thủ công (bottleneck mất 25 phút/ca) -> soạn câu trả lời bằng tay -> check sót đơn thủ công cuối ngày.

FUTURE STATE — Quy trình mới:
AI gom chat & phân loại ưu tiên -> AI tự động tra kho & soạn draft câu trả lời -> Nhân viên trực chat duyệt và gửi (1 giây) -> AI tự động lên lịch nhắc nhở bám đuổi đơn hàng cuối ngày.
```

Before/after impact:

| Metric | Trước | Sau kỳ vọng | Ghi chú |
|---|---:|---:|---|
| Tổng thời gian xử lý ca | 90 phút | 21 phút | Giảm 76% công sức trực chat |
| Thời gian phản hồi (ART) | 3 - 5 phút | Dưới 30 giây | Trả lời ngay lập tức để giữ chân khách |
| Số bước thủ công | 5 bước | 1 bước duy nhất | Bước Duyệt & Gửi của nhân viên trực chat |
| Rủi ro vận hành | Trôi tin nhắn, sai giá | AI Hallucination | Khắc phục bằng ranh giới kiểm duyệt (Human-in-the-loop) |

## Problem Statement v0

| Field | Nội dung |
|---|---|
| **Actor** | Nhân viên trực chat chốt đơn tại các shop Social Commerce quy mô SMB tại Việt Nam. |
| **Workflow** | Nhận tin nhắn đa kênh $\rightarrow$ Đọc và tự lọc $\rightarrow$ Tra cứu kho $\rightarrow$ Soạn câu trả lời $\rightarrow$ Gửi $\rightarrow$ Check sót đơn. |
| **Bottleneck** | Khâu tra cứu tồn kho, giá sản phẩm và soạn câu trả lời chốt đơn mất nhiều thời gian (5-7 phút/inbox). |
| **Impact** | Gây trễ phản hồi, trôi tin nhắn và rò rỉ doanh thu của shop. |
| **Success Metric** | Giảm thời gian phản hồi và tăng tỷ lệ chốt đơn thành công. |
| **Boundary** | AI không tự động gửi tin nhắn trực tiếp khi chưa có sự phê duyệt của con người. |

## Rule / Workflow / Agent

| Mức | Phương án | Khi nào đủ | Rủi ro | Chọn? |
|---|---|---|---|---|
| **Rule** | Tự động hóa lấy số, dùng tin nhắn mẫu (Quick Reply) | Đủ nếu khách chỉ hỏi thông tin cơ bản | Cứng nhắc, không hiểu ngữ cảnh tiếng lóng Việt Nam | Chỉ dùng hỗ trợ bước lấy dữ liệu |
| **Workflow** | AI tự tra kho $\rightarrow$ AI soạn draft $\rightarrow$ Người duyệt gửi | Đủ cho quy trình tuyến tính cần tính chính xác cao | AI draft bị lỗi/hallucination | **CHỌN** |
| **Agent** | Agent tự quyết định phân loại, tự chat và lên đơn hoàn toàn | Cần khi quy trình phức tạp nhiều nhánh rẽ | Rủi ro tự ý báo sai giá gây đền bù tài chính | Chưa chọn |

Mức chọn:

```text
Workflow
```

Vì sao:

- Quy trình chốt đơn là tuyến tính, yêu cầu độ chính xác dữ liệu (kho, giá) tuyệt đối. Workflow kết hợp người duyệt (Hybrid) là phương án an toàn nhất.

Vì sao không chọn mức đơn giản hơn:

- Rule-based không thể xử lý được ngôn ngữ tự nhiên viết tắt và tiếng lóng phức tạp của khách hàng Việt Nam.

## Problem Statement v1

| Field | Nội dung |
|---|---|
| **Actor** | Nhân viên trực chat chốt đơn tại các shop Social Commerce quy mô SMB tại Việt Nam. |
| **Workflow** | Nhận tin nhắn đa kênh $\rightarrow$ Đọc và tự lọc $\rightarrow$ Tra cứu kho $\rightarrow$ Soạn câu trả lời $\rightarrow$ Gửi $\rightarrow$ Check sót đơn. |
| **Bottleneck** | Khâu tra cứu tồn kho, giá sản phẩm và soạn câu trả lời chốt đơn mất nhiều thời gian (5-7 phút/inbox). |
| **Impact** | Gây trễ phản hồi, trôi tin nhắn làm rò rỉ 15% doanh thu; nhân viên bị quá tải căng thẳng dẫn đến sai sót báo giá. |
| **Success Metric** | Giảm tổng thời gian xử lý tin nhắn xuống dưới 30 giây/inbox; giảm tỷ lệ rớt đơn do trễ phản hồi xuống <3%. |
| **Boundary** | AI không tự động gửi tin nhắn trực tiếp khi chưa có sự phê duyệt bấm nút của con người. AI không tự ý thay đổi giá hoặc hứa hẹn sai chính sách. |
| **AI intervention point** | Sau khi nhận tin nhắn và trước khi phản hồi khách hàng (AI tự tra kho và soạn draft phản hồi). |
| **Mức chọn** | Workflow (Chrome Extension tích hợp Pancake kết hợp RAG Engine). |
| **Rủi ro & người thật kiểm tra** | Risk: AI bịa thông tin sản phẩm hoặc hiểu sai từ viết tắt. Người kiểm tra: Nhân viên trực chat bắt buộc phải lướt qua xem nội dung AI soạn nháp trước khi bấm nút "Gửi". |

## Final decision

Decision:

```text
Go với quy mô nhỏ (SaaS Pro 299k/user/tháng)
```

Pilot nhỏ nhất:

- Chạy thử nghiệm thủ công (bán tự động) trên 100 đơn hàng đầu tiên của 2 shop online quen thuộc bằng cách copy tin nhắn dán vào prompt RAG để đo độ chính xác.

Exit / rollback:

- Nếu nhân viên trực chat phải sửa lại hơn 70% nội dung soạn nháp của AI liên tục trong 2 tuần, hạ cấp giải pháp về mức dùng template thông thường kết hợp dashboard.

Decision rationale:

- Đề tài có workflow rõ ràng, nỗi đau đo lường được bằng tiền mặt.
- Mô hình Chrome extension giúp tối ưu chi phí vận hành và tích hợp trực tiếp, tránh đối đầu trực diện với Pancake.
