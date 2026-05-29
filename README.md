# Day 02 Lab — AI Inbox Operator

## Thông tin bài nộp

| Mục | Nội dung |
|---|---|
| Học viên | Anh Tuan Ngo |
| Mã học viên | 2A202600933 |
| Chủ đề | AI Inbox Operator |
| Case nhóm chọn | Tối ưu phễu chốt đơn Social Commerce tại Việt Nam |
| Actor chính | Nhân viên trực chat chốt đơn tại các shop Social Commerce quy mô SMB tại Việt Nam |
| Mức giải pháp chọn | Workflow |
| Decision | Go với quy mô nhỏ |

---

## Tổng quan

Repo này là bài nộp cho **Day 02 Lab**, tập trung vào cách đi từ problem thật đến workflow, metric, boundary và quyết định mức độ phù hợp với AI.

Case được chọn là **AI Inbox Operator cho shop Social Commerce tại Việt Nam**. Bài toán xuất phát từ việc các shop online nhận quá nhiều tin nhắn từ nhiều kênh như Facebook, Zalo, Shopee, TikTok Shop, Instagram và livestream. Nhân viên trực chat phải đọc/lọc tin nhắn, tra tồn kho/giá, soạn câu trả lời và follow-up khách hàng hoàn toàn thủ công. Điều này gây phản hồi chậm, trôi tin nhắn, báo sai giá/tồn kho và rò rỉ cơ hội chốt đơn.

Điểm quan trọng của bài nộp là không bắt đầu bằng “làm chatbot” hay “xây agent”, mà bắt đầu từ:

```text
Problem → Actor → Workflow → Bottleneck → Metric → Boundary → Rule / Workflow / Agent → Decision
```

---

## Cấu trúc repo

```text
Day02-MãHọcViên-HọVàTên/
├── README.md
├── 01-individual-problem-scan/
│   └── 01-individual-problem-scan.md
├── 02-group-problem-statement/
│   └── 02-group-problem-statement.md
└── 03-individual-reflection/
    └── 03-individual-reflection.md
```

---

## Nội dung từng phần

### 1. `01-individual-problem-scan/`

Phần này là bài làm cá nhân, tập trung vào việc scan problem trước khi chọn giải pháp.

Nội dung chính:

- Scan rộng 15 problems quanh AI Inbox Operator.
- Dùng nhiều lăng kính: lặp lại, tốn thời gian, AI có thể tốt hơn, pain từ người khác, chi phí.
- Chọn top 3 problems có khả năng đào sâu.
- Viết Problem Card chi tiết cho problem chính.
- Vẽ workflow hiện tại và workflow sau tối ưu bằng Mermaid.
- Xác định bước nghẽn, actor, impact, success metric, non-AI alternative và AI hypothesis.

Top 3 problems cá nhân:

| Rank | Problem | Lý do chọn |
|---|---|---|
| 1 | Inbox nhiều nền tảng bị phân tán, dễ bỏ sót và phản hồi chậm | Actor rõ, workflow rõ, pain thật với nhiều shop online |
| 2 | Câu hỏi lặp lại nhưng vẫn phải trả lời thủ công | Tần suất cao, có thể dùng Rule + Workflow để hỗ trợ |
| 3 | Không biết khách nào nên ưu tiên và follow-up | Gắn trực tiếp với doanh thu và tỷ lệ chốt đơn |

---

### 2. `02-group-problem-statement/`

Phần này là bản nộp nhóm. Nhóm đã hội tụ từ nhiều candidate problems về một bài toán chung:

```text
AI Inbox Operator — Tối ưu phễu chốt đơn Social Commerce tại Việt Nam
```

Nội dung chính:

- Group convergence từ nhiều candidate problems.
- Shortlist và score 3 đề tài tiềm năng.
- Quick validation với 30 shop/chủ shop/nhân viên liên quan.
- Research các giải pháp hiện có như Pancake/Haravan, chatbot cũ, Slack AI/Gemini.
- Workflow before/after.
- Problem Statement v0 và v1.
- So sánh Rule / Workflow / Agent.
- Final decision: Go với quy mô nhỏ.

Kết luận nhóm:

```text
Không nên tự xây một công cụ gom chat mới từ đầu.
Hướng phù hợp hơn là làm AI Workflow/Chrome Extension overlay lên công cụ shop đang dùng như Pancake.
AI hỗ trợ tra kho, tra giá và soạn draft.
Con người kiểm duyệt và bấm gửi cuối cùng.
```

---

### 3. `03-individual-reflection/`

Phần này là reflection cá nhân, ghi lại vai trò và đóng góp của tôi trong quá trình làm nhóm.

Nội dung chính:

- Vai trò cá nhân trong nhóm.
- Tôi đã đóng góp gì ở từng hoạt động.
- Tôi dùng AI như thế nào trong từng phase.
- AI hữu ích ở đâu, sai/hời hợt ở đâu.
- Tôi đã sửa gì bằng nhận định của bản thân.
- Tôi học được gì từ quá trình problem-first.
- Nếu làm lại, tôi sẽ thay đổi gì.

Bài học chính:

```text
AI tốt nhất không phải là AI làm thay hết con người,
mà là AI được đặt đúng chỗ trong workflow để giảm bottleneck,
trong khi con người vẫn giữ quyền quyết định ở điểm rủi ro cao.
```

---

## Problem Statement cuối cùng

| Field | Nội dung |
|---|---|
| **Actor** | Nhân viên trực chat chốt đơn tại các shop Social Commerce quy mô SMB tại Việt Nam |
| **Workflow** | Nhận tin nhắn đa kênh → đọc/lọc → tra cứu kho/giá → soạn câu trả lời → gửi → check sót đơn |
| **Bottleneck** | Khâu tra cứu tồn kho, giá sản phẩm và soạn câu trả lời chốt đơn mất nhiều thời gian |
| **Impact** | Gây trễ phản hồi, trôi tin nhắn, rò rỉ doanh thu và làm nhân viên quá tải |
| **Success Metric** | Giảm thời gian xử lý tin nhắn xuống dưới 30 giây/inbox; giảm tỷ lệ rớt đơn do trễ phản hồi xuống dưới 3% |
| **Boundary** | AI không tự gửi tin nhắn khi chưa có người duyệt; AI không tự ý thay đổi giá hoặc hứa sai chính sách |
| **AI intervention point** | Sau khi nhận tin nhắn và trước khi phản hồi khách hàng |
| **Mức chọn** | Workflow |
| **Rủi ro & người thật kiểm tra** | AI có thể hiểu sai tiếng lóng hoặc bịa thông tin sản phẩm; nhân viên trực chat phải kiểm duyệt trước khi gửi |

---

## Vì sao chọn Workflow?

Nhóm chọn **Workflow** thay vì Rule hoặc Agent vì:

| Mức | Nhận xét |
|---|---|
| Rule | Hữu ích cho câu hỏi đơn giản, nhưng quá cứng với tiếng lóng, câu hỏi tự nhiên và tình huống bán hàng linh hoạt |
| Workflow | Phù hợp nhất vì quy trình chốt đơn khá tuyến tính: AI tra dữ liệu → AI soạn draft → người duyệt gửi |
| Agent | Chưa phù hợp ở giai đoạn đầu vì rủi ro tự ý trả lời sai giá, sai tồn kho hoặc tự chốt đơn sai |

Kết luận:

```text
Workflow là mức cân bằng tốt nhất giữa hiệu quả và an toàn.
AI xử lý bước tốn thời gian, nhưng con người vẫn kiểm soát bước rủi ro cao.
```

---

## Workflow hiện tại

```text
CURRENT STATE

Khách nhắn/comment từ nhiều kênh
→ Nhân viên mở từng app
→ Đọc và lọc tin nhắn thủ công
→ Tra cứu tồn kho/giá/chính sách bằng Excel hoặc hệ thống rời rạc
→ Soạn câu trả lời bằng tay
→ Gửi phản hồi
→ Chốt đơn hoặc tự nhớ follow-up
→ Cuối ngày check sót đơn thủ công
```

Bottleneck chính:

- Nhảy app liên tục.
- Đọc/lọc tin thủ công.
- Tra cứu kho/giá chậm.
- Soạn câu trả lời mất thời gian.
- Không có cơ chế tự động ưu tiên khách nóng.
- Dễ quên follow-up và sót đơn.

---

## Workflow sau tối ưu

```text
FUTURE STATE

Khách nhắn/comment từ nhiều kênh
→ AI/Extension đọc nội dung tin nhắn
→ Rule/database tra sản phẩm, giá, tồn kho, chính sách
→ AI phân loại intent và mức độ ưu tiên
→ AI soạn draft câu trả lời
→ Nhân viên kiểm duyệt
→ Nhân viên bấm gửi
→ AI hỗ trợ follow-up và dashboard cuối ngày
```

Human boundary:

```text
AI không tự động gửi.
AI chỉ soạn nháp và đề xuất.
Nhân viên là người kiểm duyệt và bấm gửi cuối cùng.
```

Fallback:

```text
Nếu AI không chắc, thiếu dữ liệu hoặc case rủi ro cao,
hệ thống chuyển cho nhân viên xử lý thủ công.
```

---

## Final Decision

```text
Go với quy mô nhỏ.
```

Pilot nhỏ nhất:

- Chạy thử trên 2 shop online quen thuộc.
- Dùng 100 đơn hàng/tin nhắn đầu tiên để kiểm tra.
- Chạy bán tự động: copy tin nhắn vào prompt/RAG, AI soạn draft, nhân viên kiểm duyệt.
- Đo thời gian phản hồi, độ chính xác, tỷ lệ draft phải sửa và số case AI không chắc.

Exit / rollback:

```text
Nếu nhân viên phải sửa lại hơn 70% nội dung AI soạn nháp liên tục trong 2 tuần,
hạ cấp giải pháp về template thường + dashboard thay vì tiếp tục mở rộng AI workflow.
```

---

## Checklist đánh giá

### Cá nhân

- [x] Scan 5+ problems.
- [x] Scan rộng 8-10+ problems để lấy bonus.
- [x] Có top 3 Problem Cards.
- [x] Có problem card chi tiết.
- [x] Có workflow trước/sau.
- [x] Có reflection cá nhân.
- [x] Có giải thích rõ cách dùng AI và điều chỉnh bằng nhận định cá nhân.

### Nhóm

- [x] Có group convergence.
- [x] Có shortlist và score.
- [x] Có quick validation.
- [x] Có research giải pháp đã có.
- [x] Có workflow before/after.
- [x] Có Problem Statement v0/v1.
- [x] Có so sánh Rule / Workflow / Agent.
- [x] Có final decision Go / Not Yet / No-Go.

---

## Ghi chú

Bài nộp này tập trung vào chất lượng lập luận hơn là độ “ngầu” của solution. AI được xem là công cụ hỗ trợ trong workflow, không phải giải pháp mặc định cho mọi bước. Những phần cần quyết định cuối cùng như gửi tin nhắn, cam kết giá/tồn kho, xử lý khiếu nại và chốt đơn vẫn cần con người kiểm soát.
