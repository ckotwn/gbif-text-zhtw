#### Document Control
| Date       | Description | Author(s) |
| ---------- | ----------- | --------- |
|            | 初譯        | 方品仁    |
| 2021-04-15 | 覆譯及審閱  | 柯智仁    |
|            | 發布        |           |



What is Darwin Core, and why does it matter?

什麼是達爾文核心集？它為何重要?

The Darwin Core Standard (DwC) offers a stable, straightforward and flexible framework for compiling biodiversity data from varied and variable sources.

達爾文核心集標準提供一個穩定，直觀且有彈性的框架，用來編譯來源眾多、內容豐富的生物多樣性資料。

[*Platyspiza crassirostris*](https://www.gbif.org/occurrence/899939168) by Brian Gratwicke licensed under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/).

Natural history collections, environmental monitoring programmes, recording societies, citizen scientist projects and others all hold valuable data on the world’s biodiversity. They collect and manage their information in many different systems and environments, and vary widely, depending on what kind of details are captured and stored for any individual record.

自然史博物館典藏、環境監測計畫、紀錄社團、公民科學家專案…等等都保有世界上生物多樣性的珍貴資料，它們從許多不同的系統及環境收集、管理資料，其中記錄及保存下來、個別紀錄的細節變化很大。

So how can we integrate these diverse datasets most simply and efficiently so scientists, analysts and policymakers can use them in research and policy?

我們能如何簡易、有效率地整合這些多元的資料集，讓科學家、分析人員及決策者可以運用在研究及政策上呢?

The [Darwin Core Standard (DwC)](http://rs.tdwg.org/dwc) offers a stable, straightforward and flexible framework for compiling biodiversity data from varied and variable sources. Originally developed by the [Biodiversity Information Standards (TDWG) community](http://www.tdwg.org/), Darwin Core is '[an evolving community-developed biodiversity data standard](http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0029715). It plays fundamental role in the sharing, use and reuse of open-access biodiversity data and today accounts for vast majority of the hundreds of millions of species occurrence records available through GBIF.org.

達爾文核心集標準（Darwin Core Standard, DwC）提供一個穩定、直觀且有彈性的框架，用來編譯來源眾多、內容豐富的生物多樣性資料。最初由[生物多樣性資訊標準（Biodiversity Information Standard, TDWG）](https://www.tdwg.org)社群發展而來，達爾文核心集是一個「[演化中的、社群開發的生物多樣性資料標準](http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0029715)」，在分享、使用、再利用開放存取生物多樣性資料扮演十分重要的根本角色，也占了今天 GBIF.org 十數億筆的物種出現紀錄資料中的絕大部分。

In practice, using Darwin Core revolves around a standard file format, the Darwin Core Archive (DwC-A). This compact package (a ZIP file) contains interconnected text files and enables data publishers to share their data using a common terminology. This standardization not only simplifies the process of publishing biodiversity datasets, it also makes it easy for users to discover, search, evaluate and compare datasets as they seek answers to today’s data-intensive research and policy questions.

實務上，使用達爾文核心集代表著使用一種標準檔案格式，亦即達爾文核心集檔案（Darwin Core Archive, DwC-A；以下簡稱為「達爾文檔案」）。這個簡潔的檔案（實為一 ZIP 壓縮檔）包含相互關連的純文字檔案，使得發布者們能使用共同的辭彙來分享資料。此標準化的結果不僅簡化了生物多樣性資料集的發布程序，也讓使用者在尋找今日資料密集的研究與政策問題答案時，更容易地探索、搜尋、評估與比較資料集。

Additional resources

相關資源

- Wieczorek J, Bloom D, Guralnick R, Blum S, Döring M, Giovanni R, et al. (2012) Darwin Core: An Evolving     Community-Developed Biodiversity Data Standard. PLoS ONE 7(1): e29715. [doi:10.1371/journal.pone.0029715](https://doi.org/10.1371/journal.pone.0029715).
- [iOBIS Darwin Core manual](http://www.iobis.org/manual/darwincore/) iOBIS 達爾文核心集手冊
- [Darwin Core terms](https://gcube.wiki.gcube-system.org/gcube/Darwin_Core_Terms) 達爾文核心集辭彙（連結至 Gcube 維基）

What’s in an archive?

檔案中有什麼？

When preparing a Darwin Core Archive version from their source data, publishers restructure and streamline information into a small but structured collection of text files. One of these files is the ‘core’ file and holds a separate record for each of the items included in the archive. Other ‘extension’ files may also be included. These contain additional information linked to the records in the core file. Extension files allow the archive to model many-to-one relationships.

當資料發布者使用來源資料準備產生達爾文檔案時，要將資訊重組輸出成小型但結構化的數個純文字檔，其中一個檔案稱做「核心檔」，達爾文檔案內的各項資料都有一個別紀錄儲存在此；也可能有「延伸檔」，其中包含連結到核心檔紀錄的附加資訊。延伸檔使得達爾文檔案中的資料形成多對一的關係模型。

Depending on how much information the source data contains—and how much they wish to share—publishers can create a Darwin Core Archive with one of three cores:

發布者可以依照來源資料的資訊量及願意分享的內容，以下列三種核心集擇一創建達爾文核心集檔案：

- a Taxon core, which lists a set of species, typically coming from the same region or sharing common     characteristics
- 分類群核心集，一般為同一個區域或者有相同特性的一組物種清單。
- an Occurrence core, which lists a set of times and locations at which particular species have been recorded.
- 出現紀錄核心集，列出一組特定物種出現時間及地點的紀錄。
- an Event core, which lists field studies (including the protocols used, the sample size, and the location for each).
- 調查活動核心集，紀錄田野研究資訊（包含個別的取樣協定、取樣規模，採集地點等）。

In the case of an Event core, one extension file usually contains the elements displayed in an Occurrence core, which enables the inclusion of many observation records as part of a single planned field study.

若是使用調查活動核心集，延伸檔中通常會有數個出現紀錄核心集檔案，這使得許多次的觀察紀錄可以包含在單一田野調查研究之內。

Finally, each archive contains two more pieces that help both machines and humans interpreting the data. The first, a descriptor file (meta.xml), defines the precise structure and relationships between the core and any extensions. The second, a complementary metadata file, describes the datasets contained in the archive, typically in Ecological Metadata Language (EML.xml)—though the GBIF’s [Integrated Publishing Toolkit](https://www.gbif.org/ipt) produces these files automatically for its users.

最後，每一個達爾文檔案會包含兩個或兩個以上的部分來協助機器及人解讀資料。第一部分為結構描述檔（meta.xml），用來定義核心集和延伸集之間精確的結構與關係。第二部分為附加的詮釋資料檔，用來提供資料集的背景資訊，通常以生生態詮釋資料語言（Ecological Metadata Language, EML）記載（EML.xml）。使用 GBIF 的[整合式資料發布工具](https://www.gbif.org/ipt)會自動幫使用者產生這些檔案。

Sharing species monitoring and sampling data with the Event Core 

以調查活動核心集分享物種監測和取樣資料

Efforts to track shifts in biodiversity patterns over space and time have increased the amount of species information available through sampling and monitoring programmes. In addition to having more precisely described methods than ‘presence-only’ data, these sample-based datasets capture richer, more complex details about species quantities and frequency.

透過調查採樣與監測計畫來追蹤生物多樣性在空間與時間上移動格局，成就、增加了物種資訊量。這些基於取樣的資料集在「簡單出現」（presence-only）資料之外精確地描述採樣方法，記錄下關於物種數量及頻度更豐富、複雜的內容。

With their frequent inclusion of repeated measurements from the same places, sampling-event data from ecological and environmental investigations are better at detecting shifts and trends in species populations—and critical to understanding the scope and speed of global change.

透過相同地點頻繁地多次測量取樣，生態及環境調查的調查活動資料更適合用在偵測物種族群的移動格局及趨勢，對於理解全球變遷的尺度和速度也很重要。

But to help make the most of these diverse data and ensure their efficient contribution to more precise scientific analyses and policy outcomes, researchers need easy access to them in a consistent, compatible format.

為了充分利用這些多元的資料並確保它們能有效地貢獻在精確的科學分析及政策上，研究人員需要一穩定及相容的格式以方便取用資料。

The Darwin Core Standard has become the most widely used open-access standard for biodiversity data. Developed to provide a simple way to document and share information about species occurrences, whether in the field or in a museum collection, the standard has made it possible to integrate hundreds of millions of records through GBIF.org.

達爾文核心集標準已經是生物多樣性資料廣泛使用的開放存取標準。不論是應用在田野工作或博物館典藏，此標準的開發提供一簡單的方法來記載或分享傳遞物種出現紀錄，也使十數億筆的資料透過 GBIF.org 整合成為可能。

Recent additions to Darwin Core detailed below support the aggregation of sampling-event datasets. The newly introduced ‘Event core’ places the sampling event at the center of the simplified dataset and links its protocol, effort and measurements to the species occurrences derived from the sampling events, which are appended as a separate extension in the standard’s one-to-many star schema.

下面將詳細說明達爾文核心集的近期新增內容如何支援匯整調查活動資料集。新導入的「調查活動核心集」將調查活動（事件）置於資料模型的核心，再連結取樣協定、努力量、測量值至個別調查活動的物種出現紀錄，再分別以延伸集掛載形成達爾文檔案標準的「一對多」星芒狀結構。

As a result, researchers can now tap into more complex, quantitatively richer records for analyses and combine them alongside others focused on single organisms or individual taxa. These changes could even lead to improvements in the quality and usefulness of datasets already published on GBIF.org that derive from more complex surveys and censuses.

研究人員因此從現在起可以取用更複雜、數量更豐富的紀錄加以分析，也可以結合其它專注在單一個體或分類群的紀錄。這次的內容改變更可以改善原本已經發布在 GBIF.org 上由更複雜的調查、普查所衍生資料集，提升其品質和實用性。

The hope is that mingling these varied sources of data will, rather than limiting or prescribing their uses, encourage their discovery and reuse—and perhaps even reveal higher-level relationships and insights that would not be apparent from examining individual records.

希望混合使用不同、多元來源的資料可以鼓勵資料的發掘及再利用，而非限制或規範它們的用途—也許甚至能顯現個別紀錄檢視無法明察的高階關係與見解。

How to get started

如何開始

The most efficient way to prepare and publish Darwin Core-based datasets is through GBIF’s [Integrated Publishing Toolkit](https://www.gbif.org/ipt). [EU BON](http://www.eubon.eu/) and other partners provided vital contributions toward the changes needed to support this new class of datasets. Data holders with ongoing monitoring programmes and sampling projects can also configure automatically scheduled publishing cycles on the multilingual-friendly IPT.

最具效率的方法就是透過 GBIF 的[整合式資料發布工具 IPT](https://www.gbif.org/ipt)。[歐洲生物多樣性觀測網絡（EU BON）](http://www.eubon.eu/)和其他的合作夥伴對於支援新資料類型的所需的修訂有重要的貢獻。整合式資料發布工具 IPT 支援多國語言，也可以讓資料的擁有者在監測計畫和調查專案持續進行的同時，設定資料自動發布週期。

What’s new in the DwC-A event core

調查活動核心集新增了那些內容？

The addition of the ‘event core’ to the Darwin Core Standard includes several new terms highly applicable to sample-based and monitoring data.

達爾文核心集標準中新增的「調查活動核心集」包含一些高度適用於基於取樣和監測資料的新辭彙：

- **eventID**: an identifier specific for the event in a dataset
- **事件識別碼**：資料集中每次採樣調查活動（事件）的識別碼



- **parentEventID**: an identifier that groups events
- **母事件識別碼**：數個採樣調查活動（事件）的群組識別碼。



- **samplingProtocol**: name, reference, description of method or protocol used during sampling event
- **取樣協定**：採樣調查活動（事件）的採樣方法的名稱、引用出處及方法或協定的描述。



- **sampleSizeValue**: numeric value for the size (duration, length, area or volume) of a sample in a sampling event. Must have a corresponding sampleSizeUnit
- **取樣大小數值**：採樣調查活動（事件）中樣本的大小數值（持續時間、長度、面積或體積）。必須要有對應的取樣大小單位。



- **sampleSizeUnit**: the unit of measure of the size (sampleSizeValue)
- **取樣大小單位**：測量數量的單位（取樣大小數值）。



- **organismQuantity**: a number for the quantity of organisms. Must have a corresponding organismQuantityType
- **個體數量**：個體數量的數值。必須有相對應的個體數量類型。



- **organismQuantityType**: the type of quantification system used for the quantity of organisms
- **個體數量類型**：表示個體數量所使用的量化系統。

 