# Cơ Chế Quản Lý Bộ Nhớ & Duy Trì Tính Nhất Quán Tuyệt Đối (Continuity & Memory Engine)

Khi sáng tác tiểu thuyết dài tập (từ vài chục nghìn đến hàng trăm nghìn chữ), AI thường gặp hiện tượng **"trôi ngữ cảnh" (Context Drift)**, quên các chi tiết nhỏ đã gieo từ đầu, làm sai lệch trạng thái nhân vật hoặc xưng hô lộn xộn.

Để khắc phục triệt để vấn đề này, toàn bộ quá trình sáng tác được vận hành dựa trên **Hệ Thống Trạng Thái Động 3 Tệp Tin (The Dynamic 3-File Memory Architecture)**.

---

## 1. Hệ Thống 3 Tệp Tin Quản Lý Bộ Nhớ (The 3 Core Memory Files)

Khi bắt đầu một dự án truyện trong thư mục làm việc, hãy tạo 3 tệp tin sau:

```
project_truyen/
├── story_bible.md       (Kinh Thánh Cốt Truyện - Cố định & Mở rộng dần)
├── character_state.md   (Bảng Trạng Thái Nhân Vật - Cập nhật liên tục sau mỗi chương)
└── plot_tracker.md      (Sổ Theo Dõi Tình Tiết & Phục Bút - Cập nhật sau mỗi chương)
```

---

## 2. Mẫu Khung Template Điền Sẵn Cho 3 Tệp Tin (Ready-to-Use Templates)

### 📂 Tệp 1: Mẫu `story_bible.md`
```markdown
# KINH THÁNH CỐT TRUYỆN (STORY BIBLE)

## 1. Thông Tin Cốt Lõi
- **Tên tác phẩm:** [Tên truyện]
- **Thể loại:** [Thể loại chính + phụ trong 30 thể loại hoặc Thể loại Lai ghép]
- **Tông giọng & Khí quyển:** [U tối / Hào sảng / Hài hước / Lãng mạn / Ly kỳ...]
- **Góc nhìn kể chuyện (POV):** [Ngôi thứ 1 / Ngôi thứ 3 giới hạn / Ngôi thứ 3 toàn tri]
- **Logline:** [Nhân vật] + [Biến cố] + [Mục tiêu] + [Trở ngại/Cái giá]

## 2. Bối Cảnh & Quy Luật Thế Giới (World-Building)
- **Không gian & Thời gian:** [Địa lý, thời đại, môi trường đặc thù]
- **Hệ thống sức mạnh / Phân tầng xã hội:** [Cấp bậc / Giai cấp / Tiền tệ / Công nghệ]
- **Quy tắc bất biến (Iron Laws):** [Những giới hạn tuyệt đối không thể vi phạm]

## 3. Quy Ước Văn Phong & Danh Xưng (Style & Naming Guide)
- **Quy ước xưng hô:**
  * Nhân vật A gọi B là: "Huynh / Đệ" hoặc "Cậu / Tớ" hoặc "Anh / Em"...
  * Tông giọng đối thoại của A: [Trầm ổn, sắc lạnh / Bồng bột, tinh nghịch...]
```

---

### 📂 Tệp 2: Mẫu `character_state.md`
```markdown
# BẢNG TRẠNG THÁI NHÂN VẬT (CHARACTER SNAPSHOTS)
*Cập nhật sau Chương: [Số chương mới nhất]*

## 1. Nhân Vật Chính: [Tên]
- **Cảnh giới / Năng lực / Cấp bậc hiện tại:** [Chỉ số / Cấp bậc]
- **Trang bị / Vật phẩm / Tài sản đang mang theo:**
  * Vật phẩm 1: [Tên & Tình trạng/Số lượng]
  * Vật phẩm 2: [Tên & Tình trạng/Số lượng]
- **Tình trạng sức khỏe & Vết thương:** [Khỏe mạnh / Bị thương / Mệt mỏi...]
- **Vị trí hiện tại:** [Địa danh / Tọa độ cụ thể]
- **Mối quan hệ & Tâm lý hiện tại:**
  * Với Nhân vật B: [Tin tưởng 80% / Vừa nảy sinh nghi ngờ...]
  * Mục tiêu trước mắt: [Chuẩn bị vào phó bản / Đang chờ đối chất...]

## 2. Các Nhân Vật Phụ / Phản Diện Liên Quan
- **[Tên Nhân Vật Phụ 1]:** [Trạng thái sức khỏe, vị trí, thái độ với nhân vật chính]
- **[Tên Nhân Vật Phụ 2]:** [Trạng thái sức khỏe, vị trí, thái độ với nhân vật chính]
```

---

### 📂 Tệp 3: Mẫu `plot_tracker.md`
```markdown
# SỔ THEO DÕI TÌNH TIẾT & PHỤC BÚT (PLOT TRACKER)

## 1. Dòng Thời Gian Đã Diễn Ra (Timeline Summary)
- **Chương 1:** [Tóm tắt 2-3 câu sự kiện chính đã xảy ra].
- **Chương 2:** [Tóm tắt 2-3 câu sự kiện chính đã xảy ra].
- **Chương [N]:** [Tóm tắt 2-3 câu sự kiện chính đã xảy ra].

## 2. Danh Sách Phục Bút Đang Mở (Open Loops / Active Foreshadowing)
- [ ] **[Mã PB-01]** *Chương 2:* Nhặt được chiếc nhẫn bạc có khắc chữ cổ (Chưa rõ lai lịch).
- [ ] **[Mã PB-02]** *Chương 4:* Phát hiện Thư ký Vương rời công ty lúc nửa đêm (Chưa rõ mục đích).

## 3. Danh Sách Phục Bút Đã Thu Lưới (Closed Loops)
- [x] **[Mã PB-00]** *Chương 1:* Mùi nước hoa lạ trên áo nạn nhân $\rightarrow$ *Thu lưới ở Chương 5:* Xác định thuộc về Thục phi.
```

---

## 3. Quy Trình Nạp Ngữ Cảnh Từng Chương (The Context Injection Cycle)

Mỗi khi chuẩn bị viết một chương mới (Chương $N$), thực hiện tuần tự 3 bước:

```
[1. Đọc Trạng Thái Hiện Tại] ───► [2. Chấp Bút Chương N] ───► [3. Hậu Kiểm & Cập Nhật]
- Đọc character_state.md         - Bám sát Style Guide         - Cập nhật vết thương/đồ đạc
- Đọc plot_tracker.md            - Show Don't Tell             - Ghi nhận phục bút mới
- Đọc tóm tắt chương N-1         - Cài cắm phục bút            - Tóm tắt 2 dòng nội dung
```

1. **Bước 1: Nạp Ngữ Cảnh Tức Thời:**
   * Tóm tắt 1-2 chương liền trước ($N-1, N-2$).
   * Trạng thái hiện tại từ `character_state.md`.
   * Danh sách mục tiêu và phân cảnh của Chương $N$.
2. **Bước 2: Chấp Bút (Drafting):**
   * Tuân thủ đúng giọng văn trong `story_bible.md`.
   * Kiểm tra tránh dùng nhầm bảo vật đã hỏng hoặc xưng hô sai quy ước.
3. **Bước 3: Hậu Kiểm & Cập Nhật (Post-flight Update):**
   * Sau khi hoàn tất chương, cập nhật ngay các biến động trạng thái vào `character_state.md` và `plot_tracker.md`.

---

## 4. Cơ Chế Quản Lý Truyện Đa Tuyến & Đa Góc Nhìn (Multi-POV Story Tracking)

Đối với các tác phẩm sử dụng nhiều góc nhìn nhân vật:
1. **Ghi rõ chủ thể POV ở đầu mỗi phân cảnh:** `### POV: [Tên Nhân Vật] - Địa điểm: [Tên Nơi Chốn]`.
2. **Nguyên tắc Giới Hạn Nhận Thức (Epistemic Boundary):** Nhân vật ở POV nào thì CHỈ ĐƯỢC BIẾT những gì mắt thấy, tai nghe và tâm trí họ suy luận. Tuyệt đối không để nhân vật biết trước các sự kiện xảy ra ở POV của nhân vật khác nếu chưa có người truyền tin.
3. **Bảng Theo Dõi Tuyến Song Song (Parallel Timeline Tracker):** Theo dõi dòng thời gian giữa các địa điểm khác nhau một cách logic, không để xảy ra mâu thuẫn thời gian di chuyển.
4. **Quy định góc nhìn Ngôi thứ hai ("Bạn" / "Ngươi"):** Khi dùng POV ngôi thứ 2 (đặc biệt trong Quy tắc quái đàm / Gamebook tương tác), giữ sự tập trung trực diện vào giác quan và hành động tức thời của đối tượng "Bạn", mọi manh mối sinh tồn phải gắn liền với môi trường trực tiếp xung quanh.
5. **Theo dõi dàn nhân vật phụ (Cast Economy Tracking):** Đảm bảo nhân vật phụ xuất hiện trong phân cảnh có chức năng rõ ràng (Gương phản chiếu, Kẻ châm ngòi, Điểm neo cảm xúc), tránh xuất hiện tràn lan gây loãng kịch bản.

---

## 5. Bảng Ánh Xạ Trạng Thái Cho 30 Thể Loại Truyện (Universal Genre Mapping)

| # | Thể Loại | Trọng Tâm Theo Dõi ở `character_state.md` | Trọng Tâm Theo Dõi ở `plot_tracker.md` |
| :--- | :--- | :--- | :--- |
| **1** | **Tiên Hiệp / Huyền Huyễn** | Cảnh giới, công pháp đang luyện, đan dược/linh thạch, thương tổn kinh mạch. | Bí cảnh chưa mở, tàn hồn sư phụ, ân oán tông môn. |
| **2** | **Khoa Huyễn / Cyberpunk** | Năng lượng pin/lõi, độ bền Cyberware, mã dữ liệu giải được, cấp độ truy nã. | Lỗ hổng bảo mật tập đoàn, tín hiệu lạ không gian. |
| **3** | **Đô Thị Dị Năng / Hệ Thống** | Cấp độ hệ thống, điểm tích lũy, cổ phần doanh nghiệp, quan hệ gia tộc ngầm. | Nhiệm vụ thời hạn đếm ngược, kẻ thù kiếp trước. |
| **4** | **Trinh Thám / Hình Sự** | Vật chứng thu giữ, khẩu cung mâu thuẫn, sơ đồ quan hệ nghi phạm. | Manh mối chưa giải mã, chứng cứ ngoại phạm chưa kiểm chứng. |
| **5** | **Ngôn Tình / Lãng Mạn** | Mức độ hảo cảm, bí mật quá khứ, hiểu lầm chưa giải tỏa, rào cản gia đình. | Lời hứa chưa thực hiện, tín vật tình cảm, cơ hội chạm mặt. |
| **6** | **Cung Đấu / Gia Đấu** | Phẩm cấp/địa vị, ân sủng bề trên, mạng lưới tai mắt nội gián, độc dược/vật cấm đang giấu. | Bẫy mưu kế đang giăng, thư mật chưa gửi, mối thù đời trước. |
| **7** | **Kinh Dị / Tâm Lý U Tối** | Chỉ số tinh thần (Sanity), nguồn sáng còn lại, vết thương hoảng loạn, vật phẩm xua tà. | Quy tắc cấm kỵ của địa điểm, hành tung của thực thể vô danh. |
| **8** | **Đời Thường / Chữa Lành** | Tâm trạng (vui/buồn/áp lực), tài chính sinh hoạt, tiến độ dự án/kỳ thi, quan hệ bạn bè. | Kế hoạch đi chơi/nấu ăn, món quà bất ngờ, tâm sự chưa giãi bày. |
| **9** | **Lịch Sử / Dã Sử** | Binh lực dưới quyền, sĩ khí quân đội, lương thảo còn lại, chức tước triều đình. | Bản đồ chiến sự, mật chỉ hoàng đế, mưu kế công thành. |
| **10** | **Võ Hiệp Truyền Thống** | Tầng võ học kiếm pháp, ám khí/độc dược, ân oán thù hằn giang hồ. | Bí kíp võ công thất lạc, danh tính sát thủ bịt mặt. |
| **11** | **Kỳ Ảo Phương Tây** | Mana/Phép thuật còn lại, độ bền thần khí, khế ước linh thú, ngôn ngữ cổ giải mã. | Di tích cổ đại chưa thám hiểm, phong ấn chúa tể bóng tối. |
| **12** | **Vô Hạn Lưu / Trò Chơi Sinh Tử** | Điểm tích lũy Không Gian, đạo cụ vượt ải đặc thù, bảng đánh giá (Rank S/A), trạng thái gen. | Quy tắc ẩn của phó bản hiện tại, manh mối về BOSS ngầm, âm mưu của công hội đối địch. |
| **13** | **Xuyên Nhanh / Cứu Vãn Pháo Hôi** | Mảnh vỡ linh hồn thu thập, điểm công đức, kỹ năng mang theo giữa các thế giới. | Chấp niệm chưa hóa giải của nguyên chủ, thân phận kiếp này của đối tượng công lược. |
| **14** | **Mạt Thế / Zombie** | Sức chứa không gian trữ đồ, cấp độ tinh hạch dị năng, lượng đạn dược/thuốc men, pin năng lượng. | Đợt thủy triều zombie kế tiếp, vị trí phòng thí nghiệm bí mật, kẻ nội gián trong căn cứ. |
| **15** | **Võng Du / Esports** | Cấp độ nhân vật game, trang bị hoàng kim/thần khí, bảng điểm elo/chỉ số APM, hợp đồng thi đấu. | Kỷ lục phó bản bị phá, chiến thuật khắc chế đối thủ trận sau, giải đấu mùa thu. |
| **16** | **Tây Huyễn Lãnh Chúa / Làm Ruộng** | Dân số lãnh địa, sản lượng lương thực/thép, quy mô quân đội ma kỹ, ngân khố. | Mưu đồ xâm chiếm của quý tộc láng giềng, tuyến đường thương mại bị phong tỏa. |
| **17** | **Đạo Mộ / Khảo Cổ Thần Bí** | Đèn cầy, móng lừa đen, la bàn phong thủy, mức độ ngộ độc khí chướng/thi độc. | Vị trí huyệt đạo chính điện, câu đối giải mã cơ quan bát quái, lai lịch chủ nhân cổ mộ. |
| **18** | **Đam Mỹ / Bách Hợp (BL/GL)** | Trạng thái pheromone (ABO), liên kết tinh thần (Sentinel/Guide), rào cản thân phận. | Hiểu lầm chưa tháo gỡ, khoảnh khắc rung động định mệnh, thử thách sinh tử kề vai. |
| **19** | **Kỳ Ảo Đô Thị Ẩn Bí** | Mức độ kiểm soát ma lực ngầm, danh tính che giấu dưới Bức Màn (Veil), huyết mạch thức tỉnh. | Phong ấn tà thần cổ đại bị nứt, tung tích thợ săn tà đạo, bí mật gia tộc người gác đêm. |
| **20** | **Phản Anh Hùng / Phản Diện** | Mạng lưới tay chân ngầm, con bài tẩy tống tiền/đe dọa, mức độ thao túng các phe phái. | Bẫy sát cục giăng sẵn cho phe chính nghĩa, điểm yếu chí mạng của đối thủ chưa khai thác. |
| **21** | **Tình Cảm Trưởng Thành / Adult Romance** | Ranh giới thỏa thuận thể xác, mức độ kiểm soát/phục tùng (Power dynamics), tổn thương tâm lý. | Khoảnh khắc phá vỡ rào cản lý trí, bí mật đời tư bị phơi bày, sự lựa chọn giữa dục vọng và tình cảm. |
| **22** | **Vòng Lặp Thời Gian / Đa Tuyến** | Số lần lặp (Reset Counter: Loop N), di chứng thể xác/tinh thần, biến số tích lũy (Delta tracker). | Quy luật bất biến của dòng thời gian, biến số mới kích hoạt, danh tính kẻ cùng tỉnh thức. |
| **23** | **Văn Học Tâm Lý Xã Hội / Trưởng Thành** | Trạng thái cảm xúc, áp lực tài chính/gia đình, sự thỏa hiệp đạo đức, ranh giới tổn thương. | Bí mật gia đình sắp vỡ lở, nút thắt ân oán thế hệ, cơ hội chuyển mình hay hòa giải. |
| **24** | **Cổ Đại Điền Văn / Nông Môn** | Tiền vốn tích lũy, số mẫu ruộng/xưởng sản xuất, công thức chế biến độc quyền, thái độ họ hàng/làng xóm. | Đơn hàng lớn sắp giao, đợt thuế má/mất mùa, cơ hội mở chi nhánh lên huyện thành. |
| **25** | **Tinh Tế Cơ Giáp / Đại Chiến Vũ Trụ** | Cấp bậc tinh thần lực, độ đồng bộ cơ giáp (Sync Rate), năng lượng động cơ hạt nhân, chức vụ quân đội. | Mật lệnh chiến dịch quân sự, tọa độ ổ Trùng tộc, bằng chứng phản bội của tướng lĩnh. |
| **26** | **Quy Tắc Quái Đàm / Dị Thường SCP** | Chỉ số tinh thần (Sanity), mức độ ô nhiễm nhận thức (0-100%), đạo cụ hóa giải quy tắc, vết cắn/dấu ấn quái dị. | Danh sách quy tắc chưa kiểm chứng (Thật/Giả), giờ giới nghiêm, điều kiện kích hoạt cửa thoát hiểm. |
| **27** | **Hài Bựa Sa Điêu / Cẩu Đạo / Vô Địch** | Mức độ cảnh giác/hoang tưởng, số lượng pháp bảo phòng ngự đang giấu, thực lực che giấu (giả vờ Luyện Khí/thực chất Đại Thừa). | Suy diễn hiểu lầm của môn phái/kẻ thù (Não bổ tracker), sự kiện rắc rối muốn né tránh nhưng bị cuốn vào. |
| **28** | **Đồng Nhân / Diễn Sinh / Fanfiction** | Mức độ lệch khỏi nguyên tác (Divergence Rate), hảo cảm của dàn nhân vật gốc (Canon Cast Affinity), tri thức tương lai đang giữ. | Mốc sự kiện canon sắp diễn ra cần can thiệp, biến số cánh bướm đã kích hoạt, danh tính kẻ xuyên không/biến số ngầm. |
| **29** | **Light Novel / Isekai / Học Viện** | Bảng chỉ số Status & Kỹ năng ẩn, mức độ gắn kết đồng đội/Heroine, thứ hạng học viện, cấp bậc linh thú đồng hành. | Sự kiện đại hội ma thuật sắp tới, dấu hiệu thâm nhập của Ma Vương giáo đoàn, công thức/vật phẩm độc lạ đang nghiên cứu. |
| **30** | **Linh Dị Dân Gian / Trừ Tà Bắt Ma** | Số lượng bùa chú/chu sa còn lại, thời hạn âm khí (giờ Tý/ngày rằm), mức độ nhiễm tà khí/lời nguyền trên cơ thể. | Manh mối vụ án oan khuất lịch sử, sơ đồ mắt trận phong thủy, thời điểm kẻ giấu mặt kích hoạt đại tế lễ. |

---

## 6. Checklist 7 Câu Hỏi Vàng Tự Kiểm Tra Tính Nhất Quán (Consistency Checklist)

Trước khi kết thúc một chương, luôn tự rà soát:
1. **Logic Động Cơ:** Hành động của nhân vật có xuất phát từ tính cách và hoàn cảnh đã thiết lập không?
2. **Logic Trạng Thái & Tài Sản:** Nhân vật có bị "quên vết thương" hoặc dùng nhầm vật phẩm không có trong túi đồ không?
3. **Logic Không Gian & Thời Gian:** Thời gian di chuyển giữa các địa điểm có bị nhảy cóc phi thực tế không?
4. **Logic Quan Hệ & Xưng Hô:** Cách xưng hô và mức độ thân mật giữa các nhân vật có giữ đúng quy ước không?
5. **Logic Giọng Văn & Khí Quyển:** Văn phong có duy trì đúng tông giọng của tác phẩm hay bị biến đổi bất thường?
6. **Logic Phục Bút:** Đã cập nhật đầy đủ các chi tiết phục bút mới vừa xuất hiện trong chương vào `plot_tracker.md` chưa?
7. **Logic Dàn Nhân Vật Phụ (Cast Economy Check):** Các nhân vật phụ xuất hiện trong chương có đảm nhận đúng vai trò chức năng (Gương phản chiếu, Châm ngòi, Điểm neo cảm xúc) hay đang làm loãng mạch truyện chính?
