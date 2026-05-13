# DM_UET Handoff Notes

## Repo

- Da tao repo Git rieng trong `D:\Caohoc\WebMining\cuoiki\DM_UET`.
- Da push len remote: `https://github.com/nghia0303/reportwebmining`
- Nhanh hien tai: `main`

## Citation / References

- Da bo sung them tai lieu tham khao de tang so luong muc trong bibliography, khong chi la tang mat do cite.
- Rule hien tai:
  - `paper`: nen tai PDF local va doi chieu truoc khi cite.
  - `tool/web`: co the cite trang chinh thuc, khong can paper.
- Da tao thu muc kiem chung:
  - `refs_checked/`
  - `refs_checked/VERIFIED.md`
- Da tai va doi chieu local cho nhieu paper nhu:
  - `SciBERT`
  - `SPECTER`
  - `S2ORC`
  - `Passage Re-Ranking with BERT`
  - `OpenAlex`
  - `BEIR`
  - `ESRA`
  - `AI-Driven Research Support Systems`
  - `GraphRAG`
- Da thay cite paper cho `VOSviewer` va `CiteSpace` bang cite tool:
  - `vosviewerTool2026`
  - `citespaceTool2026`
- Da xoa 2 entry paper cu khoi `references.bib`:
  - `vaneck2010vosviewer`
  - `chen2006citespace`

## Related Work

- Da mo rong subsection `Graph-Based and Research Support Systems`.
- Da them related work cho:
  - `scite`
  - `Consensus`
  - `Perplexity Research`
  - `ChatGPT Deep Research`
  - `Gemini Deep Research`
- Da giam cac cum cite dai o cuoi doan de van doc tu nhien hon.
- Da tiep tuc viet lai doan ket `Related Work` de bo cac cum tieng Anh kho hieu nhu `bibliometric`, `literature discovery`, `pipeline`, thay bang cach dien dat de hieu hon nhung van giu lap luan ve khoang trong nghien cuu.

## Figure 1

- Da sua lai `Fig 1` trong `main.tex`.
- Bo cuc hien tai:
  - Hang tren: `Raw data -> Parser -> Qwen3 Embedding -> Milvus`
  - Nhanh metadata: `Parser -> SQLite -> FastAPI`
  - Hang duoi: `Streamlit UI -> FastAPI -> Query Planner -> Hybrid Search -> Qwen3 Reranker -> Ollama/LLM`
- Muc tieu cua ban sua:
  - Bo mui ten gay khuc xau o nhanh `Parser -> SQLite/Embedding`
  - Khong de arrow xuyen node
  - Hinh de doc hon
- Trang thai:
  - Tot hon ban cu ro ret
  - Van co the toi uu tiep neu muon giam chieu cao figure, vi du rut ngan duong `Milvus -> Hybrid Search`

## Table XII

- Da sua bang `System performance va row-count checks`.
- Da doi qua `tabular*`, giam `tabcolsep`, rut gon mot so nhan:
  - `Value/Count` -> `Count`
  - `Milvus rows`
  - `SQLite papers`
  - `Chat mock gen.`
- Ket qua:
  - Khong con `Overfull \\hbox` o block bang nay.

## Conclusion

- Da gop:
  - `Section VIII: Limitations and Future Work`
  - `Section IX: Conclusion`
- Thanh:
  - `Conclusion and Future Work`
- Da viet lai de phan cuoi gon hon:
  - 1 doan tong ket ket qua chinh
  - 1 doan neu han che va huong phat trien

## Compile Status

- Da build lai bang `pdflatex`.
- File hien tai:
  - `main.pdf`
- Sau khi gop section, PDF con `7` trang.
- Warning con lai trong `main.log` chu yeu la cac overfull/underfull cu, khong phai do Figure 1 hay Table XII.
- Overfull dang con:
  - lines `282--282`
  - lines `340--350`
  - lines `418--429`

## Important Note

- Trong qua trinh sua co luc da chay `pdflatex` song song tren cung file, lam PDF/aux bi nhieu tam thoi.
- Trang thai hien tai da duoc build lai tuan tu va phuc hoi on.

## Editorial Rule

- Can tiep tuc ra soat toan bai de sua cac loi thuoc hai nhom:
  - `implementation leakage`
  - `README/docs tone`
- `implementation leakage` la truong hop than bai lo qua nhieu chi tiet noi bo cua code/implementation, vi du:
  - ten file
  - ten field
  - ten endpoint
  - ten collection/checkpoint
  - command van hanh
- `README/docs tone` la truong hop cau van nghe giong tai lieu huong dan, ghi chu ky thuat hoac README hon la van phong bao cao hoc thuat.
- Khi ra soat lai, uu tien:
  - thay ten artifact noi bo bang cach goi khai quat hon
  - doi cach dien dat tu giong huong dan sang giong mo ta phuong phap/he thong
  - giu lai chi tiet ky thuat chi khi no thuc su phuc vu lap luan cua bao cao

## Main Files Touched

- `main.tex`
- `references.bib`
- `refs_checked/VERIFIED.md`
- `WORKLOG_HANDOFF.md`

## Suggested Next Steps

1. Neu can dep hon nua, toi uu tiep `Fig 1` de giam chieu cao va can layout.
2. Sua 3 cum `Overfull \\hbox` con lai trong than bai.
3. Neu muon, day tiep citation/local-verification theo rule da chot.

## Section IV Plan

- Da chot huong sua phan `Materials and Methods` theo cach 2: gop cac subsection nho lai cho gon hon thay vi giu nguyen cau truc hien tai.
- Cau truc du kien:
  - `Dataset`
  - `Data Storage and Indexing`
  - `Retrieval and Query Processing`
  - `Generation and System Interface`
- Mapping du kien:
  - giu nguyen `Dataset`
  - giu nguyen `Data Storage and Indexing`
  - gop `Query Planning` + `Hybrid Retrieval` + `Reranking and Evidence Construction`
  - doi `Generation and User Interface` thanh `Generation and System Interface`
- Rule thao tac:
  - lam tung buoc nho, khong rewrite ca section trong mot lan
  - moi lan sua phai trinh ro pham vi, noi dung doi, ly do
  - user duyet roi moi sua `main.tex`
  - sau moi lan sua xong phai cap nhat lai handoff/worklog
- Tien do hien tai:
  - Da bo sung mot doan dan o dau `Materials and Methods`, sau do tiep tuc doi thanh ban goi ten ro 4 phan va bo cach chen tu `subsection` vao trong van xuoi.
  - Da sua `Dataset` theo huong giam schema noi bo, bo `combined_text`, doi `paper/crawl/record` sang cach viet tu nhien hon.
  - Da bo cach goi dataset bang ten file `Clean_data.csv` trong than bai; phan noi dung chinh gio dung cach goi formal hon: `tap du lieu bai bao arXiv do nhom thu thap va chuan hoa`.
  - Da tiep tuc rut gon mo ta ve phan van ban phuc vu retrieval theo huong tu nhien hon: `phan noi dung van ban da duoc lam sach, phuc vu cho cac buoc truy xuat va xu ly ngu nghia`.
  - Da bo sung ghi chu rang du lieu thu thap ban dau co pham vi rong hon, nhung bao cao chi su dung giai doan `2021--2026` do gioi han tai nguyen tinh toan va kha nang lap chi muc hien tai.
  - Da viet lai doan `557,134` va `39,336` theo huong hoc thuat hon, tranh dung nhan noi bo `partial-index`, dong thoi noi ro tung con so dung de lam gi va vi sao ton tai hai quy mo du lieu khac nhau.
  - Da bo sung ref cho `Bảng II` va `Bảng III` trong doan `Dataset`. Sau do da bo giai phap `\\FloatBarrier` vi gay khoang trong xau trong layout IEEE 2 cot; hien tai giu ref bang de lien ket noi dung, con vi tri bang de LaTeX tu can doi.
  - Da bo sung 2 cau nhan xet ngan cho `Bảng II` va `Bảng III` de cac bang khong chi dung lai o muc liet ke so lieu, ma co dien giai vai tro cua phan bo theo nam va phan bo theo nhom chu de.
  - Da sua `Data Storage and Indexing` theo huong co context ro hon (`Trong nghien cuu nay`), doi cach dien dat implementation-heavy thanh giong bao cao hon, nhung van giu cac thong tin ky thuat cot loi ve SQLite, Milvus, BM25 va embedding.
  - Da bo han cau nhac `SciBERT` va `SPECTER` khoi `Data Storage and Indexing` vi khong can thiet cho mo ta he thong dang dung trong subsection nay.
  - Da bo sung them mot cau giai thich ly do tach SQLite va Milvus thanh hai lop luu tru, de subsection nay du do day va noi ro hon vai tro cua cach to chuc du lieu.
  - Da tiep tuc doi cau nay sang cach dien dat manh va truc dien hon, nhan ro muc tieu cua viec tach hai lop luu tru.
  - Da sua `Query Planning` theo huong bo cach goi implementation-heavy nhu `search`, `query planner`, `intent`, `filter`, thay bang cach dien dat tu nhien hon nhung van giu du logic cua qua trinh phan tich truy van va tao dieu kien loc.
  - Da sua `Hybrid Retrieval` theo huong giu nguyen noi dung ky thuat va cong thuc RRF, nhung doi cach dien dat tu nhien hon va biet hoa ro hon cac tham so benchmark.
  - Da sua `Reranking and Evidence Construction` theo huong gon hon, bo cau literature context khong can thiet va Viet hoa cac cum implementation-heavy nhu `candidates`, `prompt builder`, `claim`.
  - Da sua `Generation and User Interface` theo huong giu chat bao cao mon hoc, nhung bo bot giong README/product va lam ro hon vai tro cua model sinh, giao dien Streamlit va API FastAPI.
  - Da thuc hien buoc gop subsection theo ke hoach. Phan IV hien con 4 subsection chinh la `Dataset`, `Data Storage and Indexing`, `Retrieval and Query Processing`, va `Generation and System Interface`.
  - Da tiep tuc chinh nhe `Generation and System Interface` de bo cach dien dat giong tai lieu UI/API va lam ro hon vai tro cua Streamlit va FastAPI trong he thong.
  - Da bat dau Section V bang cach viet lai doan mo dau de dan tu phan `Materials and Methods` sang kien truc trien khai tong the, dong thoi Viet hoa cach mo ta hai luong offline/online.
  - Da bo ten file `Clean_data.csv` khoi node dau vao cua Figure 1 va thay bang cach goi formal hon la `Du lieu bai bao arXiv`.
  - Da tiep tuc sua Figure 1 theo logic he thong trong docs/source, bo sung duong phan hoi `LLM -> FastAPI -> UI` de khong bi dut luong output o node sinh cau tra loi.
  - Da tiep tuc doi duong phan hoi cua Figure 1 cho di vong xuong duoi roi moi quay lai `FastAPI` va `UI`, de tranh mui ten gap khuc xau sat cac khoi xu ly.
  - Da tiep tuc don Figure 1 theo huong gon hon: doi `Streamlit UI <-> FastAPI` thanh ket noi hai chieu o tang tuong tac, va chi giu mot duong phan hoi rieng `LLM -> FastAPI` o phia duoi de tranh mui ten chong cheo duoi node `FastAPI`.
- Da tiep tuc doi `Streamlit UI <-> FastAPI` ve lai mui ten mot chieu `UI -> FastAPI` de dong bo phong cach mui ten voi cac canh con lai trong figure.
- Da tiep tuc don Section V theo hai nhom loi `implementation leakage` va `README/docs tone`, cu the:
  - Viet hoa va lam hoc thuat hon caption cua Figure 1.
  - Viet lai bang `Cac thanh phan trien khai chinh` de bo cach goi README-like nhu `Raw data`, `Analytics DB`, `Backend`, `Frontend`, `UI 7 tab`.
  - Viet lai doan cau hinh phan cung theo giong mo ta he thong, giam cac cum implementation-heavy nhu `runtime`, `encode batch`, `compute capability`.
- Da chinh lai mot nhan trong bang thanh phan trien khai theo nghia sat hon:
  - `Nguon du lieu` -> `Du lieu tho`.
- Da bat dau don Section VI tu subsection mo dau va bang coverage:
  - Doi tieu de `Coverage by Product Tab` thanh cach goi trung tinh hon theo chuc nang he thong.
  - Viet lai doan mo dau de bo giong product/docs nhu `7 tab san pham`, `mapping`, `artifact`.
  - Viet hoa va lam tu nhien hon bang `tab:coverage`, giu `benchmark` o nhung cho hop ly va doi cot trang thai `Covered` thanh `Co`.
- Da tiep tuc sua `Benchmark Configuration` trong Section VI:
  - Bo duong dan run noi bo va cac chi tiet artifact nhu thu muc chay cu the.
  - Giu lai cac thong so cau hinh quan trong nhu `\partialindex`, so mau retrieval, `top_k`, model sinh chinh va cac model so sanh.
  - Doi cach dien dat de giam giong README/nhat ky chay benchmark.
- Da tiep tuc don hai subsection dau cua Section VII:
  - Doi cac cum nhu `Search`, `production Milvus index`, `Chat/RAG production` sang cach goi hoc thuat va trung tinh hon.
  - Viet lai caption cua bang retrieval va bang RAG cho khop voi cach dien dat moi.
  - Lam ro hon cac cum nhan xet nhu `title-derived queries`, `partial index`, `retrieved evidence` bang tieng Viet tu nhien hon.
- Da chinh nhe bang `tab:rag-results` bang cach giam `\tabcolsep` de tranh bi an nhe sang cot ben phai.
- Da tiep tuc keo hep hon bang `tab:rag-results` bang cach giam them `\tabcolsep` tu `4pt` xuong `3pt`.
- Da sua bang `tab:components` bang cach doi sang cac cot co do rong co dinh va them `\small`, de noi dung tu xuong dong va tranh tran sang cot ben phai.
- Da thu doi `tab:generator-results` tu `table*` ve `table` de dua bang IX ve 1 cot.
- Sau khi build lai:
  - bang IX compile duoc; sau khi giam font, thu hep `\tabcolsep` va rut header `Generator` -> `Model`, muc `overfull` lon cua bang nay da duoc loai bo;
  - bang X van la ung vien hop ly de giu 2 cot;
  - bang XI da doi ve 1 cot nhung van can bop them neu muon het tran.
- Da tiep tuc bop ngang bang X va XI:
  - bang X: giam `\tabcolsep` va rut nhe header cot (`Cases` -> `N`, `Errors` -> `Err.`, `Metric chinh` -> `Metric`, `Dien giai` -> `Ghi chu`);
  - bang XI: giam `\tabcolsep` nhung giu nguyen header va noi dung.
- Sau khi build lai:
  - hai muc `overfull` lon truoc do cua bang X va XI da bien mat;
  - bang X van dang de `table*`, nhung phan tran ngang lon da duoc xu ly tot hon.
- Da thu ep bang X (`tab:model-stage`) ve 1 cot bang cach:
  - doi `table*` -> `table`;
  - doi cac cot `p{...}` tu `\textwidth` sang `\columnwidth`.
- Ket qua thu:
  - compile thanh cong, so trang giam con `7`;
  - nhung bang X phat sinh nhieu `overfull` moi trong chinh cac o du lieu, dac biet o cot `Model/Stack` va `Metric`;
  - ve mat hien thi, phuong an 1 cot hien tai kem on dinh hon phuong an 2 cot da bop ngang.
- Da tra bang X ve 2 cot va chuyen khối bang len ngay sau subsection de no co co hoi nam gan phan noi dung hon.
- Sau khi build lai:
  - so trang tro lai `8`;
  - cac canh bao `overfull` lon phat sinh do phuong an 1 cot da bien mat;
  - phuong an hien tai cho bang X la: giu `table*`, giu `\tabcolsep` nho va header cot da rut gon.
- Da thu lai bang X theo huong 1 cot, nhung lan nay bop manh hon:
  - `table*` -> `table`;
  - `\scriptsize`, `\tabcolsep=1.5pt`;
  - rut ngan hai ten stack dai nhat thanh `stack_a_cached` va `stack_b_bge`;
  - giu header ngan nhu hien tai.
- Ket qua build:
  - PDF con `7` trang;
  - bang X kha hon lan thu 1 cot dau tien, nhung van con `overfull` nhe trong cac o `Model/Stack` va `Metric`;
  - phuong an 1 cot hien tai da kha dung hon, nhung chua sach bang phuong an 2 cot.
- Da tiep tuc chinh rieng cot `Metric` cua bang X bang cach tach hai o metric dai nhat thanh 2 dong.
- Sau khi build lai:
  - muc tran cua cot `Metric` giam ro, khong con chen manh sang cot `Ghi chu` nhu truoc;
  - van con mot vai canh bao `overfull` nhe trong bang X, chu yeu do noi dung cot `Model/Stack`.
- Da thu giam co chu cua bang X tu `\scriptsize` xuong `\tiny`.
- Sau khi build lai:
  - bang X co gon hon, nhung van con tran nhe o cot `Model/Stack`;
  - cac muc tran con lai chi o muc nho hon truoc, chu yeu quanh hai dong model `Qwen3-*` va phan ghi chu loi runtime.
- Da tang nhe `\tabcolsep` cua bang X tu `1.5pt` len `2pt` de bang do bi hon mot chut.
- Sau khi build lai:
  - bang thoang hon, nhung van con tran nhe trong cot `Model/Stack`;
  - cac muc tran con lai van o muc nho, khong quay lai tinh trang tran lon nhu cac lan thu ban dau.
- Da tiep tuc tang `\tabcolsep` cua bang X len `2.5pt` va doi hai o `Metric` sang `\shortstack[l]{...}` de can trai tu nhien hon.
- Sau khi build lai:
  - cac canh bao tran goc tu bang X khong con xuat hien trong log;
  - bang X giu duoc dang 1 cot, cot `Metric` khong con chen sang `Ghi chu`, va bo cuc thoang hon so voi ban truoc.
- Da doi kieu cot `Metric` cua bang X tu `p{...}` sang `m{...}` de can giua theo chieu doc, tranh cam giac dong `R@10=...` bi keo len tren.
- Da sua them mot doan thao luan trong phan ket qua de giam `README/docs tone`, cu the:
  - bo cac cum nhu `cau hinh mac dinh cua Search va Chat`, `benchmark production`, `cho UI`;
  - doi sang cach dien dat formal hon ve cau hinh phu hop nhat cho truy xuat va hoi-dap, va ve do tre chap nhan duoc cho tuong tac nguoi dung.
- Da chinh lai rieng bang IX `tab:generator-results` de tra co chu tu `\tiny` len `\footnotesize`, sau khi nhan ra da bop chu cua bang nay qua tay.
- Da viet lai doan `Analytics and Graph Results` theo huong formal hon:
  - doi cac cum `paper`, `keyword probes`, `graph queries`, `node`, `edge`, `descriptive metrics`, `expert judgment` sang cach goi hoc thuat hon;
  - doi caption bang thanh `Ket qua phan tich thong ke va mo ta do thi`;
  - doi hai nhan hang `Trend keywords`, `Graph queries` thanh `Truy van xu huong`, `Truy van do thi`.
- Da doi ten section `Reproducibility Notes` thanh `Code Availability`, vi noi dung hien tai chi mo ta noi truy cap ma nguon, chua du de goi la ghi chu tai lap thuc nghiem.
- Da dua thong tin hoc phan va giang vien huong dan xuong footnote o trang 1 bang `\thanks{...}` trong `\title{...}`.
- Do `IEEEtran` conference mode khoa `\thanks`, da bat `\IEEEoverridecommandlockouts` trong preamble de footnote hien dung o trang dau.
- Da tiep tuc lam sach van phong o Section VII va Conclusion:
  - viet lai `Open-source Generator Comparison` theo huong formal hon, bo cac cum nhu `generator nhanh nhat trong cac model local lon`, `citation behavior`, `fixed evidence`;
  - viet lai doan giai thich `Retriever, Reranker and Full-stack Diagnostics`, doi `diagnostics`, `smoke diagnostic`, `runtime` sang cach dien dat hoc thuat hon;
  - viet lai `Task-specific Evaluation`, bo cac cum `task gap`, `server-side`, `future work`;
  - viet lai `System Performance`, bo `default production mode`, `smoke test`;
  - viet lai doan 2 cua `Overall Discussion`, bo `model thang tuyet doi`, `demo tuong tac`, `tab Models`, `trade-off`;
  - viet lai ca hai doan trong `Conclusion and Future Work`, giam cac cum `analytics`, `local LLM generation`, `UI 7 tab`, `production`, `build full`, `serving`.
- Da build lai sau dot sua tren; compile thanh cong, khong phat sinh loi moi, cac warning con lai chu yeu la warning dan trang cu.
- Da tiep tuc chuan hoa mot nhom thuat ngu con sot o phan dau bai:
  - abstract: doi `paper`, `Milvus production`, `Chat/RAG`, `known-item retrieval` sang cach goi tu nhien hon;
  - phan dong gop trong Introduction: doi `paper` thanh `bai bao`;
  - `Problem Formulation`: bo cach liet ke field name thô nhu `abstract`, `keyword/category`, `node/edge`; doi `grounded/citation` thanh `muc do co dan chung`;
  - `Dataset`: doi `analytics`, `paper`, `production index` va mot so caption/nhan bang sang cach goi thong nhat hon.
- Da build lai 2 luot sau dot chuan hoa tren; compile thanh cong, cross-reference on dinh, khong phat sinh loi moi.
- Da thuc hien mot luot ra cuoi theo huong `khong co dich qua tay`:
  - chi sua cac cho lech ro ma tieng Viet van sat nghia, nhu `title`, `abstract`, `runtime`, `title-based`, `related work` (trong ngữ cảnh mo ta loai truy van), mot so caption/ngan hang;
  - giu nguyen cac thuat ngu ky thuat ma dich sang tieng Viet de gay go nhu `benchmark`, `category`, `evidence`, `groundedness`, `known-item`.
- Sau luot ra cuoi:
  - compile da on dinh lai sau 3 lan `pdflatex`;
  - so trang hien tai la `8`;
  - cac viec con lai chu yeu la layout/overfull-underfull, khong con nhieu van de lon ve thuat ngu.
- Da xu ly tiep 3 diem layout dang gay `overfull` chinh:
  - bop nhe bang `tab:data-overview` bang cach giam `\tabcolsep`;
  - giam tiep do rong/spacing bang `tab:components`;
  - giam `\tabcolsep` cho bang `tab:retrieval-results`.
- Sau 3 lan build de on dinh:
  - cac `overfull` chinh da duoc loai bo;
  - so trang hien tai van la `8`;
  - warning con lai chu yeu la `underfull` nho trong mot vai o bang hep va cac URL dai trong references, khong con la van de lon ve bo cuc.

## Ghi Chu Cho Leader Duyet

### Nhan xet hien tai

- Bao cao hien da sach hon ve van phong va thuat ngu, nhung van co the tao cam giac `hoi mong` o 3 diem:
  - phan ket qua co so lieu nhung dien giai chua sau;
  - phan phuong phap mo ta he thong kha ro nhung ly do thiet ke va trade-off chua du day;
  - phan gioi han va huong phat trien co y chinh nhung chua tach ro tung nhom van de.

### Huong lam day uu tien

1. Day them `Experimental Results and Discussion`
- Day la cho tang chat luong bao cao hieu qua nhat.
- Moi bang chinh nen co them 2--4 cau tra loi ro:
  - ket qua nao noi bat nhat;
  - vi sao ket qua do xuat hien;
  - ket qua do noi gi ve he thong;
  - trong tinh huong nao thi ket qua do chua du manh.

2. Bo sung ly do thiet ke trong `Materials and Methods`
- Co the them ngan gon:
  - vi sao tach `SQLite` va `Milvus`;
  - vi sao dung `hybrid retrieval` thay vi dense-only hoac sparse-only;
  - vi sao tach benchmark thanh retrieval, generator va full-stack.

3. Mo rong `Conclusion and Future Work`
- Nen tach ro hon cac nhom gioi han:
  - gioi han du lieu;
  - gioi han benchmark/danh gia;
  - gioi han ha tang;
  - gioi han kha nang khai quat hoa.

### Co the lam day `Related Work` khong?

- Co, nhung nen lam day theo chieu sau lap luan, khong nen chi them them cite.
- `Related Work` hien tai da co khung hop ly, nhung van co the day them theo 3 huong sau:

1. Lam ro hon su khac nhau giua cac nhom cong trinh
- Moi cum co the ket bang 1--2 cau tong ket:
  - nhom retrieval giai quyet tot bai toan tim tai lieu;
  - nhom RAG giai quyet tot bai toan sinh cau tra loi co dan chung;
  - nhom graph/research-support giai quyet tot bai toan kham pha boi canh nghien cuu.

2. Tang do ro cua `research gap`
- Sau moi cum nen chi ra gioi han cu the hon, thay vi chi noi chung chung.
- Vi du:
  - retrieval manh nhung chua tro thanh he thong ho tro nghien cuu tich hop;
  - RAG manh cho hoi-dap nhung chua bao phu du nhu cau analytics va so sanh phuong phap;
  - graph/research-support systems huu ich nhung thuong thien ve mot lat cat rieng.

3. Them 1 doan chot cuoi section
- Doan nay nen noi ro:
  - he thong trong bao cao nam o giao diem cua retrieval, RAG, analytics va research-support;
  - khoang trong ma bao cao muon thu hep la su thieu vang mot he thong tich hop cac nhu cau nay tren cung mot corpus arXiv cuc bo va co danh gia dinh luong.

### Luu y khi lam day `Related Work`

- Khong nen bien section nay thanh danh sach cong cu.
- Uu tien mo rong phan so sanh va research gap hon la them nhieu ten he thong moi.
- Neu can them do day, nen them 1--2 doan phan tich sau moi cum, thay vi them 4--5 citation moi ma khong co lap luan.

### Kien nghi neu can uu tien mot cho de nang chat bao cao

- Uu tien 1: `Experimental Results and Discussion`
- Uu tien 2: `Related Work`
- Uu tien 3: `Conclusion and Future Work`

- Neu leader muon bao cao day hon ma van giu chat luong, cach an toan nhat la mo rong Section VII truoc, sau do bo sung lap luan trong `Related Work`.

## Bo Sung Theo Y Kien Leader (2026-05-13)

### 1. Them dinh nghia RAG

- Co, nen them.
- Vi tri hop ly nhat:
  1. `Introduction`
  - Sau cau noi ve han che cua LLM neu chi dua vao tri thuc tham so.
  - Nen viet 1--2 cau ro nghia:
    - RAG la cach ket hop truy xuat tai lieu lien quan truoc khi sinh cau tra loi;
    - muc tieu la tang tinh co can cu va giam tra loi khong dung tai lieu.
  2. `Related Work` / `Retrieval-Augmented Generation`
  - Co the mo rong them 1 cau de tach bach:
    - RAG khong chi la `retrieval + generation`, ma la mot co che rang buoc cau tra loi vao tap evidence duoc truy xuat.

- Khong nen lam dai qua:
  - tong cong 2--3 cau la du;
  - tranh lap lai dung nghia giong nhau o nhieu cho.

### 2. Giai thich tai sao lai dung Milvus

- Co, nen them, vi day la quyet dinh thiet ke quan trong nhung hien tai ly do chua du ro.
- Vi tri hop ly nhat:
  1. `Data Storage and Indexing`
  - Them 2--3 cau sau doan mo ta hai lop `SQLite` va `Milvus`.
  - Y can lam ro:
    - Milvus phu hop vi can luu va truy van dense vector va sparse representation trong cung mot he thong;
    - ho tro hybrid retrieval, ket hop BM25 va vector search;
    - phu hop voi bai toan truy xuat tren corpus lon hon la chi dung mot CSDL quan he.
  2. `System Design and Implementation`
  - Co the them 1 cau nhac lai vai tro cua Milvus trong luong online:
    - day la lop chi muc phuc vu truy xuat nhanh cho retrieval va RAG.

- Khong nen viet theo kieu quang ba cong nghe.
- Nen giai thich bang ngon ngu quyet dinh he thong:
  - `chon Milvus de ho tro retrieval lai va mo rong chi muc vector`, khong phai `vi Milvus pho bien`.

### 3. Ra tung section xem co the lam day o dau ma khong lan man

#### Introduction
- Co the day them rat nhe.
- Nen them:
  - 1 cau dinh nghia RAG ro hon;
  - 1 cau noi vi sao bai toan nay khong chi la hoi-dap.
- Khong nen them nhieu vi mo bai da kha day.

#### Problem Formulation
- Chi nen day rat it.
- Co the them:
  - 1 cau chot ly do can nhieu kieu dau ra khac nhau.
- Khong nen them qua nhieu ky hieu hay formalism moi.

#### Related Work
- Co the day them tot, nhung theo chieu sau lap luan.
- Nen them:
  - 1--2 cau tong ket sau moi subsection;
  - 1 doan chot cuoi section noi ro hon he thong cua bao cao nam o giao diem nao giua retrieval, RAG, analytics va research-support.
- Day la cho co the lam day ma van hoc thuat, neu lam dung cach.

#### Materials and Methods
- Day la cho nen day them muc vua.
- Nen them:
  - ly do chon `Milvus`;
  - ly do tach `SQLite` va `Milvus`;
  - ly do dung `hybrid retrieval`;
  - ly do tach benchmark retrieval / generator / full-stack.
- Moi y chi can 1--2 cau.

#### System Design and Implementation
- Co the day them nhe.
- Nen them:
  - 1 cau noi vai tro cua luong ngoai tuyen va truc tuyen;
  - 1 cau nhac ly do luc nao du lieu di vao `SQLite`, luc nao di vao `Milvus`.
- Khong nen bien section nay thanh README cong nghe.

#### Evaluation Methodology
- Con day du, nhung co the day them co chu dich.
- Nen them:
  - 1 cau giai thich vi sao dung `weak label` cho retrieval benchmark;
  - 1 cau noi han che cua benchmark hien tai.
- Khong nen them qua nhieu cong thuc hay metric moi.

#### Experimental Results and Discussion
- Day la cho nen uu tien lam day nhat.
- Moi subsection nen co them 2--4 cau phan tich:
  - ket qua nao noi bat;
  - vi sao;
  - ham y gi cho he thong;
  - khi nao thi ket qua nay chua du thuyet phuc.
- Neu can tang do day nhanh ma van chat luong, uu tien section nay dau tien.

#### Conclusion and Future Work
- Co the day them muc vua.
- Nen tach ro hon:
  - gioi han du lieu;
  - gioi han benchmark;
  - gioi han ha tang;
  - huong mo rong corpus va danh gia con nguoi.
- Phan nay day them se tao cam giac bao cao chin hon.

### 4. Thu tu uu tien neu can lam tiep

1. Them dinh nghia RAG trong `Introduction`
2. Them ly do chon `Milvus` trong `Data Storage and Indexing`
3. Day them `Experimental Results and Discussion`
4. Day them `Related Work`
5. Mo rong `Conclusion and Future Work`

### 5. Nguyen tac chung

- Moi cho chi them 1--3 cau co gia tri, khong chen doan dai neu y do da ro.
- Uu tien:
  - ly do thiet ke;
  - y nghia cua ket qua;
  - gioi han va khoang trong.
- Khong uu tien:
  - liet ke them ten cong cu;
  - lap lai dinh nghia da co;
  - nhac lai chi tiet implementation noi bo.

## Leader Review - Noi Co The Lam Day Them (ban rut gon, khong lan man)

### Muc tieu chung

- Bao cao hien tai da kha sach ve cau chu, nhung van co the "day" hon o 3 huong co gia tri:
  1. lam ro hon cac quyet dinh thiet ke;
  2. phan tich y nghia ket qua sau moi bang chinh;
  3. tach ro gioi han va huong mo rong.
- Nguyen tac van giu:
  - moi cho chi them 1--3 cau co gia tri;
  - uu tien ly do, ham y, gioi han;
  - khong mo rong theo kieu liet ke cong nghe hay lap y.

### Section I - Introduction

- Nen bo sung:
  - 1 cau dinh nghia RAG ro hon sau cau noi ve han che cua LLM.
  - 1 cau noi ro hon vi sao bai toan nghien cuu khong the giam ve mot he hoi-dap thuong.
- Ly do:
  - leader muon "them RAG dinh nghia";
  - day la cho doc gia can duoc dat nen khoi niem ngay tu dau.
- Muc day hop ly:
  - them tong cong 2 cau la du.

### Section II - Problem Formulation

- Co the day them rat nhe.
- Nen bo sung:
  - 1 cau ket noi giua cac kieu dau ra va nhu cau thuc te cua nguoi lam nghien cuu.
- Ly do:
  - hien section nay da ro ve mat hinh thuc, nhung van co the them 1 cau giai thich tai sao can nhieu loai output.
- Muc day hop ly:
  - 1 cau, khong them ky hieu moi.

### Section III - Related Work

- Co the day them kha tot ma van gon.
- Nen bo sung:
  - 1 cau tong ket cuoi subsection `Retrieval Methods for Scientific Documents` de noi ro retrieval giai quyet tot "tim tai lieu", nhung chua giai quyet "tong hop va phan tich".
  - 1 cau tong ket cuoi subsection `Retrieval-Augmented Generation` de noi ro RAG giai quyet grounding nhung chua bao phu analytics va research support.
  - 1 doan chot cuoi section noi ro hon he thong cua bao cao nam o giao diem nao giua retrieval, RAG, analytics va research-support systems.
- Ly do:
  - day them theo chieu sau lap luan, khong phai theo so luong paper.
- Muc day hop ly:
  - moi subsection them 1 cau;
  - doan ket section them 2--3 cau.

### Section IV - Materials and Methods

- Day la cho nen day them vua phai.
- Nen bo sung:
  - `Data Storage and Indexing`
    - them 2 cau tra loi ro "tai sao la Milvus" thay vi mot vector store khac hay chi dung SQLite.
    - huong dien dat nen la:
      - Milvus phu hop vi ho tro dong thoi dense vector va sparse representation;
      - ho tro hybrid retrieval va mo rong chi muc truy xuat tot hon CSDL quan he cho bai toan nay.
  - `Retrieval and Query Processing`
    - them 1 cau ly do tai sao hybrid retrieval la lua chon hop ly cho corpus khoa hoc.
  - `Benchmark Configuration`
    - them 1 cau giai thich tai sao retrieval benchmark, generator benchmark va full-stack diagnostics duoc tach rieng.
- Ly do:
  - day la cac quyet dinh thiet ke can duoc bao ve ro hon.
- Muc day hop ly:
  - tong cong moi subsection them 1--2 cau.

### Section V - System Design and Implementation

- Co the day them nhe.
- Nen bo sung:
  - 1 cau sau doan mo dau section de noi ro ly do can tach luong ngoai tuyen va truc tuyen.
  - 1 cau duoi Figure 1 hoac sau bang thanh phan de nhan manh Milvus la lop chi muc phuc vu truy xuat nhanh cho retrieval va RAG, con SQLite phuc vu thong ke va tra cuu.
- Ly do:
  - giup section nay bieu lo ro hon kien truc va vai tro tung lop, thay vi chi mo ta thanh phan.
- Muc day hop ly:
  - them 2 cau tong cong.

### Section VI - Evaluation Methodology

- Chi nen day co chu dich.
- Nen bo sung:
  - 1 cau sau `Retrieval Metrics` de giai thich retrieval benchmark hien tai la known-item benchmark va no phu hop de do kha nang tra cuu co muc tieu.
  - 1 cau sau `Answer and Citation Metrics` de noi ro nhung metric nay khong thay the danh gia chuyen gia toan dien.
- Ly do:
  - giup nguoi doc hieu benchmark do duoc gi va khong do duoc gi.
- Muc day hop ly:
  - tong cong 2 cau.

### Section VII - Experimental Results and Discussion

- Day la cho nen uu tien lam day nhat.
- Nen bo sung:
  - `Retrieval Performance`
    - them 1--2 cau giai thich vi sao hybrid retrieval vuot sparse va dense tren chi muc hien tai.
  - `RAG Answer Quality`
    - them 1--2 cau ve ham y cua citation coverage 0.8000 va required-term coverage 0.6417.
  - `Analytics and Graph Results`
    - them 1 cau noi ro vi sao cac chi so nay huu ich cho khai pha literature, du chua du de ket luan chat luong hoc thuat cua do thi.
  - `Open-source Generator Comparison`
    - them 1 cau ket noi ket qua model voi trade-off su dung thuc te.
  - `Retriever, Reranker and Full-stack Diagnostics`
    - them 1 cau tach bach ro "loi thuc thi" va "chat luong mo hinh".
  - `Task-specific Evaluation`
    - them 1 cau neu ro cac task nao hien da on, task nao con mong ve du lieu.
  - `Overall Discussion`
    - co the them 1 cau tong ket gia tri thuc te cua he thong trong bai toan nghien cuu.
- Ly do:
  - day la section tang "do day" hieu qua nhat ma khong can them bang hay cite.
- Muc day hop ly:
  - moi subsection them 1--2 cau phan tich.

### Section VIII - Conclusion and Future Work

- Co the day them muc vua.
- Nen bo sung:
  - tach gioi han thanh 3 nhom ro hon:
    - gioi han du lieu/index;
    - gioi han benchmark/ground truth;
    - gioi han ha tang va thuc thi.
  - them 1 cau noi ro huong phat trien uu tien nhat la mo rong Milvus index va bo sung human relevance assessment.
- Ly do:
  - phan nay day them se tao cam giac bao cao "chin" hon ma van rat gon.
- Muc day hop ly:
  - them 3--4 cau, khong can them subsection moi.

### Thu tu nen lam neu leader duyet

1. Bo sung dinh nghia RAG o `Introduction`.
2. Bo sung ly do chon Milvus o `Data Storage and Indexing`.
3. Day them `Experimental Results and Discussion`.
4. Day them `Related Work`.
5. Mo rong nhe `Conclusion and Future Work`.
