# 重積性癲癇時間軸

依 **American Epilepsy Society（AES）2016** 與 **Neurocritical Care Society（NCS）2012** 指引製作的互動工具：以 0–5 / 5–20 / 20–40 / >40 分鐘時間軸引導處置，依體重自動計算 benzodiazepine、第二線抗癲癇藥與麻醉劑輸注劑量，並記錄每次給藥時間。

線上版：https://yht5582-source.github.io/status-epilepticus/

> ⚠️ **僅供急救流程輔助與教學，不取代臨床判斷。** 藥物劑量、濃度與輸注速率請依院內處方集並經藥師確認；兒童、孕婦、肝腎功能不全者需另行調整。

## 功能

| 時間 | 階段 | 內容 |
|---|---|---|
| 0–5 分 | 穩定期 | ABC 與給氧、監測、指尖血糖（<60 mg/dL：thiamine 100 mg → D50W 50 mL）、靜脈管路、抽血、病史 |
| 5–20 分 | 初始治療 | Lorazepam IV 0.1 mg/kg（上限 4 mg，可重複一次）；Midazolam IM 10 mg（>40 kg）或 5 mg（13–40 kg），單次；Diazepam IV 0.15–0.2 mg/kg（上限 10 mg，可重複一次）；替代：phenobarbital 15 mg/kg、直腸 diazepam 0.2–0.5 mg/kg |
| 20–40 分 | 第二線 | Levetiracetam 60 mg/kg（上限 4,500 mg）、fosphenytoin 20 mg PE/kg（上限 1,500 mg PE）、valproate 40 mg/kg（上限 3,000 mg）；另列 phenytoin、phenobarbital、lacosamide |
| >40 分 | 第三線／難治性 | 麻醉劑負荷與持續輸注劑量（NCS 2012）：midazolam、propofol、pentobarbital，自動換算 mg 與 mg/h；插管與連續腦波 |
| 麻醉劑 ≥24 小時 | 超難治性（SRSE） | Ketamine（負荷 0.5–5 mg/kg、輸注 1–10 mg/kg/h，文獻範圍）、吸入性麻醉劑、免疫治療（72 小時內）、生酮飲食（勿與 propofol 併用） |

其他功能：
- **發作計時**：頂部時間軸游標即時移動，目前階段高亮；可輸入「已發作幾分鐘」回推發作開始時間。
- **建議下一步**：依時間與已給藥物即時提示，例如超過 5 分鐘未給 benzodiazepine、第一劑後 5 分鐘仍發作要重複、benzodiazepine 無效改用第二線、第二線無效進入難治性處置；需要立即處理時轉為紅色。
- **給藥紀錄**：每次按「記錄給藥」都會記下時間與劑量；可復原與複製。
- **加護病房支持照護**：連續腦波、動脈導管與升壓劑；propofol 熱量計算（1.1 kcal/mL、每 mL 0.1 g 脂肪），劑量 >4 mg/kg/h 時提示 propofol infusion syndrome 風險。
- **發作停止後檢核**：連續腦波（1 小時內開始，昏迷者至少 48 小時）、維持性抗癲癇藥、找原因、呼吸道評估、追蹤檢驗。

## 使用方式

直接用瀏覽器開啟 `index.html` 即可，不需安裝或建置。

## 在地化設定

| 項目 | 位置 |
|---|---|
| Benzodiazepine | `<script>` 內 `BENZO`、`BENZO_ALT` |
| 第二線藥物 | `SECOND` |
| 麻醉劑輸注 | `INF` |
| 穩定期與發作後檢核 | `STAB`、`POST` |
| 下一步提示邏輯 | `nextSteps()` |

## 資料與隱私

- 所有資料只存在該瀏覽器的 `localStorage`，不會上傳；重新整理頁面後計時會繼續。
- 只記錄床號與體重，請勿輸入姓名或病歷號。

## 依據

1. Glauser T, Shinnar S, Gloss D, et al. Evidence-based guideline: treatment of convulsive status epilepticus in children and adults: report of the Guideline Committee of the American Epilepsy Society. *Epilepsy Curr* 2016;16:48–61.
2. Brophy GM, Bell R, Claassen J, et al. Guidelines for the evaluation and management of status epilepticus. *Neurocrit Care* 2012;17:3–23.
3. Kapur J, Elm J, Chamberlain JM, et al. Randomized trial of three anticonvulsant medications for status epilepticus (ESETT). *N Engl J Med* 2019;381:2103–2113.
4. Shorvon S, Ferlisi M. The treatment of super-refractory status epilepticus: a critical review of available therapies and a clinical treatment protocol. *Brain* 2011;134:2802–2818.
5. Review and updates on the treatment of refractory and super refractory status epilepticus. [PMC8304618](https://pmc.ncbi.nlm.nih.gov/articles/PMC8304618/)
6. Wickstrom R, et al. International consensus recommendations for management of new onset refractory status epilepticus (NORSE) including febrile infection-related epilepsy syndrome (FIRES). *Epilepsia* 2022.

## 授權

請依使用單位規定自行選擇授權方式（例如 MIT）。
