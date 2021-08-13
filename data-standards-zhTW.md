https://www.gbif.org/zh-tw/standards

#### Document Control
| Date | Description | Author(s) |
| ---- | ----------- | --------- |
|      | 初譯        | 方品仁    |
| | 覆譯及審閱  | 柯智仁    |
| 2021-08-13 | 發布  | 柯智仁 |

#### Keywords

standard, standards, dwc, darwin core, darwin

標準, 達爾文核心集, 達爾文

# Data standards

資料標準

Shared data standards are the main enabler for bringing together the hundreds of millions of primary biodiversity records in the GBIF index.
共享的資料標準，使得推動彙整 GBIF 索引中數以億計的基礎生物多樣性資料成為可能。

The data available through GBIF.org and its associated services is the result of the GBIF network of Participants and publishers applying shared rules and conventions to describe, recording and structure thousands of different datasets drawn from hundreds of institutions around the world. Common standards are the main enabler for bringing together the hundreds of millions of primary biodiversity records in the GBIF index.

透過 GBIF.org 及其附屬服務公開的資料，都是 GBIF 會員網絡和資料發布者們經由共享的規則及慣例，從世界各地數以百計的機構獲取數以千計的資料集加以描述、紀錄、建構而成。而共享的資料標準，使得推動彙整 GBIF 索引中數以億計的基礎生物多樣性資料成為可能。

Within the biodiversity domain, the group most often responsible for developing and maintaining data standards is [Biodiversity Information Standards](http://www.tdwg.org). As an affiliate of the [International Union of Biological Science](http://www.iubs.org/), this nonprofit scientific and educational association focuses on the development of standards for the exchange of biological and biodiversity data. Members of the biodiversity community generally refer to this group as **TDWG** (pronounced *tad-wig*)—a vestigial reminder of its earlier manifestation as the Taxonomic Databases Working Group.

在生物多樣性的領域，主要負責開發及維護資料標準的是[生物多樣性資訊標準]()組織。作為[國際生命科學聯盟](http://www.iubs.org/)的附屬機構，該非營利的科學及教育協會專注於開發生物及生物多樣性資料的交換標準。生物多樣性的社群成員一般將此組織稱為**TDWG**（音同 Tad-Wigs），因其前身為分類學資料庫工作小組（Taxonomic Databases Working Group）。



## Commonly used standards

經常使用的標準規範

### Darwin Core

達爾文核心集

The Darwin Core Standard (DwC) offers a stable, straightforward and flexible framework for compiling biodiversity data from varied and variable sources. The majority of the datasets shared through GBIF.org are published using the Darwin Core Archive format (DwC-A).   

達爾文核心集標準（Darwin Core Standard, DwC）提供一個穩定、直觀及可塑的框架來編譯不同、多變來源的生物多樣性資料。絕大多數由 GBIF.org 分享的資料集都是以達爾文核心集檔案格式（Darwin Core Archive format, DwC-A）發布。

+ [What is Darwin Core, and why does it matter?](/darwin-core)
+ 什麼是達爾文核心集？它為何重要?
+ [Introduction to sampling-event data](/sampling-event-data)
+ 調查活動資料集簡介
+ [iOBIS Darwin Core manual](http://www.iobis.org/manual/darwincore/)
+ 達爾文核心集手冊
+ [Darwin Core terms](https://gcube.wiki.gcube-system.org/gcube/Darwin_Core_Terms) (via Gcube Wiki)
+ 達爾文核心集詞彙（透過 Gcube Wiki）



### EML: Ecological Metadata Language

生態詮釋資料語言

Ecological Metadata Language, or **EML**, is a metadata standard that records information about ecological datasets in a series of modular and extensible XML document types. All of the descriptions of datasets in GBIF.org rely on ‘metadata’—that is, the information about data—using the open-source EML standard, which is administered and maintained by [The Knowledge Network for Biocomplexity](https://knb.ecoinformatics.org). Each Darwin Core Archive includes as one of its components an EML file (written in XML format). 

生態詮釋資料語言（Ecological Metadata Language, **EML**），是一種詮釋資料規範。它使用一系列模組化、可擴展的 XML 文件類型來記錄生態資料集的資訊。GBIF.org 所有資料集的描述都依賴詮釋資料；也就是說，關於資料的資訊都使用此開源 EML 標準—它是由[生物複雜性知識網絡](https://knb.ecoinformatics.org)所管理及維護。每個達爾文核心集資料檔案的組成部件中都包含一個 EML 文件（以XML 格式撰寫）。

+ [GBIF Metadata Profile: How-to Guide](https://github.com/gbif/ipt/wiki/GMPHowToGuide)
+ GBIF 詮釋資料說明：導引手冊
+ [EML standard](https://knb.ecoinformatics.org/#external//emlparser/docs/index.html)
+ EML 標準



### BioCASe / ABCD

The [Biological Collection Access Service](http://www.biocase.org), commonly referred to as **BioCASe**, is an international network linking biological collections data from natural history museums, botanical/zoological gardens and research institutions. BioCASe relies on the [Access to Biological Collections Data (ABCD) data exchange standard](https://abcd.tdwg.org/), which TDWG also administers.

[生物典藏存取服務](http://www.biocase.org)（Biological Collection Access Service），又稱 **BioCASe**，是一個連結國際間自然史典藏、動植物園、研究機構所有生物典藏資料的網絡。BioCASe 仰賴[生物典藏資料取用交換標準](https://abcd.tdwg.org/)（Access to Biological Collections Data, ABCD），亦是由 TDWG 所管理。

+ [BioCASe Protocol](http://www.biocase.org/products/protocols)
+ BioCASe 協定
+ [User access of BioCASe data through GBIF.org](http://www.biocase.org/whats_biocase/gbif_downloads.cgi?view=2)
+ 透過 GBIF.org 取用 BioCASe 所發布資料的統計 
