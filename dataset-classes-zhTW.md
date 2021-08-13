https://www.gbif.org/zh-tw/dataset-classes

#### Document Control
| Date | Description | Author(s) |
| ---- | ----------- | --------- |
|      | 初譯        | 方品仁    |
| | 覆譯及審閱  | 柯智仁    |
| 2021-08-13 | 發布  | 柯智仁 |


# Dataset classes
資料集類別

The four classes of datasets supported by GBIF start simply and become progressively richer, more structured and more complex

GBIF 支援四種資料集，從簡單的程度漸進至更豐富、更具結構及更加複雜。

We encourage data holders to publish the richest data possible to ensure their use across a wider range of research approaches and questions, but not every dataset includes information at the same level of detail. Sharing what is available through GBIF.org is valuable, because even partial information answers some important questions.

即使每個資料集涵蓋的資訊有不同的詳細程度，我們仍鼓勵資料的擁有者們儘可能地發布最詳細的資料，以確保這些資料可以廣泛地應用在各種研究方法及議題。經由 GBIF.org 發布任何已有的資料均有其價值，因為即便是片段的資訊也能回答一些重要問題。


### Resources metadata
資源的詮釋資料

At its simplest level, GBIF.org allows institutions to create datasets describing undigitized resources like those in natural history and other collections. All three other dataset classes include this basic information, but this ‘metadata-only’ class offers researchers a valuable tool for discovering and learning about evidence not yet available online. They can also help assess the relative importance and value of undigitized collections and set priorities for future digitization. As with all datasets, GBIF ensures that each metadata dataset is associated with a unique Digital Object Identifier (DOI) to streamline data users’ citation of these resources.

[詮釋資料](http://terms.naer.edu.tw/detail/1679224/)（Metadata），又稱後設資料、元資料或元數據，提供原始資料的產生背景、取得方法、資料規格或聯絡人員等等描述資訊。

在此最簡單的程度，GBIF.org 接受各個機構建立資料集來敘述尚未數位化的自然史典藏或其他蒐藏。相較於其他三種，這類「純詮釋資料」讓研究人員知曉已存在但原始內容尚未發布的資料集，也能協助評估尚未數位化典藏相對的重要性及價值，以決定未來數位化的優先順序。如同所有的資料集，GBIF 確保每份資料都有一獨立的數位物件識別碼（Digital Object Identifier, DOI），以便利使用者引用這類資料。

- [瀏覽詮釋資料集](/dataset/search?type=METADATA)

### Checklist data
物種名錄資料

Datasets can also provide a catalogue or list of named organisms, or taxa. While they may include additional details like local species names or specimen citations, these ‘checklists’ typically categorize information along taxonomic, geographic, and thematic lines, or some combination of the three. For example, a dataset that catalogues the Red Listed molluscs of Seychelles has distinct elements of taxonomy (the phylum Mollusca), geography (the island nation of Seychelles) and theme (species deemed imperiled by IUCN experts). Checklists function as a rapid summary or baseline inventory of taxa in a given context.

資料集也可以提供一份已命名物種或分類群的目錄或清單。這些「名錄」資料通常以物種類群、地理分佈、主題或綜合上述三者來歸類，有時也會包含像是普通名或是引證標本的細節。例如，賽席爾共和國的軟體動物紅皮書資料集中，包含有分類（軟體動物門）、地理分布（賽席爾島國）、主題（物種由 IUCN 專家列為瀕危）。物種名錄可用於任何給定條件下分類群的快速摘要或基線清單。

- [瀏覽名錄資料集](/dataset/search?type=CHECKLIST)
- [物種名錄資料的達爾文核心集檔案範本](https://github.com/gbif/ipt/wiki/checklistData#templates)
- [物種名錄資料的資料品質要求](https://www.gbif.org/zh-tw/data-quality-requirements-checklists)

### Occurrence data

Other datasets published through GBIF.org have sufficiently consistent detail to contribute information about the location of individual organisms in time and space—that is, they offer evidence of the occurrence of a species (or other taxon) at a particular place on a specified date. Occurrence datasets make up the core of data published through GBIF.org, and examples can range from specimens and fossils in natural history collections, observations by field researchers and citizen scientists, and data gathered from camera traps or remote-sensing satellites.

有別於前述的資料集類別，以下的資料類別可提供關於生物的地點、時間資訊—也就是說，他們提供了某個或某些物種在特定的時間與地點出現的證據。GBIF.org 資料庫主要由物種出現紀錄資料集所構成，包括自然歷史博物館的館藏和化石標本、公民科學家與研究人員的野外調查數據、自動相機（註）及衛星遙測收集的資料等。

Occurrence records in these datasets sometimes provide only general locality information, sometimes simply identifying the country, but in many cases more precise locations and geographic coordinates support fine-scale analysis and mapping of species distributions.

物種出現紀錄資料有時只記錄籠統的地點資訊，或甚至只記載出現的國家。但多數情況下，正確的位置、地理座標資訊有助於細微尺度的研究分析和物種分布繪製。

- [瀏覽物種出現紀錄資料集](https://www.gbif.org/zh-tw/dataset/search?type=OCCURRENCE)
- [物種出現紀錄資料集的達爾文核心集檔案範本](https://github.com/gbif/ipt/wiki/occurrenceData#templates)
- [物種出現紀錄資料的資料品質要求](https://www.gbif.org/zh-tw/data-quality-requirements-occurrences)

註：自動相機指使用動作傳感器、紅外探測器或其他光束作為觸發機關的遙控相機。它常被用來拍攝攝影師不容易直接拍得的畫面，多運用在生態研究領域，例如監督狩獵、觀察野生動物、尋找稀有物種等。

### Sampling-event data

調查活動資料集

Datasets sometimes provide greater detail, not only offering evidence that a species occurred at a given location and date, but also making it possible to assess community composition for broader taxonomic groups or even the abundance of species at multiple times and places. These quantitative or sampling-event datasets typically derive from standard protocols for measuring and monitoring biodiversity like vegetation transects, bird censuses and freshwater or marine sampling.

資料集有時可以提供相當詳細的內容，不僅紀錄物種出現的地點及時間，更能加以評估廣泛的物種群聚組成，甚至是許多不同時間及地點的物種豐度。這些量化的、調查活動資料來自測量或監測生物多樣性的典型標準程序，例如：植被樣區調查、鳥類普查以及淡水或海洋的採樣資料。

By indicating the methods, events and relative abundance of species recorded in a sample, these datasets improve comparisons with data collected using the same protocols at different times and places—in some cases, even leading researchers to infer the absence of particular species from particular sites.

藉由說明採集方法、調查活動過程與紀錄物種相對豐度，此類資料集改善了研究者使用一致的方法協定在不同地點、時間的對照—在某些案例中，甚至能導引研究者推斷在特定區域不再出現的物種。

- [調查活動資料介紹](https://www.gbif.org/zh-tw/sampling-event-data)
- [瀏覽調查活動資料集](https://www.gbif.org/zh-tw/dataset/search?type=SAMPLING_EVENT)
- [調查活動資料集的達爾文核心集範本](https://github.com/gbif/ipt/wiki/samplingEventData#templates)
- [調查活動資料集的資料品質要求](https://www.gbif.org/zh-tw/data-quality-requirements-sampling-events)