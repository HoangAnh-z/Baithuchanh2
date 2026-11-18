**PROMPT 1**

```text
[Role] Chuyên gia nghiên cứu thị trường B2B.

[Context] Phòng Marketing chuẩn bị bài PR giới thiệu giải pháp AI Chatbot mới cho doanh nghiệp.

[Task]
1. Xác định 3 nhóm khách hàng mục tiêu (ngành, quy mô, vai trò ra quyết định).
2. Với mỗi nhóm, liệt kê 3-4 nỗi đau (pain points) mà AI Chatbot giải quyết.
3. Với mỗi pain point, nêu 1 tính năng chatbot giải quyết được.

[Explantion] Không viết bài PR. Không bịa số liệu; nếu cần số liệu, ghi "[cần xác minh]".

[Tone]: Chuyên nghiệp, ngắn gọn.

[Extras]: Định dạng JSON bao gồm:
{
  "nhom_khach_hang": [
    {"ten": "", "mo_ta": "",
     "pain_points": [{"van_de": "", "tinh_nang_giai_quyet": ""}]}
  ],
  "tu_khoa_goi_y": ["", "", ""]
}
```
**Chạy thử PROMPT 1**

```JSON
{
  "nhom_khach_hang": [
    {
      "ten": "Nhóm 1: Doanh nghiệp bán lẻ & thương mại điện tử quy mô vừa",
      "mo_ta": "Ngành: bán lẻ, TMĐT, F&B chuỗi. Quy mô: 50-300 nhân sự, có kênh bán online (website, Facebook, Zalo, sàn TMĐT). Người ra quyết định: Giám đốc Kinh doanh/Marketing (đề xuất), CEO/Chủ doanh nghiệp (phê duyệt ngân sách).",
      "pain_points": [
        {
          "van_de": "Khách nhắn tin ngoài giờ hành chính nhưng không có người trả lời, mất đơn hàng",
          "tinh_nang_giai_quyet": "Trả lời tự động 24/7 trên đa kênh (website, Facebook, Zalo)"
        },
        {
          "van_de": "Nhân viên CSKH quá tải vào mùa cao điểm (Black Friday, Tết), phải trả lời lặp đi lặp lại các câu hỏi giống nhau",
          "tinh_nang_giai_quyet": "Thư viện FAQ thông minh tự xử lý câu hỏi thường gặp (giá, tồn kho, chính sách đổi trả)"
        },
        {
          "van_de": "Khách hỏi tình trạng đơn hàng liên tục, tốn nhân lực tra cứu thủ công",
          "tinh_nang_giai_quyet": "Tích hợp hệ thống đơn hàng/vận chuyển để tra cứu trạng thái theo thời gian thực"
        },
        {
          "van_de": "Bỏ lỡ cơ hội upsell/cross-sell vì tư vấn không nhất quán giữa các nhân viên",
          "tinh_nang_giai_quyet": "Gợi ý sản phẩm theo ngữ cảnh hội thoại và lịch sử mua hàng"
        }
      ]
    },
    {
      "ten": "Nhóm 2: Ngân hàng, tài chính, bảo hiểm (BFSI) quy mô vừa và lớn",
      "mo_ta": "Ngành: ngân hàng, công ty tài chính, bảo hiểm, fintech. Quy mô: 300+ nhân sự, có tổng đài/contact center. Người ra quyết định: Giám đốc Trải nghiệm khách hàng (CX), Giám đốc Công nghệ (CTO/CIO), kèm bộ phận Tuân thủ/Bảo mật tham gia thẩm định.",
      "pain_points": [
        {
          "van_de": "Chi phí vận hành tổng đài cao, thời gian chờ máy của khách dài",
          "tinh_nang_giai_quyet": "Chatbot xử lý tầng 1 (tra cứu số dư, biểu phí, thủ tục) giảm tải cho tổng đài viên"
        },
        {
          "van_de": "Yêu cầu bảo mật và tuân thủ dữ liệu khách hàng nghiêm ngặt",
          "tinh_nang_giai_quyet": "Xác thực người dùng, mã hóa dữ liệu hội thoại, phân quyền truy cập và nhật ký kiểm toán (audit log)"
        },
        {
          "van_de": "Quy trình mở sản phẩm/nộp hồ sơ phức tạp khiến khách bỏ dở giữa chừng",
          "tinh_nang_giai_quyet": "Hướng dẫn từng bước và thu thập thông tin hồ sơ qua hội thoại"
        },
        {
          "van_de": "Chuyển cuộc gọi qua lại giữa nhiều bộ phận, khách phải lặp lại thông tin",
          "tinh_nang_giai_quyet": "Chuyển giao sang nhân viên thật (human handoff) kèm tóm tắt toàn bộ ngữ cảnh cuộc trò chuyện"
        }
      ]
    },
    {
      "ten": "Nhóm 3: Doanh nghiệp B2B dịch vụ, SaaS và giáo dục/đào tạo",
      "mo_ta": "Ngành: phần mềm/SaaS, dịch vụ chuyên nghiệp, trung tâm đào tạo, bất động sản. Quy mô: 20-200 nhân sự, đội sales và hỗ trợ nhỏ. Người ra quyết định: Trưởng phòng Sales/Customer Success (người dùng chính), Giám đốc Vận hành hoặc CEO (duyệt chi).",
      "pain_points": [
        {
          "van_de": "Lượng lớn lead đổ về nhưng đội sales không đủ người sàng lọc, lead chất lượng bị bỏ sót",
          "tinh_nang_giai_quyet": "Chấm điểm và phân loại lead tự động qua câu hỏi sàng lọc trong hội thoại"
        },
        {
          "van_de": "Mất nhiều thời gian đặt lịch demo/tư vấn qua lại bằng email, tin nhắn",
          "tinh_nang_giai_quyet": "Tự động đặt lịch hẹn, đồng bộ với Google Calendar/Outlook"
        },
        {
          "van_de": "Thông tin lead và khách nằm rải rác, không đồng bộ vào CRM",
          "tinh_nang_giai_quyet": "Tích hợp CRM (HubSpot, Salesforce, v.v.) tự động tạo và cập nhật hồ sơ khách hàng"
        }
      ]
    }
  ],
  "tu_khoa_goi_y": [
    "AI chatbot doanh nghiệp",
    "tự động hóa chăm sóc khách hàng 24/7",
    "chatbot tích hợp CRM"
  ]
}
```

**PROMPT 2**

```text
[Role] Biên tập viên nội dung PR kiêm chuyên gia SEO.

[Request]: Yêu cầu cấu trúc:
- 1 Headline (≤ 70 ký tự, chứa từ khóa chính)
- Lead: nêu rõ pain point nổi bật nhất
- 4-5 mục H2, mỗi mục có 2-3 H3; mỗi pain point chính ứng với ít nhất 1 H2/H3
- CTA cuối bài
- Với mỗi mục: ghi ý chính (1-2 dòng), từ khóa SEO gắn vào, số từ dự kiến (tổng 1000-1500)

[Task]: Từ output ở PROMPT 1 hãy lập dàn ý chi tiết cho bài PR 1000-1500 từ.

[Explantion] Không viết nội dung bài. Giữ tone chuyên nghiệp, tin cậy.

[Tone]: Chuyên nghiệp, ngắn gọn.

[Extras]: Danh sách đánh số theo cấp (Headline > Lead > H2 > H3 > CTA).
```

**PROMPT 3**

```text
[Role] Biên tập viên nội dung PR kiêm chuyên gia SEO.

[Request]:
- Đủ: Headline, Lead giải quyết pain points, H2/H3 đúng dàn ý, CTA rõ ràng cuối bài (kèm hành động cụ thể: đăng ký demo/liên hệ).
- Từ khóa chính xuất hiện ở Headline, Lead, ít nhất 1 H2 và CTA; mật độ tự nhiên 1-2%, không nhồi nhét.
- Câu ngắn, đoạn ≤ 4 dòng, không lặp ý giữa các mục.
- Giữ nguyên tone chuyên nghiệp, tin cậy từ đầu đến cuối.
- Định dạng Markdown (#, ##, ###).

[Explantion] Không viết nội dung bài. Giữ tone chuyên nghiệp, tin cậy.

[Task]: Từ output ở PROMPT 2 hãy viết hoàn chỉnh bài PR theo đúng dàn ý, thứ tự từng mục.

[Tone]: Chuyên nghiệp, ngắn gọn.

[Extras]: Danh sách đánh số theo cấp (Headline > Lead > H2 > H3 > CTA).
```