---
name: he-thong-affiliate-ai
description: Bản đồ điều phối (playbook) kết nối bộ 52 skill affiliate marketing từ Affitor/affiliate-skills với các skill nội dung riêng của dự án (content-sale-page, dao-dien-ai) thành một hệ thống sản xuất nội dung khép kín, chuyên biệt cho ngách AI (công cụ AI, khóa học AI, phần mềm AI). Dùng file này khi người dùng muốn quảng bá/affiliate một công cụ hoặc khóa học AI cụ thể, muốn biết dùng skill nào ở bước nào, hoặc muốn lên roadmap toàn bộ funnel affiliate AI.
---

# Hệ Thống Affiliate AI — Playbook Điều Phối

Đây không phải một skill mới độc lập, mà là **bản đồ kết nối** giữa 3 nguồn:

1. **52 skill affiliate** từ [Affitor/affiliate-skills](https://github.com/Affitor/affiliate-skills), đã đăng ký vào project tại `.claude/skills/{ten-skill}/SKILL.md` (8 giai đoạn S1-S8).
2. **`.claude/skills/content-sale-page/SKILL.md`** — skill tự viết, chuyên viết content trang bán hàng dựa trên nghiên cứu nội dung win.
3. **`.claude/skills/dao-dien-ai/SKILL.md`** — skill tự viết, dựng shotlist đạo diễn cho video Google Flow, dùng để sản xuất video demo/quảng cáo.

Toàn bộ 55 skill (52 + 2 skill riêng + playbook này) đều nằm phẳng trong `.claude/skills/` theo đúng convention project-skill của Claude Code — mỗi skill một thư mục con tên khớp với skill, chứa `SKILL.md`. Khi người dùng nhắc tới quảng bá công cụ AI (HeyGen, Synthesia, Midjourney, ChatGPT plugin, khóa học AI...), đọc SKILL.md tương ứng trong `.claude/skills/{ten-skill}/` và làm theo đúng workflow trong đó — không cần đăng ký gì thêm, chỉ có thể cần Claude Code quét lại project ở phiên làm việc mới để skill xuất hiện trong danh sách `/` lệnh.

## Vì Sao Chuyên Biệt Cho Ngách AI

Ngách AI có 3 đặc điểm khác các ngách affiliate khác, cần lưu ý khi áp dụng các skill bên dưới:

- **Thay đổi rất nhanh**: công cụ AI ra bản mới/tính năng mới hàng tuần → ưu tiên chạy `trending-content-scout` và `content-research-brief` thường xuyên hơn thay vì viết một lần dùng mãi.
- **Cạnh tranh cực cao trên các "ông lớn"** (ChatGPT, Midjourney...) → dùng `monopoly-niche-finder` và `purple-cow-audit` để tìm góc ngách hẹp (vd: "AI cho kế toán nhỏ lẻ" thay vì "AI nói chung").
- **Nhiều chương trình affiliate SaaS có hoa hồng recurring cao** → khi chạy `affiliate-program-search`, ưu tiên lọc theo `recurring commission` và `cookie days` dài, không chỉ theo % hoa hồng.

## Luồng Chạy Đề Xuất Cho Một Công Cụ/Khóa Học AI Cụ Thể

Khi người dùng nói "tôi muốn quảng bá [công cụ AI X]" hoặc "giúp tôi lên hệ thống affiliate cho ngách AI [Y]", chạy theo thứ tự sau, mỗi bước đọc SKILL.md tương ứng:

### Bước 1 — Research (S1)
- `.claude/skills/affiliate-program-search/SKILL.md` — tìm chương trình affiliate của công cụ AI đó, so sánh hoa hồng/cookie.
- `.claude/skills/trending-content-scout/SKILL.md` — quét YouTube/TikTok/X/Reddit xem content nào về công cụ này đang viral, hook nào ăn khách.
- `.claude/skills/competitor-spy/SKILL.md` — xem các affiliate khác đang quảng bá công cụ này thế nào.
- `.claude/skills/niche-opportunity-finder/SKILL.md` hoặc `monopoly-niche-finder/SKILL.md` — nếu chưa chốt công cụ cụ thể, tìm ngách AI còn trống.

### Bước 2 — Content (S2 + skill riêng)
- `.claude/skills/content-research-brief/SKILL.md` — thu thập nguồn thật, số liệu thật về công cụ (funding, số người dùng, tính năng mới).
- `.claude/skills/viral-post-writer/SKILL.md`, `twitter-thread-writer`, `reddit-post-writer` — viết bài mạng xã hội dựa trên research trên.
- `.claude/skills/tiktok-script-writer/SKILL.md` — viết kịch bản video ngắn demo công cụ.
- **`.claude/skills/dao-dien-ai/SKILL.md`** — khi kịch bản TikTok/demo cần dựng thành shotlist quay bằng Google Flow (cảnh, cú máy, continuity), đưa kịch bản từ bước trên vào đây để ra file HTML shotlist.
- `.claude/skills/infographic-generator/SKILL.md` — dựng infographic so sánh nếu cần.

### Bước 3 — Blog/SEO (S3, tùy chọn)
- `comparison-post-writer` (X vs Y), `listicle-generator` ("Top N công cụ AI cho..."), `how-to-tutorial-writer` — nếu kênh chính là blog/SEO, không bắt buộc nếu chỉ chạy social + landing page.

### Bước 4 — Offer & Trang Bán Hàng (S4 + skill riêng)
- `.claude/skills/grand-slam-offer/SKILL.md` — thiết kế offer theo Value Equation (Hormozi) cho gói giới thiệu công cụ AI của bạn.
- `.claude/skills/bonus-stack-builder/SKILL.md` — tạo bonus riêng (vd: template prompt, mini-course) chỉ có khi mua qua link affiliate của bạn — đây là lợi thế cạnh tranh quan trọng nhất trong affiliate SaaS AI.
- `.claude/skills/guarantee-generator/SKILL.md` — nếu bán kèm sản phẩm số của riêng bạn (không phải affiliate thuần).
- **`.claude/skills/content-sale-page/SKILL.md`** — dùng skill này để viết toàn bộ copy trang bán hàng (13 block) dựa trên research + offer đã thiết kế ở trên.
- `.claude/skills/landing-page-creator/SKILL.md` hoặc `product-showcase-page/SKILL.md` — dựng HTML trang đích từ content vừa viết.

### Bước 5 — Distribution (S5)
- `bio-link-deployer`, `social-media-scheduler`, `email-drip-sequence`, `github-pages-deployer` — đưa nội dung/trang lên và lên lịch đăng.

### Bước 6 — Analytics (S6, vòng lặp ngược về S1)
- `conversion-tracker`, `ab-test-generator`, `performance-report` — đo hiệu quả, kết quả này quay lại nuôi Bước 1 cho vòng lặp tiếp theo.

### Bước 7-8 — Automation & Meta (khi cần)
- `paid-ad-copy-writer` nếu chạy ads trả phí, `content-repurposer` để tái sử dụng 1 bài thành nhiều định dạng.
- `funnel-planner` khi người dùng muốn roadmap tổng thể theo số giờ/tuần rảnh.
- `compliance-checker` — **luôn chạy trước khi đăng bất kỳ content affiliate AI nào**, vì FTC yêu cầu disclosure rõ ràng.
- `skill-finder` khi không chắc dùng skill nào.

## Quy Tắc Khi Điều Phối

- Không cần người dùng tự gọi từng skill — khi họ mô tả nhu cầu bằng ngôn ngữ tự nhiên (vd: "tìm công cụ AI viết content đang hot rồi viết bài LinkedIn"), tự xác định bước tương ứng trong luồng trên, đọc đúng SKILL.md, và thực hiện.
- Luôn ưu tiên dữ liệu thật (research-backed) trước khi viết — không bịa số liệu/testimonial, đúng nguyên tắc đã đặt ra trong `content-sale-page.md`.
- Khi output là video, luôn bàn giao kịch bản sang `dao-dien-ai.md` thay vì tự viết prompt Google Flow trong skill khác.
- Khi output là trang bán hàng, luôn bàn giao content đã viết sang skill landing tương ứng để dựng HTML, không viết HTML tay trong bước content.
- Ghi rõ nguồn/skill nào vừa được dùng khi trả lời, để người dùng biết hệ thống đang chạy bước nào trong 8 giai đoạn.

## Ghi Chú Cài Đặt

- Đã đăng ký 55 skill (52 từ affiliate-skills + content-sale-page + dao-dien-ai + playbook này) vào `D:\skill\.claude\skills\{ten-skill}\SKILL.md` — đúng convention project-skill mà Claude Code quét tự động. `affiliate-skills/` (README, registry.json, shared/references, API.md) vẫn giữ lại làm tài liệu tham chiếu gốc, không phải nơi các skill được đọc từ đó nữa.
- Vì danh sách skill khả dụng của một phiên chat được nạp lúc phiên bắt đầu, các skill mới đăng ký này có thể chưa hiện ra trong menu `/` ở phiên hiện tại — mở phiên làm việc mới tại `D:\skill` để Claude Code quét lại `.claude/skills/` và các lệnh `/ten-skill` xuất hiện đầy đủ. Trong lúc chờ, tôi vẫn có thể đọc và làm theo bất kỳ SKILL.md nào trực tiếp khi bạn mô tả nhu cầu.
- Bỏ qua skill gốc `affiliate-check` (cần build binary bằng Bun, không phải Markdown thuần) — nếu muốn dùng CLI tra cứu chương trình affiliate trực tiếp, cần cài Bun và chạy `./setup` thủ công, không bắt buộc cho luồng làm việc chính.
- Repo gốc còn gợi ý companion tool `hidrix-tools` (MCP server 16 tool: web/X/Reddit/TikTok/YouTube search, scraping, traffic analytics) để các skill research có dữ liệu thật thay vì chỉ dựa vào WebSearch — cân nhắc cài nếu cần dữ liệu engagement chính xác, nhưng cần API keys riêng.
