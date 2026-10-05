# Three-option Design Sheet — October · Case B: AI Notes

> Worksheet thiết kế. A/B/C là ba giả thuyết giải pháp trên cùng một tình huống mẫu; chưa có người học thật xác nhận nhu cầu hoặc chọn phương án. Phần test được mô phỏng và ghi rõ ở [Group Feedback Synthesis](group-feedback-synthesis.md).

## 1. Problem và dấu vết Day 17

**Hypothesis Problem (giả thuyết, chưa được xác nhận):** Khi quay lại ôn sau một buổi học của chương trình A.I Thực Chiến mà mình đã tạo dấu vết để xem lại trong 7 ngày gần đây, **học viên A.I Thực Chiến** gặp khó khăn trong việc **tìm lại và ghép ngữ cảnh các dấu vết để ôn** vì **dấu vết có thể nằm ở nhiều nơi hoặc thiếu liên kết với nguồn**, dẫn đến **có thể tốn thêm thời gian, trì hoãn ôn, bỏ sót nội dung hoặc phải làm lại một bước**.

Đây là giả thuyết, không phải finding. Ghi chép lượt luyện Day 17 của Linh (trước khi tinh gọn repo: `interview/notes.md`, tóm tắt từ chép lời tự động) ghi P1 thường ghi giấy, có lúc chụp/lưu phần khó, đưa ngữ cảnh cho công cụ AI và tự đối chiếu vài khả năng; P1 mô tả việc đó tốn thêm thời gian. Interviewer đã nhắc Gemini trước. Không xác định được P1 có thuộc chương trình A.I Thực Chiến không, một buổi cụ thể, điều kiện 7 ngày, số phút hoặc hệ quả ôn tập; bản ghi không có lời trích nguyên văn đủ tin cậy. Do đó chưa thể xác nhận Gate 1 hoặc coi AI là lựa chọn ưu tiên.

**Bốn đầu vào Chặng 1 sau khi gom về sáu file:** Hypothesis ở đoạn trên; Practice Note 1 chỉ có tóm tắt lượt luyện Day 17 chưa đủ chi tiết, Practice Notes 2/3 là **hai tình huống giả lập riêng** trong [README](README.md) và không có nguồn phỏng vấn độc lập; Solution Parking Lot nằm ngay dưới; Conversation Guide cuối ở README cũ chỉ dùng làm context, với nguyên tắc hỏi sự việc gần đây, hành vi trước công cụ, hệ quả bằng câu hỏi mở và xin consent ghi âm rõ ràng. Day 18 không tiếp tục problem interview. Guide và phiếu trống cũ đã bỏ khỏi cây file theo format mới.

**Solution Parking Lot — năm hướng brainstorm chưa kiểm chứng:** (1) giữ nguồn cạnh note/highlight; (2) gom dấu vết do user chọn; (3) tự gắn nhãn theo buổi/chủ đề; (4) tìm lại theo nội dung, nguồn hoặc thời điểm; (5) hỗ trợ cấu trúc ghi chú, có thể cân nhắc AI như một hướng. Không hướng nào ở đây là nhu cầu hoặc lựa chọn user đã xác nhận.

## 2. Phần giữ nguyên để so sánh

| Thành phần | Giá trị dùng chung cho A/B/C |
|---|---|
| User | Học viên chương trình A.I Thực Chiến đã tạo dấu vết học tập trong 7 ngày gần đây. Đây là tiêu chí thiết kế, chưa được xác minh trong lượt Day 17. Tester thật, nếu có, ở trong chương trình nhưng ngoài nhóm October. |
| Situation | Sau buổi học của chương trình, quay lại một đoạn tài liệu đã đánh dấu để xử lý câu hỏi còn mở. Đây là scenario mẫu, không phải sự việc có thật đã quan sát. |
| Outcome task | “Trong tình huống này, hãy dùng từng phương án để tạo một ghi chú ôn tập từ dấu vết đã lưu, kèm nguồn để xem lại câu hỏi sau.” |
| Desired outcome | Ghi chú giữ nội dung, nguồn và trạng thái câu hỏi; user quyết định điều gì được lưu. |
| Fixture tổng hợp | A.I Thực Chiến · **buổi học mẫu giả lập** “Rà câu trả lời AI với tài liệu nguồn” · handout mục 2. Đoạn: “Khi dùng AI để tóm tắt một tài liệu học, hãy đối chiếu từng ý quan trọng với đoạn gốc. Nếu tài liệu chưa đủ căn cứ, giữ câu hỏi ở trạng thái chưa xác minh; không để AI tự bổ sung chi tiết ngoài nguồn. Chỉ lưu ghi chú sau khi người học đọc và sửa.” Câu hỏi: “Nếu AI thêm một ý không có trong tài liệu, bạn xử lý thế nào trước khi lưu ghi chú?” Đây là nội dung tạo để thử luồng, **không phải giáo trình chính thức hoặc dữ liệu người tham gia**. |

## 3. Ba solution options

| | A — Tự biên soạn | B — Gọi AI khi cần | C — AI gợi ý khi mở dấu vết |
|---|---|---|---|
| Cơ chế | User đọc nguồn, tự viết note hoặc để câu hỏi mở. | User chủ động yêu cầu AI tạo draft từ đoạn đã chọn, rồi rà và quyết định. | Mở dấu vết là trigger cho một gợi ý AI tùy chọn; user quyết định có dùng hay bỏ. |
| AI làm gì? | Không tham gia. | Soạn draft mẫu giới hạn ở đoạn, câu hỏi và vị trí nguồn; không tự lưu. | Chủ động đề xuất draft mẫu từ cùng đầu vào sau khi user mở dấu vết; không tự lưu. |
| User làm gì? | Viết/sửa, đánh dấu chưa rõ, lưu hoặc bỏ. | Xem giới hạn trước khi gọi, kiểm tra nguồn, sửa/lưu hoặc bỏ draft. | Nhận ra nguồn gốc gợi ý, kiểm tra/sửa/lưu hoặc bỏ ngay để tự làm. |
| Trade-off cần thử | Quyền tác giả cao; phải tự soạn. | Có điểm bắt đầu nhanh; thêm công kiểm tra. | Bớt thao tác gọi; có thể ngắt mạch đọc hoặc gây bất ngờ. |

**Distance check:** A khác B ở người tạo nội dung; B khác C ở trigger và quyền khởi xướng; A khác C ở cả việc có AI lẫn trigger. Ba phương án khác cơ chế và phân công user–AI, không chỉ khác bố cục. C được thêm ở Chặng 4; bảng này là bản hợp nhất để nộp, không viết lại lịch sử như thể C đã được chốt ở Chặng 2.

## 4. Human–AI design pass

| Quyết định | A | B | C |
|---|---|---|---|
| Expectation trước hành động | Biết đây là note tự viết và nguồn luôn cạnh note. | Trước khi gọi draft, thấy AI chỉ dùng đoạn/câu hỏi/nguồn đang mở và không tự xác minh. | Khi mở dấu vết, gợi ý tự hiện; trên gợi ý phải giải thích ngay trigger và đây là nội dung AI. Đây là điểm cần kiểm tra hiểu nhầm. |
| Agency: Act/Ask/Don’t Act | AI không hành động. | AI chỉ Act sau yêu cầu rõ; Ask nếu nguồn chưa rõ; Don’t Act khi user hủy hoặc nguồn không đủ. | AI Act ở mức **gợi ý chưa lưu** sau khi user mở dấu vết; không âm thầm lưu, không tự kết luận câu hỏi đã giải quyết. User có thể bỏ ngay. |
| Evidence và uncertainty | Đoạn gốc/vị trí nguồn cạnh note; trạng thái “còn vướng” do user chọn. | Draft dán nhãn AI/chưa xác minh, có đoạn nguồn; phần chưa được hỗ trợ phải để mở. | Cùng giới hạn nguồn như B; phải hiển thị rõ vì sao gợi ý xuất hiện và không dùng nguồn ngoài. |
| Recovery | Sửa/bỏ note, quay lại nguồn hoặc để câu hỏi mở; lưu có chủ ý. | Dừng, sửa, bỏ draft, quay lại nguồn/tự viết/để mở; không tự lưu. | Bỏ qua gợi ý ở ngay đầu thẻ, tự viết hoặc để mở; có đường quay lại nguồn. |
| Feedback/data | Không có AI. Mock không dùng dữ liệu người học thật. | Draft soạn sẵn; không gọi model, không học từ feedback. | Draft soạn sẵn; không theo dõi ngoài scenario, không học từ feedback. |

<a id="stage4"></a>
## 5. Chặng 4 — Build ba micro-prototype

### 5.1 Scope chuẩn và phần dùng chung

```text
COMMON CONTEXT (dấu vết + task + nguồn)
       ↓
CRITICAL INTERACTION (A tự viết / B gọi draft / C nhận gợi ý)
       ↓
RESULT / USER DECISION (lưu, để mở, bỏ hoặc quay lại nguồn)
```

Đây là **ba màn hình/trạng thái chính** của mỗi option; các đường sửa, bỏ và Đặt lại trong [prototype](prototype-link.md) là nhánh phục hồi từ trạng thái chính, không phải một task mới. Phần dùng chung theo scope khoảng 70% là context của học viên A.I Thực Chiến, cùng handout mẫu mục 2, câu hỏi, outcome task và cách trình bày bằng Markdown. Chỉ critical interaction khác: người tự viết ở A, chủ động gọi draft ở B, hoặc nhận gợi ý khi mở dấu vết ở C. Tỷ lệ 70% là mục tiêu thiết kế, không có phép đo pixel hay thành phần giao diện.

| Option | Common context | Critical interaction | Result / user decision |
|---|---|---|---|
| A | [Bắt đầu](prototype-link.md#start) → [A0](prototype-link.md#a0) | [A1 nguồn](prototype-link.md#a1) → [A2 tự viết](prototype-link.md#a2) | [Lưu](prototype-link.md#a-save), [để mở](prototype-link.md#a-open), bỏ/quay lại nguồn hoặc Đặt lại. |
| B | [Bắt đầu](prototype-link.md#start) → [B0](prototype-link.md#b0) | [B1 xin draft](prototype-link.md#b1) → [B2 rà draft](prototype-link.md#b2) | [Lưu](prototype-link.md#b-save), [để mở](prototype-link.md#b-open), bỏ/tự viết hoặc Đặt lại. |
| C | [Bắt đầu](prototype-link.md#start) → [C0](prototype-link.md#c0) | [C1 gợi ý tự hiện](prototype-link.md#c1) | [Lưu](prototype-link.md#c-save), [để mở](prototype-link.md#c-open), bỏ/tự viết hoặc Đặt lại. |

Prototype giấy số hóa dùng **canned AI output**, không cần model/API, onboarding, dashboard, responsive nhiều thiết bị hoặc visual polish hoàn chỉnh. Cùng một bản nháp mẫu được dùng cho B/C để so sánh trigger; nội dung user muốn sửa phải được nói thành lời vì Markdown không có ô nhập hay lưu trạng thái. Không có người đóng vai AI phải giải thích giao diện hộ tester.

### 5.2 Definition of testable và trạng thái thực tế

| Điều kiện | Trạng thái có thể kiểm từ repo |
|---|---|
| Tester tự mở và thao tác A/B/C | Có liên kết tự đi trong [prototype](prototype-link.md), nhưng chưa có quan sát học viên A.I Thực Chiến ngoài nhóm October tự dùng. |
| Cùng context, task và fixture | Có chung màn Bắt đầu, cùng đoạn, câu hỏi và nguồn; chỉ cơ chế tạo note khác. |
| Không cần facilitator narrate | Luồng có nhãn và đường đi; **chưa được học viên trong chương trình ngoài nhóm October xác minh**. |
| Nội dung đủ để ra quyết định | Có đoạn nguồn, câu hỏi, draft mẫu và các lựa chọn; chưa biết người thử thật có thấy đủ hay không. |
| Recovery và reset | A/B/C có đường sửa/bỏ/để mở; mỗi nhánh có **Đặt lại** về common context. Markdown không xóa trạng thái vì không lưu trạng thái. |

### 5.3 Build order 80 phút — mốc làm việc của lab

| Phút | Việc cần có | Dấu vết trong repo |
|---|---|---|
| 0–10 | Vẽ common context, task, content fixture. | Mục 2 và màn [Bắt đầu](prototype-link.md#start). |
| 10–55 | Chia nhau build A/B/C bằng shared components. | Ba luồng trong cùng prototype; **chưa có log phân công hoặc thời gian thực tế** của Linh và Châm Anh. |
| 55–65 | Thêm control/recovery và evidence/uncertainty. | Mục 4 và các nhánh sửa, bỏ, để mở, nguồn. |
| 65–75 | Mỗi thành viên tự thử option người khác build. | **Chưa có ghi chép cross-check của hai thành viên.** Không ghi là đã diễn ra. |
| 75–80 | Chuẩn hóa A/B/C, kiểm link và reset. | Cùng fixture/task; liên kết và anchor được rà trong repo. Việc học viên ngoài nhóm October tự hiểu vẫn chưa xác minh. |

### 5.4 Prototype annotation — chỉ cho nhóm, ngoài màn tester

Các annotation này ở Design Sheet; **không đặt trong [màn prototype cho tester](prototype-link.md#start)** và không đọc trước khi tester thao tác.

| Option | We expect the tester to | Watch for | Do not explain |
|---|---|---|---|
| A | Mở dấu vết, tự nêu ghi chú hoặc để câu hỏi mở, giữ nguồn rồi lưu/bỏ. | Họ có biết viết gì, có nhận ra câu hỏi có thể để mở và tìm lại nguồn không. | Câu trả lời mẫu, nội dung cần viết, nút nên chọn. |
| B | Đọc giới hạn, chủ động yêu cầu draft, đối chiếu nguồn rồi sửa/lưu/bỏ. | Họ có hiểu draft chưa xác minh, đọc nguồn, thấy đường dừng/bỏ và tự tiếp tục không. | Đáp án, chỗ cần đối chiếu, rằng AI chắc chắn tiết kiệm thời gian. |
| C | Mở dấu vết, nhận ra gợi ý tự xuất hiện và tùy chọn; quyết định đọc/sửa/lưu/bỏ. | Bất ngờ, nhầm tác giả hoặc trigger, bỏ qua có dễ thấy không, có tự quay lại nguồn không. | Trigger trước khi họ mở dấu vết, vị trí đường bỏ qua hay phản ứng “đúng”. |

**Gate 4 — Chưa thể xác nhận đạt theo tiêu chí tester thật.** Liên kết và các nhánh của mock có thể được tự đi, nhưng chưa có một **học viên A.I Thực Chiến không thuộc nhóm October và không tham gia build** mở, làm cùng task qua A/B/C rồi trở về common context mà không cần giải thích. Ba tình huống T1/T2/T3 là mô phỏng nên chỉ hoàn tất bài tập diễn tập, không thay lượt kiểm tra này. Không test ngoài chương trình.

## 6. Điều cần quan sát trong test

**Relevant context — hỏi tối đa 2 phút trước test:** “Trong 7 ngày gần đây, bạn có từng ghi chú, đánh dấu hoặc lưu một đoạn từ buổi học A.I Thực Chiến để xem lại sau không?” Chỉ mời học viên trong chương trình không thuộc nhóm October; nếu họ trả lời không, vẫn có thể xem interaction breakdown nhưng không đưa ra value claim từ lượt đó.

Giữ cùng task và fixture; tập trung tối đa năm loại ghi nhận: (1) nguồn được đọc hay bỏ qua, (2) hiểu nhầm tác giả/trigger/trạng thái câu hỏi, (3) lúc cần trợ giúp, (4) sửa hoặc lấy lại quyền kiểm soát, (5) option được chọn kèm trade-off. Không hỏi “Bạn có thích không?”. Khi tester hỏi cách hoạt động, chỉ hỏi “Theo bạn, nó nên hoạt động như thế nào?”.

**Trạng thái:** Ba option có thiết kế và [prototype Markdown để thử luồng](prototype-link.md). Các phản hồi T1/T2/T3 là kịch bản giả lập về học viên A.I Thực Chiến, không phải ba tester độc lập trong chương trình. Gate 2/3 có căn cứ thiết kế; Gate 1/4/5 theo tiêu chí test thật vẫn chưa thể xác nhận.
