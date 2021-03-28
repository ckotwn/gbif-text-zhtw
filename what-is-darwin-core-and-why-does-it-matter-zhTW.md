#### Document Control
| Date | Description | Author(s) |
| ---- | ----------- | --------- |
|      | 初譯        | 方品仁    |
|      | 覆譯及審閱  | 柯智仁    |
|      | 發布        |           |



What is Darwin Core, and why does it matter?

什麼是達爾文核心集，其重要性為何?

*The Darwin Core Standard (DwC) offers a stable, straightforward and flexible framework for compiling biodiversity data from varied and variable sources.*

*達爾文核心集規範提供一個穩定，直觀且可塑的資料框架，編譯來源眾多的生物多樣性資料。*

[*Platyspiza crassirostris*](https://www.gbif.org/occurrence/899939168) by Brian Gratwicke licensed under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/).

 

Natural history collections, environmental monitoring programmes, recording societies, citizen scientist projects and others all hold valuable data on the world’s biodiversity. They collect and manage their information in many different systems and environments, and vary widely, depending on what kind of details are captured and stored for any individual record.

自然歷史博物館藏、環境監測計畫、紀錄協會、公民科學家專案等都保有珍貴的世界生物多樣性資料。它們從各個不同的系統、不同的環境收集資料並管理，

So how can we integrate these diverse datasets most simply and efficiently so scientists, analysts and policymakers can use them in research and policy?

我們如何簡易、有效率地整合這些多元的資料集，讓科學家、資料分析者、政策制定者可以運用在研究及政策呢?

The [Darwin Core Standard (DwC)](http://rs.tdwg.org/dwc) offers a stable, straightforward and flexible framework for compiling biodiversity data from varied and variable sources. 

Originally developed by the [Biodiversity Information Standards (TDWG) community](http://www.tdwg.org/), Darwin Core is '[an evolving community-developed biodiversity data standard](http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0029715). It plays fundamental role in the sharing, use and reuse of open-access biodiversity data and today accounts for vast majority of the hundreds of millions of species occurrence records available through GBIF.org.

達爾文核心集規範(Darwin Core Standard (DwC))提供一個穩固、直觀、可塑的框架來編譯這些來源複雜的生物多樣性資料集。同時，達爾文核心集規範也是一個不斷演進的社群開發生物多樣性資料規範，最初由生物多樣性資訊規範社群(Biodiversity Information Standards Community)發展而來。在開源多樣性資料的共享、使用、再利用方面都扮演重要的核心角色，佔了GBIF.org所收錄生物出現紀錄資料很大部分。

In practice, using Darwin Core revolves around a standard file format, the Darwin Core Archive (DwC-A). This compact package (a ZIP file) contains interconnected text files and enables data publishers to share their data using a common terminology. This standardization not only simplifies the process of publishing biodiversity datasets, it also makes it easy for users to discover, search, evaluate and compare datasets as they seek answers to today’s data-intensive research and policy questions.

實務上，達爾文核心集就是使用一套標準檔案格式，也就是達爾文核心檔案集(Darwin Core Archive (DwC-A))。達爾文核心檔案壓縮檔(ZIP)包含互聯的文件檔，使得發佈者們有共同的科學用語。這樣的標準規範不僅簡化了發佈資料集的流程，當使用者在尋找資料密集型研究與政策問題的答案時，更容易探索、搜尋、評估和比較資料集。

Additional resources 額外來源

- Wieczorek J, Bloom D, Guralnick R, Blum S,     Döring M, Giovanni R, et al. (2012) Darwin Core: An Evolving     Community-Developed Biodiversity Data Standard. PLoS ONE 7(1):     e29715. [doi:10.1371/journal.pone.0029715](https://doi.org/10.1371/journal.pone.0029715).
- [iOBIS Darwin Core manual](http://www.iobis.org/manual/darwincore/) IOBIS 達爾文核心手冊
- [Darwin Core terms](https://gcube.wiki.gcube-system.org/gcube/Darwin_Core_Terms) (via Gcube Wiki)達爾文核心專有名詞(Gcube維基)

What’s in an archive? 歸檔包含什麼

When preparing a Darwin Core Archive version from their source data, publishers restructure and streamline information into a small but structured collection of text files. One of these files is the ‘core’ file and holds a separate record for each of the items included in the archive. Other ‘extension’ files may also be included. These contain additional information linked to the records in the core file. Extension files allow the archive to model many-to-one relationships.

資料發佈者依據來源資料準備達爾文核心歸檔集時，要將資訊重組串流成小型結構化的數個文件檔。其中一個檔案是核心檔，核心歸檔集內各項目紀錄都被保存在此，也包括其餘的擴充文件檔。這些擴充檔包含可以連結到核心集的資訊，也允許歸檔集建立多對一的連結。

Depending on how much information the source data contains—and how much they wish to share—publishers can create a Darwin Core Archive with one of three cores:

發佈者可以在以下3個達爾文核心歸檔集裡面自行創建檔案。取決於資料來源包含的資訊量，以及發佈者願意共享的內容。

- a Taxon core, which lists a set of     species, typically coming from the same region or sharing common     characteristics
- 分類核心集，列出同一個區域或者有相同外型特徵的物種清單。
- an Occurrence core, which lists a set of     times and locations at which particular species have been recorded.
- 出現紀錄核心集，紀錄特定物種出現的時間及地點。
- an Event core, which lists field studies     (including the protocols used, the sample size, and the location for     each).
- 事件核心集，紀錄田野調查資訊(包含調查程序，採樣數量，採集地點)

In the case of an Event core, one extension file usually contains the elements displayed in an Occurrence core, which enables the inclusion of many observation records as part of a single planned field study.

在事件核心集的情況，擴充文件會涵蓋數個出現紀錄核心集，使得包含數個觀察紀錄可作為單一田野調查的一部分。

Finally, each archive contains two more pieces that help both machines and humans interpreting the data. The first, a descriptor file (meta.xml), defines the precise structure and relationships between the core and any extensions. The second, a complementary metadata file, describes the datasets contained in the archive, typically in Ecological Metadata Language (EML.xml)—though the GBIF’s [Integrated Publishing Toolkit](https://www.gbif.org/ipt) produces these files automatically for its users.

最後每一個歸檔會包含2個或2個以上的部分來協助機器及人整合資料。第一部分為敘述檔(meta.xml)，用來定義核心集和擴充文件之間精確的結構關係。第二部分為附加元資料檔，用來敘述歸檔集所包含的資料集，通常是生態元資料語言Ecological Metadata Language (EML.xml)，不過GBIF的整合發佈套件會自動替使用者產生這些檔案。

Sharing species monitoring and sampling data with the Event Core 由事件核心集共享物種監測和採樣資料

Efforts to track shifts in biodiversity patterns over space and time have increased the amount of species information available through sampling and monitoring programmes. In addition to having more precisely described methods than ‘presence-only’ data, these sample-based datasets capture richer, more complex details about species quantities and frequency.

透過採樣與監測計畫來追蹤生物多樣性在空間與時間上的變化模式，大幅增加了物種資訊量。根據採樣所紀錄的資料集除了精確描述方法，內容也詳細記載物種的數量及頻度，而不是只有物種出現紀錄資料。

With their frequent inclusion of repeated measurements from the same places, sampling-event data from ecological and environmental investigations are better at detecting shifts and trends in species populations—and critical to understanding the scope and speed of global change.

透過相同地點的多次採樣，生態及環境監測的採樣資料更適合用於偵測生物族群的變動趨勢，也是我們理解全球變遷範圍和速度的關鍵。

But to help make the most of these diverse data and ensure their efficient contribution to more precise scientific analyses and policy outcomes, researchers need easy access to them in a consistent, compatible format.

為了充分利用這些多元的資料，並確保它們在精確的科學研究及政策上能有效地貢獻，研究者需要有一個簡易的管道來取得這些格式一致且相容的資料。

The Darwin Core Standard has become the most widely used open-access standard for biodiversity data. Developed to provide a simple way to document and share information about species occurrences, whether in the field or in a museum collection, the standard has made it possible to integrate hundreds of millions of records through GBIF.org.

達爾文核心集規範已經被廣泛使用在開源生物多樣性資料。不論在田野調查或博物館館藏，此規範都提供了相當簡易的方法來記載或共享物種出現紀錄，也實現了GBIF.org整合數以萬計筆資料的可能。

Recent additions to Darwin Core detailed below support the aggregation of sampling-event datasets. The newly introduced ‘Event core’ places the sampling event at the center of the simplified dataset and links its protocol, effort and measurements to the species occurrences derived from the sampling events, which are appended as a separate extension in the standard’s one-to-many star schema.

以下詳細介紹達爾文核心集的新增內容，可支援採樣資料資料集的匯整。新導入的「事件核心集」將採樣事件設置於簡化資料集中心，並連結採樣程序、工作量、測量

As a result, researchers can now tap into more complex, quantitatively richer records for analyses and combine them alongside others focused on single organisms or individual taxa. These changes could even lead to improvements in the quality and usefulness of datasets already published on GBIF.org that derive from more complex surveys and censuses.

因此，研究人員現在可以利用更複雜，數量更豐富的記錄資料，結合單一生物個體或個體分類群的記錄來分析。這次內容的改變甚至提升了原本已經發佈在GBIF.org資料庫裡複雜的調查、普查資料集之品質和實用性。

The hope is that mingling these varied sources of data will, rather than limiting or prescribing their uses, encourage their discovery and reuse—and perhaps even reveal higher-level relationships and insights that would not be apparent from examining individual records.

 

目的主要是希望可以融會不同來源的資料，提倡發掘資料與利用資料，而非限制或規定它們的用途。甚至可能發現找出在記錄中，資料之間更高層次的關係與見解。

How to get started 如何開始

The most efficient way to prepare and publish Darwin Core-based datasets is through GBIF’s [Integrated Publishing Toolkit](https://www.gbif.org/ipt). [EU BON](http://www.eubon.eu/) and other partners provided vital contributions toward the changes needed to support this new class of datasets. Data holders with ongoing monitoring programmes and sampling projects can also configure automatically scheduled publishing cycles on the multilingual-friendly IPT.

最具效率的方法就是透過GBIF網站的整合發佈套件(Integrated Publishing Toolkit, IPT)。歐洲生物多樣性觀察網(EU BON)和其他的合作夥伴對於支持這新資料集類別所需的轉變有重要的貢獻。支援多國語言介面的整合發佈套件，可以讓資料擁有者在持續監測計畫和採樣計畫進行下，透過套件設定資料自動發佈週期。

What’s new in the DwC-A event core

事件核心集新增那些內容

The addition of the ‘event core’ to the Darwin Core Standard includes several new terms highly applicable to sample-based and monitoring data.

在達爾文核心規範中的「事件核心集」新增了一些適用於採樣和監測資料的專有名詞。

- **eventID**: an     identifier specific for the event in a dataset
- **採樣事件****ID:** **用來辨別資料集裡的每個採樣調查**
-  
- **parentEventID**: an     identifier that groups events
- **母事件辨識碼****:****數個採樣調查的同屬辨識碼。**
-  
- **samplingProtocol**: name, reference, description of method or protocol     used during sampling event
- **採樣程序****:****採樣方法的名稱、引文出處、描述，或採樣程序。**
-  
- **sampleSizeValue**: numeric value for the size (duration, length, area     or volume) of a sample in a sampling event. Must have a corresponding     sampleSizeUnit
- 採樣數量值:關於採樣事件的相關數值(採樣持續過程、時間長短、地區、體積)。必須要有對應的採樣數量單位。
-  
- **sampleSizeUnit**: the unit     of measure of the size (sampleSizeValue)
- 採樣數量單位:紀錄樣本數量的單位
-  
- **organismQuantity**: a number for the quantity of organisms. Must have     a corresponding organismQuantityType
- 採集個體數量:紀錄個體數量的值。必須有相對應的個體數量形式。
-  
- **organismQuantityType**: the type of quantification system used for the     quantity of organisms
- **個體數量形式****:****紀錄採集個體數量的量化形式**

 