# 📖 HƯỚNG DẪN SỬ DỤNG BỘ KỸ NĂNG SÁNG TÁC TIỂU THUYẾT TOÀN DIỆN
### *(Universal Novel Writing Skill Guide)*

> **Phiên bản:** 2.0 (Toàn năng - Phổ quát - Chuyên nghiệp)  
> **Áp dụng cho:** Tất cả 30+ dòng thể loại (Tiên hiệp, Huyền huyễn, Khoa huyễn, Ngôn tình, Trinh thám, Kinh dị, Điền văn, Vô hạn lưu, Đồng nhân, Hiện thực tâm lý...) và các tác phẩm **Lai ghép Đa tầng (Hybrid Genres)**.

---

## 🌟 1. TỔNG QUAN VỀ BỘ KỸ NĂNG

`novel-writing-skill` là hệ thống kỹ năng sáng tác truyện chữ chuyên nghiệp được thiết kế để biến AI thành một **Trợ Lý / Bạn Đồng Tác Giả (Co-Author)** chuẩn mực. Bộ kỹ năng giải quyết triệt để các nhược điểm cố hữu của AI khi viết văn:
- ❌ *Không còn* văn phong sáo rỗng, triết lý dạy đời, "văn mẫu AI".
- ❌ *Không còn* hiện tượng "trôi ngữ cảnh" (quên phục bút, lộn xộn trang bị/cảnh giới, sai xưng hô) khi viết truyện dài tập.
- ❌ *Không còn* tình trạng lướt nhanh tình tiết, kết thúc chương vội vã, "nói thay vì tả" (*Telling instead of Showing*).

---

## 📂 2. CẤU TRÚC THƯ MỤC CỦA BỘ KỸ NĂNG

```
novel-writing-skill/
├── SKILL.md                                 # [Trọng tâm] Quy trình Kim tự tháp 4 cấp bậc, 4 chế độ & 8 kỹ thuật viết
├── README.md                                # [Hướng dẫn] Tài liệu tổng quan & hướng dẫn thực hành nhanh (tệp này)
└── resources/
    ├── story_templates.md                   # 30 Khung mẫu cấu trúc truyện chuyên biệt cho từng thể loại
    ├── crafting_guide.md                    # Cẩm nang 20 kỹ thuật sáng tác nâng cao & Bộ thanh lọc văn mẫu AI Detox 2.0
    └── continuity_and_memory_guide.md       # Cơ chế quản lý bộ nhớ 3 tệp tin chống trôi ngữ cảnh & Templates
```

---

## 🎮 3. BỐN CHẾ ĐỘ TÁC NGHIỆP (OPERATIONAL MODES) & MẪU CÂU LỆNH (PROMPTS)

Tùy thuộc vào giai đoạn sáng tác của bạn, hãy chọn 1 trong 4 chế độ dưới đây:

```
                      ┌────────────────────────────────────────┐
                      │      CHỌN CHẾ ĐỘ TÁC NGHIỆP           │
                      └──────────────────┬─────────────────────┘
                                         │
       ┌──────────────────┬──────────────┴─────┬──────────────────┐
       ▼                  ▼                    ▼                  ▼
┌──────────────┐   ┌──────────────┐     ┌──────────────┐   ┌──────────────┐
│  CHẾ ĐỘ 1    │   │  CHẾ ĐỘ 2    │     │  CHẾ ĐỘ 3    │   │  CHẾ ĐỘ 4    │
│  Khởi Tạo    │   │  Chấp Bút    │     │  Biên Tập &  │   │  Bắt Bệnh &  │
│  Từ Đầu      │   │  Từng Chương │     │  Nâng Tầm    │   │  Gỡ Bí Plot  │
└──────────────┘   └──────────────┘     └──────────────┘   └──────────────┘
```

---

### 🟢 CHẾ ĐỘ 1: KHỞI TẠO TỪ ĐẦU (FROM-SCRATCH MODE)
* **Dành cho:** Bạn có ý tưởng sơ khai, muốn xây dựng một bộ truyện mới hoàn chỉnh từ cốt truyện, nhân vật đến thế giới.
* **Quy trình AI thực hiện:**
  1. Giúp bạn đúc kết **Logline** chuẩn và xác định thể loại chính/phụ (hoặc công thức lai ghép thể loại 3 tầng).
  2. Xây dựng **Hồ sơ nhân vật 3 chiều (3D Character Bible)**: Khát vọng bề mặt (Want), Nhu cầu thực sự (Need), Vết thương quá khứ (Ghost/Wound), Điểm yếu (Flaws).
  3. Thiết lập **Bối cảnh & Thế giới (World-Building)**: Hệ thống sức mạnh, bản đồ, quy tắc bất biến.
  4. Lựa chọn **Khung cấu trúc Macro Arc** phù hợp trong số 12 mô hình cấu trúc.
  5. Khởi tạo bộ **3 Tệp Bộ Nhớ**.

> **💡 Mẫu Câu Lệnh (Prompt Template):**
> ```text
> [CHẾ ĐỘ 1: KHỞI TẠO TỪ ĐẦU]
> Tôi muốn viết một bộ truyện:
> - Thể loại: [Ví dụ: Tiên hiệp lai Cyberpunk / Ngôn tình cưới trước yêu sau / Trinh thám điều tra dị thường]
> - Ý tưởng ban đầu: [Mô tả 1-3 câu về ý tưởng cốt lõi của bạn]
> - Tông giọng mong muốn: [Ví dụ: U tối ly kỳ / Hài hước bựa / Trầm lắng chữa lành]
> - Quy mô: [Ví dụ: Truyện ngắn 10.000 chữ / Sách đơn 50.000 chữ / Trường thiên 500 chương]
> 
> Hãy cùng tôi hoàn thiện Premise Sheet, Character Bible và đề xuất Khung Hồi (Macro Arc) cho tác phẩm này.
> ```

---

### 🔵 CHẾ ĐỘ 2: CHẤP BÚT TRỰC TIẾP (DIRECT DRAFTING MODE)
* **Dành cho:** Đã có dàn ý/bối cảnh sẵn, muốn AI chấp bút trực tiếp Chương X sống động, chuẩn văn học, độ dài 2.000 – 4.000 chữ.
* **Quy trình AI thực hiện:**
  1. Phân rã chương thành **3 – 4 Phân cảnh (Beats)** theo mô hình *Scene & Sequel*.
  2. Xác định **Hook mở đầu** và **Micro-Cliffhanger cuối chương**.
  3. Áp dụng 8 Kỹ thuật viết văn (Deep POV, Show Don't Tell, Đa giác quan, Đối thoại ngầm Subtext).
  4. Hỗ trợ 2 phương thức:
     * **Phương thức A (Liền mạch):** Viết đủ 3-4 beats với dung lượng phân bổ đều (~600-900 chữ/beat).
     * **Phương thức B (Beat-by-Beat):** Viết sâu từng Beat $\rightarrow$ Bạn duyệt/chỉnh sửa $\rightarrow$ Viết tiếp Beat sau (khuyên dùng cho cảnh cao trào).

> **💡 Mẫu Câu Lệnh (Prompt Template):**
> ```text
> [CHẾ ĐỘ 2: CHẤP BÚT CHƯƠNG]
> Hãy viết Chương [Số chương]: [Tên chương nếu có]
> - Bối cảnh & Điểm rơi: [Ví dụ: Nối tiếp chương trước, nhân vật A đang bị bao vây tại Hắc Phong Cốc]
> - Mục tiêu chương: [Ví dụ: A tìm cách kích hoạt trận pháp trốn thoát, phát hiện bí mật về kẻ phản bội]
> - Tông cảm xúc: [Ví dụ: Căng thẳng nghẹt thở, nhịp câu dồn dập]
> - Phương thức chấp bút: [Phương thức A - Toàn chương LIỀN MẠCH / Phương thức B - Từng Beat]
> 
> Yêu cầu: Áp dụng Deep POV, Show Don't Tell, miêu tả tối thiểu 3 giác quan, đối thoại có Subtext, không dùng văn mẫu sáo rỗng.
> ```

---

### 🟡 CHẾ ĐỘ 3: BIÊN TẬP & NÂNG TẦM VĂN PHONG (POLISHING & REWRITING)
* **Dành cho:** Bạn đã có đoạn văn thô / chương truyện tự viết hoặc bản dịch thô, muốn AI trau chuốt, nâng cấp chiều sâu nghệ thuật.
* **Quy trình AI thực hiện:**
  1. **Khử văn mẫu AI (Detox 2.0):** Loại bỏ cụm từ sáo rỗng (*"như một minh chứng cho..."*, *"không khí ngột ngạt đến mức có thể cắt ra được..."*), khử cấu trúc bị động ngoại lai (*"được/bị"* gượng ép).
  2. **Chuyển đổi Tell sang Show:** Thay thế tính từ cảm xúc chung chung bằng phản ứng cơ thể, cử chỉ vi mô, âm thanh và xúc giác.
  3. **Đan cài Subtext:** Tăng độ sắc sảo cho đối thoại.
  4. **Tối ưu nhịp câu (Sentence Flow):** Điều phối câu ngắn dồn dập và câu phức giàu hình ảnh.

> **💡 Mẫu Câu Lệnh (Prompt Template):**
> ```text
> [CHẾ ĐỘ 3: BIÊN TẬP & NÂNG TẦM]
> Dưới đây là đoạn văn thô của tôi:
> """
> [Dán đoạn văn cần biên tập vào đây]
> """
> 
> Yêu cầu biên tập:
> 1. Thanh lọc toàn bộ văn mẫu sáo rỗng và cấu trúc dịch thuật bị động.
> 2. Chuyển toàn bộ các đoạn "kể lể cảm xúc" (Tell) sang "miêu tả hành động & giác quan" (Show).
> 3. Nâng cấp góc nhìn Deep POV và tăng cường Subtext cho lời thoại.
> 4. Giữ nguyên diễn biến tình tiết và dụng ý nghệ thuật của tôi.
> ```

---

### 🔴 CHẾ ĐỘ 4: BẮT BỆNH CỐT TRUYỆN & GỠ BÍ (PLOT DOCTORING MODE)
* **Dành cho:** Bị tắc ý tưởng (Writer's Block), cốt truyện xuất hiện lỗ hổng logic (Plot Hole), hoặc cần một **Plot Twist** đỉnh cao.
* **Quy tắc 3 Nhánh Biến Hóa (The 3-Branch Rule):** AI bắt buộc đề xuất **3 phương án** khác nhau để bạn lựa chọn:
  * **Nhánh A (Thỏa Mãn Kỳ Vọng / Canonical & Sảng Điểm):** Hướng đi thuận tự nhiên, đem lại cảm giác thỏa mãn, đền đáp kỳ vọng người đọc.
  * **Nhánh B (Lật Kèo Bất Ngờ / Subversive Twist):** Đảo ngược giả định, đổi góc nhìn, cú lừa ngoạn mục nhưng vẫn tôn trọng logic phục bút.
  * **Nhánh C (Chiều Sâu Bi Kịch & Triết Lý / Emotional Depth):** Đặt nhân vật vào thế tiến thoái lưỡng nan về đạo đức, đào sâu vào vết thương tâm lý và bài học nhân sinh.

> **💡 Mẫu Câu Lệnh (Prompt Template):**
> ```text
> [CHẾ ĐỘ 4: BẮT BỆNH CỐT TRUYỆN]
> Tôi đang gặp vấn đề ở đoạn này:
> - Tình thế hiện tại: [Mô tả tình huống nhân vật đang đối mặt]
> - Điểm nghẽn / Lỗ hổng: [Ví dụ: Kẻ phản diện quá mạnh, nhân vật chính không có cách thoát thân hợp lý / Chưa tìm được động cơ giết người đủ thuyết phục]
> - Mục tiêu mong muốn: [Ví dụ: Cần một Plot Twist lật ngược tình thế hoặc một giải pháp logic không dùng Deus ex Machina]
> 
> Hãy phân tích nguyên nhân và đề xuất cho tôi 3 Hướng Biến Hóa (Nhánh A, Nhánh B, Nhánh C) theo đúng Quy tắc đồng sáng tác.
> ```

---

## 🧠 4. HỆ THỐNG QUẢN LÝ BỘ NHỚ 3 TỆP TIN (CHỐNG TRÔI NGỮ CẢNH)

Khi sáng tác truyện dài tập, hãy tạo 3 tệp tin `.md` trong thư mục dự án của bạn:

```
📁 thu_muc_truyen_cua_ban/
├── 📄 story_bible.md         # Kinh Thánh Cốt Truyện (Bối cảnh, hệ thống sức mạnh, quy ước xưng hô)
├── 📄 character_state.md     # Bảng Trạng Thái Nhân Vật (Cập nhật thương thế, cấp bậc, trang bị, vị trí)
├── 📄 plot_tracker.md        # Sổ Theo Dõi Tình Tiết (Phục bút đã gieo/đã thu, tiến độ Arc, móc câu)
└── 📁 chapters/
    ├── chuong_001.md
    ├── chuong_002.md
    └── ...
```

### Cách phối hợp cùng AI:
1. **Trước khi viết chương mới:** AI tự động đọc 3 tệp tin này để nắm chắc tình trạng mới nhất.
2. **Sau khi viết xong chương:** Yêu cầu AI cập nhật các thay đổi vào `character_state.md` và `plot_tracker.md` (hoặc AI sẽ chủ động xuất khối cập nhật để bạn lưu lại).

*(Chi tiết định dạng và mẫu điền sẵn xem tại `resources/continuity_and_memory_guide.md`)*.

---

## 💎 5. BỘ 8 KỸ THUẬT VIẾT VĂN BẬC THẦY CỐT LÕI

| STT | Kỹ Thuật | Ý Nghĩa Thực Chiến | Ví Dụ Chuyển Đổi |
| :---: | :--- | :--- | :--- |
| **1** | **Show, Don't Tell** | Diễn tả cảm xúc bằng phản xạ sinh học, hành động cụ thể thay vì nêu tên cảm xúc. | ❌ *Hắn rất sợ hãi.*<br>✅ *Gáy hắn lạnh toát. Mồ hôi rịn ra trơn trượt trên then cửa gỗ mục.* |
| **2** | **Đa Giác Quan** | Đan cài tối thiểu 3/5 giác quan (thị, thính, khứu/vị, xúc, nội cảm). | Tả cảnh chiến đấu có mùi khét lưu huỳnh, tiếng xương rạn, vị máu tanh nồng. |
| **3** | **Subtext Đối Thoại** | Nhân vật không nói thẳng ý nghĩ; dùng lời nói để che giấu, thăm dò, công kích ngầm. | Hoàng hậu mời trà sen kèm câu nhắc khéo về vụ sẩy thai của phi tần đối thủ. |
| **4** | **Deep POV** | Xóa bỏ từ lọc trung gian (*"hắn thấy", "cô cảm thấy"*), nhập thẳng vào dòng tâm tư. | ❌ *Hắn thấy bóng đêm đang ập xuống.*<br>✅ *Bóng đêm nuốt chửng những rặng phi lao.* |
| **5** | **Nhịp Điệu Câu** | Câu ngắn dồn dập cho cảnh sinh tử; câu phức êm đềm cho cảnh hồi ức/lắng đọng. | Tạo hiệu ứng tăng tốc và giảm tốc nhịp tim của độc giả. |
| **6** | **Phong Vị Văn Hóa** | Từ vựng chuẩn mực theo thời đại & không gian. | Chuẩn Hán Việt cho Tiên hiệp; chuẩn Âu Mỹ cho Tây huyễn; khẩu ngữ tự nhiên cho Đô thị Việt Nam. |
| **7** | **Điều Tiết Sảng Điểm** | Cân bằng giữa dồn nén (ức chế) và giải tỏa (vả mặt/đột phá/thành công). | Đảm bảo phần thưởng xứng đáng với công sức nhân vật bỏ ra (Cathartic Payoff). |
| **8** | **Thuần Việt Tự Nhiên** | Khử cấu trúc dịch máy lủng củng, không lạm dụng *"bị/được"*, liên từ thừa. | Văn phong trôi chảy, giàu nhạc tính và mang hơi thở tiếng Việt hiện đại. |

---

## 📚 6. DANH MỤC TÀI LIỆU TRA CỨU CHUYÊN SÂU (IN RESOURCES)

Khi cần tra cứu chuyên sâu cho từng tình huống, bạn có thể tham khảo trực tiếp 3 tài liệu trong thư mục `resources/`:

### 📕 `resources/story_templates.md` (30 Khung Mẫu Thể Loại)
* **Tiên hiệp / Huyền huyễn / Tu chân:** Cấu trúc thăng tiến & mở rộng bản đồ.
* **Khoa huyễn / Cyberpunk / Viễn tưởng:** Cấu trúc 7 điểm căng thẳng Dan Wells.
* **Đô thị dị năng / Trọng sinh hệ thống:** Chu kỳ khen thưởng Dopamine Loop.
* **Trinh thám / Suy luận phá án:** Cấu trúc Khởi - Thừa - Chuyển - Hợp (Kishōtenketsu).
* **Ngôn tình / Lãng mạn:** Cấu trúc 4 nhịp đập Romancing the Beat.
* **Kinh dị tâm linh / Quy tắc quái đàm:** Chu kỳ xâm thực & giải mã dị thường SCP.
* **Cổ đại nông môn / Tây huyễn điền văn:** Chu kỳ kiến thiết sản nghiệp & làm giàu.
* **Sa điêu / Cẩu đạo / Vô địch lưu:** Cấu trúc trào phúng & phản bội kỳ vọng.
* *...và 22 thể loại kinh điển khác.*

### 📗 `resources/crafting_guide.md` (20 Kỹ Thuật Sáng Tác Nâng Cao)
* Kỹ thuật gieo Phục bút & Thu lưới (Foreshadowing & Payoff).
* Kỹ thuật Đấu trí quyền mưu & Lời thoại ngầm 3 tầng.
* Kỹ thuật xây dựng Bầu không khí ám ảnh & Rùng rợn (Atmosphere & Dread).
* Kỹ thuật biên đạo Cảnh giao đấu & Hành động đa giác quan.
* Bộ quy tắc Khử văn mẫu AI Detox 2.0 (Bảng từ cấm & cấu trúc cấm).
* Kỹ thuật viết Cảnh thân mật trưởng thành & Căng thẳng tình dục (Mature Romance / Steam).
* Kỹ thuật kiểm soát lạm phát sức mạnh (Power Creep Management).
* Kỹ thuật viết Hồi tưởng phi tuyến tính (Non-linear Flashbacks & In Medias Res).
* ...

### 📘 `resources/continuity_and_memory_guide.md` (Hệ Thống Quản Lý Bộ Nhớ)
* Chi tiết cấu trúc 3 tệp tin `story_bible.md`, `character_state.md`, `plot_tracker.md`.
* Cơ chế cập nhật vi mô (Micro-Update) sau mỗi chương.
* Chiến lược xử lý truyện siêu dài trên 100 chương (Rolling Summary & Archive).

---

## ⚡ 7. QUY TRÌNH THỰC HÀNH MẪU TỪ ĐẦU ĐẾN CUỐI (QUICK START)

Dưới đây là kịch bản 4 bước để bạn bắt đầu ngay một buổi viết truyện hiệu quả:

```
[Bước 1: Khởi Tạo]
👤 Bạn: "[CHẾ ĐỘ 1] Tôi muốn viết truyện Trinh thám tâm lý lấy bối cảnh Đà Lạt mù sương, nhân vật chính là một họa sĩ có khả năng nhìn thấy ký ức của đồ vật qua xúc giác..."
🤖 AI: Tiếp nhận ➔ Lập Logline ➔ Lập Character Bible ➔ Chọn cấu trúc Kishōtenketsu ➔ Đề xuất dàn ý 3 Hồi & Tạo 3 file bộ nhớ.

[Bước 2: Chuẩn Bị Dàn Ý Chương]
👤 Bạn: "Hãy lập dàn ý chi tiết cho Chương 1: Bức họa không gương mặt."
🤖 AI: Phân rã 4 Beats (Hook mở đầu ➔ Va chạm vụ án ➔ Xung đột nội tâm ➔ Micro-Cliffhanger).

[Bước 3: Chấp Bút Sâu]
👤 Bạn: "[CHẾ ĐỘ 2] Tiến hành viết toàn văn Chương 1 theo Phương thức A."
🤖 AI: Chấp bút 2.500 - 3.000 chữ với Deep POV, tả sương mù và mùi sơn dầu đa giác quan, đối thoại sắc sảo, không văn mẫu sáo rỗng.

[Bước 4: Cập Nhật & Tiến Bước]
🤖 AI: Xuất bảng trạng thái mới (Vết thương, vật phẩm nhặt được, phục bút vừa gieo).
👤 Bạn: Lưu vào character_state.md và plot_tracker.md ➔ Sẵn sàng viết Chương 2!
```

---

## 🛡️ NGUYÊN TẮC BẤT BIẾN (CO-AUTHOR GUARDRAIL)

1. **Quyền quyết định tối thượng thuộc về bạn (Tác giả):** AI là người trợ lực và mở rộng ý tưởng, không bao giờ tự ý giết nhân vật hay thay đổi định hướng nếu bạn chưa duyệt.
2. **Luôn có 3 Nhánh Lựa Chọn:** Khi bí ý tưởng, AI luôn cung cấp Nhánh A (Thỏa mãn), Nhánh B (Lật kèo), Nhánh C (Chiều sâu tâm lý) để bạn toàn quyền điều khiển cốt truyện.

---
*Chúc bạn có những tác phẩm thăng hoa cùng bộ kỹ năng `novel-writing-skill`!*
