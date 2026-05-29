# 03 — Individual Reflection

## Case: AI Inbox Operator — Tối ưu phễu chốt đơn Social Commerce tại Việt Nam

> Reflection này ghi lại vai trò cá nhân của tôi trong quá trình nhóm chọn và phát triển bài toán **AI Inbox Operator**. Ý tưởng ban đầu xuất phát từ pain tôi quan sát về inbox đa kênh của shop online, sau đó nhóm đã cùng nhau thu hẹp và làm rõ thành bài toán: **tối ưu phễu chốt đơn Social Commerce cho shop SMB tại Việt Nam**.

---

# 1. Đóng góp của tôi trong nhóm

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng |
|---|---|---|
| Scan cá nhân | Tôi đưa ra nhiều problem xoay quanh AI Inbox Operator: inbox đa kênh bị trôi, trả lời câu hỏi lặp lại, không biết khách nào là khách nóng, follow-up thủ công, chi phí nhân sự tăng khi lượng inbox tăng | Nhóm có một candidate mạnh về chăm sóc khách hàng/chốt đơn, có actor rõ và workflow có thể vẽ được |
| Pitch Problem Card | Tôi pitch vấn đề shop online nhận quá nhiều tin nhắn từ Facebook, Zalo, Shopee, TikTok, Instagram và livestream, khiến nhân viên phải mở nhiều app, đọc thủ công, tra kho/giá và dễ bỏ sót khách | Bài AI Inbox Operator được nhóm đưa vào shortlist và cuối cùng được chọn làm đề tài nhóm |
| Challenge / phản biện | Tôi đặt câu hỏi về việc problem này nên dừng ở mức gom inbox, rule/template hay cần AI workflow; đồng thời hỏi rủi ro nếu AI tự trả lời sai giá/tồn kho | Nhóm không đi theo hướng chatbot tự động 100%, mà chọn hướng Hybrid: AI soạn draft, con người duyệt và gửi |
| Gom trùng / cluster | Tôi cùng nhóm gom các candidate liên quan tới inbox, FAQ, follow-up và sales workflow vào cluster “Chăm sóc khách hàng / chốt đơn” | Nhóm nhìn rõ pattern chung: không chỉ là trả lời tin nhắn, mà là tối ưu tốc độ giao tiếp và phễu chuyển đổi khách nóng |
| Chọn candidate problem | Tôi ủng hộ chọn AI Inbox Operator vì actor rõ, workflow rõ, pain có evidence, impact đo được bằng thời gian phản hồi và tỷ lệ chốt đơn | Nhóm thống nhất chọn **AI Inbox Operator (Tối ưu phễu chốt đơn Social Commerce)** với điểm cao nhất trong bảng score |
| Validation / kiểm chứng nhanh | Tôi đóng góp hướng cần khảo sát chủ shop/nhân viên inbox về số lượng tin nhắn/ngày, tình trạng trôi tin, phản hồi trễ, sai giá/tồn kho và khách rời đi nếu phản hồi chậm | Nhóm đưa vào báo cáo phần khảo sát/phỏng vấn nhanh 30 shop, giúp bài có evidence rõ hơn thay vì chỉ dựa vào cảm giác |
| Research giải pháp | Tôi cùng nhóm phân tích các tool hiện có như Pancake/Haravan, chatbot tự động cũ, Slack AI/Gemini để xem họ giải quyết bước nào và còn khoảng trống gì | Nhóm nhận ra không nên tự xây hub chat mới từ đầu, mà nên đi theo hướng Chrome Extension/overlay tích hợp lên Pancake để giảm CAC và tránh đối đầu trực diện |
| Workflow trước/sau | Tôi hỗ trợ vẽ và làm rõ current workflow/future workflow: hiện tại nhân viên nhảy app, lọc tin, tra Excel, soạn tay; tương lai AI tra kho, soạn draft, nhân viên duyệt gửi | Nhóm có workflow trước/sau rõ ràng, nhìn được bottleneck, AI intervention point, human boundary và fallback khi AI sai |
| Problem Statement | Tôi đóng góp vào việc làm rõ actor, bottleneck, impact, success metric và boundary của Problem Statement v0/v1 | Problem Statement được thu hẹp hơn: không còn là “AI trả lời inbox chung chung”, mà là “AI hỗ trợ chốt đơn nhanh, chính xác, có người duyệt” |
| Rule / Workflow / Agent | Tôi lập luận rằng bài này nên chọn **Workflow**, không chọn Agent ngay, vì quy trình chốt đơn khá tuyến tính nhưng cần độ chính xác cao với giá/tồn kho | Nhóm thống nhất chọn Workflow: AI tra kho → AI soạn draft → người duyệt gửi |
| Final decision | Tôi ủng hộ quyết định **Go với quy mô nhỏ**, bắt đầu bằng pilot 2 shop, 100 đơn hàng đầu tiên, đo độ chính xác và tỷ lệ draft cần sửa | Nhóm có decision thực tế hơn, có scope nhỏ, có exit/rollback nếu AI draft không đủ tốt |

---

# 2. Vai trò cá nhân của tôi trong nhóm

Vai trò chính của tôi là người đưa ra bài toán ban đầu và kéo nhóm đi theo hướng **problem-first** thay vì **AI-first**.

Ban đầu, ý tưởng “AI Inbox Operator” rất dễ bị hiểu thành một chatbot tự động trả lời khách hàng. Tuy nhiên, sau khi phân tích workflow, tôi nhận ra pain thật không chỉ nằm ở việc trả lời tin nhắn, mà nằm ở toàn bộ quy trình chốt đơn:

```text
Khách nhắn tin
→ Nhân viên đọc/lọc
→ Tra giá/tồn kho
→ Soạn câu trả lời
→ Phản hồi khách
→ Chốt đơn hoặc follow-up
→ Check sót đơn cuối ngày
```

Tôi đóng góp nhiều nhất ở 4 điểm:

1. Đưa ra candidate problem ban đầu về inbox đa kênh của shop online.
2. Làm rõ bottleneck: tra kho/giá và soạn câu trả lời mất thời gian, dễ sai, dễ làm khách rời đi.
3. Gợi ý hướng giải không phải chatbot tự động 100%, mà là AI workflow có người duyệt.
4. Nhấn mạnh metric và boundary: phản hồi dưới 30 giây, giảm rớt đơn, AI không tự gửi khi chưa được nhân viên duyệt.

---

# 3. Bảng dùng AI trong reflection

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai/hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| Scan | Tôi dùng AI để mở rộng danh sách problem quanh AI Inbox Operator cho shop online Việt Nam | AI giúp tôi nghĩ thêm các pain như inbox đa kênh, câu hỏi lặp lại, khách nóng bị trôi, follow-up thủ công, chi phí nhân sự và cost per conversation | Một số gợi ý ban đầu hơi rộng, dễ biến thành “làm chatbot bán hàng tự động” hoặc “AI agent thay toàn bộ nhân viên” | Tôi giữ lại những problem có workflow thật và actor rõ, bỏ các ý quá rộng hoặc chưa có dấu hiệu pain cụ thể |
| Problem Card | Tôi dùng AI để phản biện Problem Card: actor đã rõ chưa, bottleneck có cụ thể không, metric có đo được không, rule có đủ không | AI giúp tôi làm rõ các field như actor, current workflow, bottleneck, success metric, non-AI alternative và AI hypothesis | AI có xu hướng làm problem nghe lớn hơn, ví dụ muốn gom cả CRM, chatbot, tạo đơn, follow-up và dashboard vào một sản phẩm ngay từ đầu | Tôi thu hẹp lại thành bài toán chính: nhân viên trực chat chốt đơn bị chậm do phải tra kho/giá và soạn câu trả lời thủ công |
| Workflow | Tôi nhờ AI hỗ trợ chuyển mô tả workflow thành Mermaid current/future workflow | AI giúp tôi vẽ rõ luồng trước/sau, đánh dấu bottleneck, AI intervention point, human boundary và fallback | Flow ban đầu hơi dài và có nguy cơ ôm quá nhiều tính năng như CRM, tạo đơn, phân tích doanh thu, chăm sóc khách cũ | Tôi cùng nhóm giữ lại các bước quan trọng nhất cho lab: nhận tin → lọc → tra kho → draft → người duyệt gửi → follow-up/check sót |
| Research | Tôi dùng AI để gợi ý cách phân tích đối thủ và khoảng trống thị trường | AI giúp tôi nhìn ra không nên claim “chưa ai làm”, vì thị trường đã có Pancake, Haravan, chatbot cũ và các công cụ AI khác | AI có thể đưa claim quá mạnh nếu không kiểm chứng, ví dụ “sản phẩm này chưa có ai làm” hoặc “AI chắc chắn giảm doanh thu rò rỉ X%” | Tôi chỉ giữ luận điểm an toàn: thị trường đã có công cụ gom chat/chatbot, nhưng khoảng trống là AI hỗ trợ soạn draft chốt đơn nhanh, có RAG với kho/giá và người duyệt |
| Quick validation | Tôi dùng AI để gợi ý câu hỏi phỏng vấn chủ shop/nhân viên trực chat | AI giúp đề xuất các câu hỏi như: một ngày có bao nhiêu tin, có bị trôi tin không, mất bao lâu để tra kho, khách có bỏ đi nếu phản hồi chậm không | AI không thể thay thế dữ liệu thật từ shop; nếu chỉ dựa vào AI thì evidence sẽ yếu | Nhóm dùng hướng câu hỏi đó để trình bày khảo sát/phỏng vấn nhanh 30 shop và rút ra insight cụ thể hơn |
| Problem Statement | Tôi dùng AI để kiểm tra xem Problem Statement v0 có bị mơ hồ không | AI giúp tôi thấy cần làm rõ actor, workflow, bottleneck, impact, success metric và boundary | AI có xu hướng viết problem statement quá dài, đôi khi trộn cả solution vào problem | Tôi rút lại thành các field ngắn, đo được và bám vào workflow thật của nhân viên trực chat |
| Rule / Workflow / Agent | Tôi dùng AI để so sánh 3 mức Rule / Workflow / Agent | AI giúp tôi thấy Rule quá cứng với tiếng lóng/ngôn ngữ tự nhiên, Agent thì quá rủi ro nếu tự gửi hoặc tự chốt đơn | AI đôi khi gợi ý Agent quá sớm vì nghe “AI Inbox Operator” giống một hệ thống tự động toàn phần | Tôi cùng nhóm chọn Workflow vì phù hợp nhất: AI tra kho/giá và soạn draft, nhân viên duyệt gửi |
| Decision | Tôi dùng AI để gợi ý tiêu chí Go / Not Yet / No-Go và pilot nhỏ nhất | AI giúp tôi nghĩ rõ hơn về pilot: thử trên 2 shop, 100 đơn đầu tiên, đo tỷ lệ draft cần sửa và thời gian phản hồi | AI không thể tự chốt decision thay nhóm vì cần dữ liệu thật và sự đồng thuận của các thành viên | Tôi đề xuất Go với scope nhỏ, có exit/rollback nếu nhân viên phải sửa hơn 70% draft trong 2 tuần |

---

# 4. Tôi học được gì?

## 4.1. Problem tốt không phải problem nghe “AI” nhất

Tôi học được rằng một problem tốt không phải là problem nghe hiện đại nhất, có nhiều AI nhất hay giống “agent” nhất. Một problem tốt phải có:

- actor rõ,
- workflow vẽ được,
- bottleneck cụ thể,
- metric đo được,
- boundary rõ,
- có thể so sánh No AI / Rule / Workflow / Agent.

Ban đầu “AI Inbox Operator” nghe khá rộng. Nếu không phân tích kỹ, rất dễ biến nó thành một chatbot/agent tự động bán hàng. Nhưng khi vẽ workflow, tôi thấy bài toán đáng làm nhất không phải “AI nói chuyện thay người”, mà là **giảm thời gian tra kho/giá và soạn câu trả lời chốt đơn cho nhân viên trực chat**.

## 4.2. Vẽ workflow giúp nhìn rõ điểm nghẽn

Trước khi vẽ workflow, tôi chỉ nghĩ chung là “shop bị quá tải inbox”. Sau khi vẽ current workflow, tôi thấy rõ các điểm nghẽn:

```text
Nhảy app liên tục
→ Đọc lọc thủ công
→ Tra cứu Excel/kho thủ công
→ Soạn câu trả lời bằng tay
→ Check sót đơn cuối ngày
```

Trong đó, bottleneck quan trọng nhất không chỉ là “nhiều tin nhắn”, mà là **biến dữ liệu thô như giá, tồn kho, phí ship, chính sách thành câu trả lời cá nhân hóa đủ nhanh để giữ khách nóng**.

## 4.3. Agent không phải đích đến mặc định

Tôi học được rằng không nên chọn Agent chỉ vì sản phẩm có chữ “AI Operator”. Trong case này, Agent tự động trả lời và tự chốt đơn có rủi ro cao:

- báo sai giá,
- báo sai tồn kho,
- hiểu sai tiếng lóng,
- tự hứa chính sách không có thật,
- làm khách bực vì cảm giác đang nói chuyện với robot,
- gây thiệt hại tài chính nếu gửi sai thông tin.

Vì vậy, Workflow hợp lý hơn Agent. Workflow vẫn tận dụng AI ở bước cần hiểu ngôn ngữ và soạn thảo, nhưng giữ con người ở điểm quyết định cuối cùng.

## 4.4. Human boundary là phần cốt lõi, không phải chi tiết phụ

Trong bài này, human boundary rất quan trọng:

```text
AI có thể tra kho và soạn nháp
Nhưng nhân viên trực chat là người kiểm duyệt và bấm gửi cuối cùng
```

Điều này giúp giảm rủi ro hallucination và giữ trải nghiệm tự nhiên với khách hàng. Nếu AI sai, người thật còn có cơ hội phát hiện trước khi gửi. Đây cũng là lý do nhóm chọn hướng Hybrid thay vì auto-reply 100%.

## 4.5. Research không phải để copy tool, mà để thấy khoảng trống

Khi research Pancake/Haravan/chatbot cũ, tôi nhận ra thị trường đã có nhiều công cụ gom chat và quản lý hội thoại. Vì vậy, nếu nói “chúng tôi làm tool inbox đa kênh” thì không đủ khác biệt.

Khoảng trống hợp lý hơn là:

```text
AI hỗ trợ nhân viên trực chat chốt đơn nhanh hơn ngay trên workflow hiện có,
đặc biệt ở bước tra kho/giá và soạn draft câu trả lời.
```

Vì vậy, nhóm chọn hướng Chrome Extension overlay lên Pancake thay vì tự xây một hub chat mới từ đầu. Đây là một thay đổi quan trọng vì nó giúp giảm scope, giảm CAC và tránh đối đầu trực diện với các nền tảng lớn.

---

# 5. Nhóm có lúc nào bị solution-first không?

Có. Ngay từ tên “AI Inbox Operator”, cả tôi và nhóm rất dễ nghĩ tới solution trước: chatbot, agent, tự động trả lời, tự động chốt đơn, tự động tạo đơn.

Tuy nhiên, sau khi quay lại worksheet, tôi nhận ra cần đi theo mạch:

```text
Problem
→ Actor
→ Workflow hiện tại
→ Bottleneck
→ Metric
→ Boundary
→ Mức AI phù hợp
```

Khi làm theo mạch này, nhóm không còn nói chung chung “làm AI trả lời inbox” nữa, mà thu hẹp thành:

```text
Nhân viên trực chat shop SMB bị chậm ở khâu tra cứu tồn kho/giá và soạn câu trả lời chốt đơn.
AI hỗ trợ tra cứu và soạn draft.
Người thật kiểm duyệt và bấm gửi.
```

Đây là bước chuyển từ solution-first sang problem-first.

---

# 6. Tôi có thay đổi ý kiến sau khi bị challenge không?

Có.

Ban đầu tôi nghĩ AI Inbox Operator có thể tiến khá gần tới một agent tự động xử lý nhiều bước: đọc tin, phân loại khách, trả lời, nhắc follow-up, thậm chí hỗ trợ chốt đơn. Nhưng sau khi nhóm challenge về rủi ro sai giá/tồn kho và trải nghiệm khách hàng, tôi thay đổi quan điểm.

Tôi thấy giai đoạn đầu nên chọn Workflow, không chọn Agent. AI chỉ nên:

- đọc hiểu tin nhắn,
- tra thông tin từ database/kho/giá,
- soạn draft câu trả lời,
- gợi ý ưu tiên/follow-up.

Còn người thật vẫn phải:

- kiểm tra nội dung,
- bấm gửi,
- xử lý khiếu nại,
- quyết định giảm giá,
- xác nhận đơn hàng.

Sự thay đổi này làm bài toán an toàn hơn và khả thi hơn trong một pilot nhỏ.

---

# 7. Tôi đóng góp gì thật sự vào artifact cuối?

Tôi đóng góp thật sự vào artifact cuối ở các phần:

1. **Ý tưởng gốc:** đưa ra hướng AI Inbox Operator từ pain inbox đa kênh của shop online.
2. **Problem framing:** giúp nhóm không chỉ nói “chatbot”, mà nói rõ actor là nhân viên trực chat chốt đơn tại shop SMB.
3. **Workflow:** đóng góp current/future workflow, chỉ rõ bước nghẽn là tra kho/giá và soạn câu trả lời.
4. **Boundary:** nhấn mạnh AI không tự gửi, con người kiểm duyệt cuối cùng.
5. **RWA decision:** lập luận chọn Workflow, không chọn Agent.
6. **Go decision:** ủng hộ pilot nhỏ thay vì build full product ngay.
7. **Investor/cost thinking:** bổ sung góc chi phí, cost per conversation, giảm workload nhân sự và tăng tỷ lệ chốt đơn.

---

# 8. Điều khó nhất khi viết Problem Statement là gì?

Điều khó nhất là **thu hẹp scope**.

AI Inbox Operator có thể mở rộng ra rất nhiều hướng:

- gom inbox đa kênh,
- chatbot trả lời FAQ,
- CRM khách hàng,
- tạo đơn tự động,
- chăm sóc khách cũ,
- phân tích doanh thu,
- nhắc follow-up,
- đánh giá hiệu suất nhân viên,
- agent tự động bán hàng.

Nếu đưa hết vào Problem Statement, bài sẽ quá rộng và khó đo. Vì vậy, nhóm phải thu hẹp lại thành một workflow cụ thể:

```text
Nhân viên trực chat nhận tin
→ đọc/lọc
→ tra kho/giá
→ soạn câu trả lời
→ duyệt gửi
→ check sót/follow-up
```

Sau khi thu hẹp, Problem Statement rõ hơn nhiều:

- Actor rõ: nhân viên trực chat chốt đơn.
- Bottleneck rõ: tra tồn kho/giá và soạn câu trả lời mất 5-7 phút/inbox.
- Impact rõ: trễ phản hồi, trôi tin, rò rỉ doanh thu.
- Metric rõ: phản hồi dưới 30 giây/inbox, giảm rớt đơn do trễ phản hồi.
- Boundary rõ: AI không tự gửi nếu chưa có người duyệt.

---

# 9. Nếu làm lại, tôi sẽ thay đổi gì?

Nếu làm lại, tôi sẽ làm 4 việc tốt hơn.

## 9.1. Validate dữ liệu thật sớm hơn

Tôi sẽ hỏi trực tiếp nhiều shop hơn trước khi chốt các con số như:

- 200-1000 tin/ngày,
- 5-7 phút/inbox,
- rò rỉ 15% doanh thu,
- rớt đơn do phản hồi trễ,
- mục tiêu dưới 30 giây/inbox.

Các con số này rất quan trọng, nên cần phân biệt rõ đâu là dữ liệu khảo sát thật, đâu là giả định cần validate thêm.

## 9.2. Tách rõ “gom inbox” và “AI chốt đơn”

Ban đầu tôi hơi trộn hai bài toán:

```text
Gom inbox đa kênh
và
AI hỗ trợ chốt đơn
```

Sau research, nhóm thấy gom inbox đã có nhiều tool như Pancake/Haravan. Vì vậy, nếu làm lại, tôi sẽ định vị ngay từ đầu là:

```text
Không xây hub chat mới.
Xây AI workflow overlay trên công cụ shop đang dùng.
```

## 9.3. Làm rõ hơn cost/ROI

Tôi sẽ bổ sung bảng tính sơ bộ:

```text
Cost per conversation
Cost LLM per draft
Thời gian nhân viên tiết kiệm được
Doanh thu giữ lại từ khách nóng không bị rớt
Giá SaaS 299k/user/tháng có hợp lý không
```

Điều này giúp bài thuyết phục hơn nếu nhìn từ góc nhà đầu tư hoặc chủ shop.

## 9.4. Challenge mạnh hơn về rủi ro AI sai

Tôi sẽ hỏi nhóm kỹ hơn:

- Nếu AI báo sai tồn kho thì ai chịu trách nhiệm?
- Nếu AI hiểu sai tiếng lóng thì fallback thế nào?
- Nếu nhân viên quá tin AI và bấm gửi sai thì sao?
- Có cần confidence score trước khi hiện draft không?
- Case nào bắt buộc escalate cho người thật?

Những câu hỏi này giúp boundary chắc hơn.

---

# 10. Bài học cuối cùng

Bài học lớn nhất của tôi là:

```text
AI tốt nhất không phải là AI làm thay hết con người,
mà là AI đặt đúng chỗ trong workflow để giảm bottleneck,
trong khi con người vẫn giữ quyền quyết định ở điểm rủi ro cao.
```

Với AI Inbox Operator, hướng tốt nhất không phải là chatbot tự động trả lời 100%. Hướng hợp lý hơn là:

```text
AI tra dữ liệu
→ AI soạn draft
→ Nhân viên kiểm duyệt
→ Nhân viên gửi
→ AI hỗ trợ follow-up và dashboard
```

Tôi cũng học được rằng muốn bài toán AI thuyết phục thì phải nói được cả 5 phần:

1. Problem thật là gì?
2. Workflow hiện tại nghẽn ở đâu?
3. Metric đo cải thiện là gì?
4. Boundary của AI nằm ở đâu?
5. Vì sao chọn Workflow thay vì Rule hoặc Agent?

Trong case này, tôi thấy nhóm chọn **Workflow** là hợp lý nhất vì nó cân bằng giữa hiệu quả và an toàn. Rule quá cứng với ngôn ngữ tự nhiên và tiếng lóng của khách Việt. Agent thì quá rủi ro nếu tự động gửi hoặc tự quyết định chốt đơn. Workflow giúp AI hỗ trợ đúng điểm nghẽn nhưng vẫn có người thật kiểm soát.

---