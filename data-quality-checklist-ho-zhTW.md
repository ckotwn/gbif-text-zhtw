https://www.gbif.org/zh-tw/data-quality-requirements-checklists

#### Document Control
| Date | Description | Author(s) |
| ---- | ----------- | --------- |
|      | 初譯        | 何宣慶    |
|      | 覆譯及審閱  | 柯智仁    |
|      | 發布  | 柯智仁   |

#### Found issues


# Data quality requirements: Checklist datasets
# 資料品質需求：名錄資料集

By following these data quality requirements and recommendations, data publishers can improve the quality, completeness and value of their checklist datasets.
依循這些資料品質的需求及建議，資料發布者可以改善其名錄資料集的品質、完整性及價值。

Checklist datasets provide a catalogue, rapid summary or baseline inventory a set of named organisms, or taxa. While they may include additional details like local species names or specimen citations, checklists typically categorize information along taxonomic, geographic, and thematic lines, or some combination of the three.
By following these data quality requirements and recommendations, data publishers can improve the quality, completeness and value of their checklist datasets.

名錄資料集提供一組已鑑定生物或分類單元（註）的目錄、摘要或基線清單。名錄通常依照分類學、地理、主題（如瀕危等級）或此三者中的組合來進行資訊的分類，同時可能包含其他細節如當地物種普通名或標本佐證。依循這些資料品質的需求及建議，資料發布者可以改善他們名錄資料集的品質、完整性及價值。

註：分類單位；分類群（taxon，複數 taxa）為演化上親緣關係接近的同系群體，可以指涉種、亞種或者種以上位階。

## Darwin Core records 
## 達爾文核心集紀錄

欄位名稱	填寫指示
taxonID（分類單位識別碼） 必填
scientificName（學名） 必填
taxonRank（分類單位位階） 必填
kingdom（界）強烈建議填寫
parentNameUsageID（母學名用法編號） 強烈建議填寫
acceptedNameUsageID（接受學名用法編號） 強烈建議填寫
vernacularName（普通名） 有則分享

## Dataset metadata (EML)
## 資料集詮釋資料（EML）

欄位名稱	填寫指示
title（資料集名稱）必填
description（基本描述）必填
publishing organization（發布組織） 必填
type（資料類型） 必填
license（資料使用授權） 必填
contact(s)（聯絡資訊） 必填
creator(s)（創建者） 必填
metadata provider(s)（詮釋資料提供者） 必填
citation（引用條目） 強烈建議填寫

Note: If the dataset is funded through a programme operated by GBIF (e.g. BID, BIFA, CESP), two additional fields are required:
注意：若一資料集為 GBIF 下的計畫所資助（例如：BID, BIFA, CESP），則必須額外填寫以下兩個欄位：
	
projectID (計畫編號) 必填
projectTitle (計畫名稱) 必填

## Status
## 填寫指示說明

### Required information
### 必填
The items listed below constitute the minimum formal requirements for publishing [an occurrence dataset](https://github.com/gbif/portal-feedback/issues/3545). GBIF.org will not accept a dataset without these terms and will not index the records. While these items are mandatory for publishing the dataset at all, they are only the starting point. The usefulness of the published data will still be severely limited unless additional information is supplied.




下方所列為正式發表名錄資料集必須之最少欄位項目。GBIF.org 不會接受缺少這些欄位元素的資料集，也不會索引其中的紀錄。雖然這些欄位是發布資料必備，但這僅只是開始而已。除非再提供更多額外欄位資料，僅滿足必填欄位的發布資料仍會有很多使用上的限制。

### Strongly recommended
### 強烈建議填寫
In addition to the mandatory data elements, we strongly recommend completing several more fields that help improve the usefulness of the dataset because: 

除了必填的資料元素以外，我們也強烈建議完成一些欄位以協助改善資料集的用處。理由是：

- some information supports the integration into a global data resource and prevents ambiguity, e.g. in matching scientific names that could apply to more than one organism (homonyms) to the correct place within the backbone taxonomy
- 有些資訊會協助匯集到全球的資料來源並避免模稜兩可的情況，例如將可能被用在超過一個物種的學名（即異物同名）放在骨幹分類架構中正確的位置。

- more precise geo-location data (coordinates) significantly increase the usefulness of the data for a wide range of use cases
- 越精確的地理位置資訊（經緯度）越可以有效地增加資料被其他案例廣泛使用的可能性。

- additional qualifiers for some data elements, e.g. coordinates, support the interpretation of those elements and help users to better estimate their usefulness for a given data use case 
- 資料元素的額外修飾子（例如經緯度相對於地點），在資料元素外進一步支援資料解讀，讓使用者能更容易地評估資料集的可用性。

- some data redundancy supports quality control and error detection (e.g. testing country codes against coordinates where both are supplied) 
- 一些額外的資訊可以支援資料品質控管以及錯誤偵測（例如，若兩者同時提供的話，國碼可用來驗證經緯度）。

- [last but not least](https://github.com/gbif/portal-feedback/issues/3546), the richer the spectrum of available information of a dataset is, the more potential usage areas it becomes available for, meaning the dataset will be more widely accessible and used and cited more often
- 列在最後但一樣重要的是，資料集的公開資訊範圍越豐富，就越有可能用在更多的地方，這也表示該資料集會將能得到更廣泛的取得和使用，當然也就會有更多的引用。


### Share if available
### 有則分享
If additional data are available, consider sharing them in order to increase the usefulness of your published data.
若有更多額外的資料，請考慮盡量分享這些資訊，以提高發表資料的可用性。

### Terms 
### 詞彙（欄位元素）

taxonID
物種識別碼 taxonID
Darwin Core dataset element, REQUIRED for checklist datasets
達爾文核心集資料元素，在名錄資料集為**必填**

A unique identifier for the taxon, allowing the same taxon to be recognized across dataset versions as well as through data downloads and use (see Darwin Core Terms: A quick reference guide
此欄位為一分類群獨一無二的識別碼，可讓同一個分類群在不同的資料集版本以及透過下載和使用的資料中辨認出來（參閱[達爾文核心集詞彙：快速參考指南](http://rs.tdwg.org/dwc/terms/taxonID)）。

Ideally, the taxonID is a persistent global unique identifier. As a minimum requirement, it has to be unique within the published dataset. It allows to recognize the same set of taxon information over time when the dataset indexing is refreshed; it links additional data like images or occurrence records; and it makes it possible to cite records e.g. in usage reports or in publications. This means that the taxonID needs to reliably stay with the taxon information at source, and to consistently refer to the same set of taxon information in published datasets and any underlying source data.
理想上，物種識別碼為一個全球獨一無二的識別碼；最低的要求則是在發布的資料集本身其有唯一性。如此隨著修訂每次針對資料集製作索引時才可以追蹤所包含的分類群資訊；它可以連結其他額外的訊息，如影像及出現紀錄；並且使人可以引用紀錄，例如，資料使用報告或學術發表。這代表物種識別碼需要可靠地連結來源的分類群內容，並且總是在同一個發布的資料集及其來源資料中指向同一組分類群資訊。


scientificName
學名 scientificName
Darwin Core dataset element, REQUIRED for checklist datasets
達爾文核心集資料元素，在名錄資料集為**必填**

The full scientific name, including authorship and year of the name where applicable. In the context of a checklist, the scientific name is the core data element of a taxon list or hierarchy that the dataset is set out to collate and publish (see Darwin Core Terms: A quick reference guide)

此欄位為一完整的學名，包含其作者及發表年代。在名錄中，學名為準備整理及發表分類群列表或階層的核心資料元素（參閱[達爾文核心集詞彙：快速參考指南](http://rs.tdwg.org/dwc/terms/scientificName)）。

Depending on the purpose of the checklist, scientific names may be of any hierarchical level, though typically would be of species rank or below for, e.g., regional floristic or faunistic checklists, Red List collations, or thematic inventories like marine organisms or taxonomic revisions of species groups. If the checklist is intended to publish a hierarchy (tree-like structure), add separate entries for the relevant upper taxonomic ranks, e.g. kingdom, class and family, and link them into a hierarchical structure using the parentNameUsageID (see below) to support unambiguous interpretation of the checklist entries.

依照名錄的需求，學名可以是任何分類階層，通常會是種級或是種級以下，例如地區性的植物相或動物相名錄、紅皮書，亦或者是海洋生物或是特定物種群的分類修訂。若要發布一個包含階層資訊的名錄（分類的樹狀結構），可以在資料集中加入一些相對高階的分類群紀錄（例如界、綱、科），再藉由母學名用法編號（parentNameUsageID）欄位連結成一階層架構（見下方說明），以清楚解讀名錄紀錄。

Valid scientific names are Latin names following the syntax rules of the respective taxon group (e.g. botanical nomenclature). Not permitted are, [i.a.](), working names (“Mallomonas sp.4”), common names (“fruit fly”), or names containing identification qualifiers (“Anemone cf. nemorosa”). If common names are used, they should be supplied in addition to the scientific names, using the VernacularName set of [fields]()(see below).

有效的學名為遵循依不同分類群語法規範的拉丁文名字（例如植物命名法規）。不可以使用臨時名稱（像是 Mallomonas sp.4）、普通名（例如 fruit fly）或是含有鑑定狀態的名稱（例如 Anemone cf. nemorosa）。如要使用普通名（俗名）則只能當成學名的補充，可以使用普通名（VernacularName）的相關欄位（見下方說明）。

taxonRank
分類階層（taxonRank）
Darwin Core dataset element, REQUIRED for checklist datasets
達爾文核心集資料元素，在名錄資料集為**必填**

The taxonomic rank of the supplied scientific name (see Darwin Core Terms: A quick reference guide
用以表示所提供學名的分類層級（參閱[達爾文核心集詞彙：快速參考指南](http://rs.tdwg.org/dwc/terms/taxonRank)）。

The taxon rank supports the interpretation of the scientific name during indexing, and supports matching the checklist records to the core taxonomy, especially in the case of names at genus level or above (monomials). While the format of higher taxon names in some groups contains indicators of their rank, this is not consistent across or even within groups, and cannot be reliably used for interpretation. For placing names correctly, explicitly specifying the taxon rank, alongside information on the higher taxonomy, is an important criterion. For practical purposes, the ranks used have to be (major) Linnean ranks: kingdom, phylum, class, order, family, genus, species. Both Latin or English terms are accepted.

分類階層在製作索引時用來解讀學名，以及核對核心分類學中的名錄紀錄，尤其是屬級或更高的層級的學名（單名）。雖然有些高階分類群的學名已經指出分類階層，但這在群體間甚至群體內部不一定一致，故無法（由索引程序）用來解讀。為使學名可以正確地歸位，在高階分類資訊中明確指出其分類階層實為必要。實務上，分類階層必須依循林奈系統的（主要）層級：kingdom（界）、phylum（門）、class（綱）、order目）、family（科）、genus（屬）、speciea（種）。此處使用拉丁文或英文的用法均可。


kingdom
界（kingdom）
Darwin Core dataset element, STRONGLY RECOMMENDED for checklist datasets
達爾文資料集核心元素, 在名錄資料集為**強烈建議填寫**

The full scientific name specifying the kingdom that the scientific name is classified under (see Darwin Core Terms: A quick reference guide and other higher taxonomy, if possible)

完整的學名加上這個學名所屬的界級分類（參閱[達爾文核心集詞彙：快速參考指南](http://rs.tdwg.org/dwc/terms/kingdom)或者其他高階分類，若有的話）。

With scientific names, there are numerous cases where the matching of a given name against the core taxonomy is unsure or ambiguous. This is the case, for example, with homonyms (identical names exist for different organisms, usually across groups), newly described names that are not yet part of the existing taxonomic tree, or spelling variants (typos, hyphenation etc). To support exact matching of a scientific name against the core taxonomy, additional names at higher ranks help interpretation and error prevention. For datasets where the hierarchical representation in the published data is not important, higher level names can be supplied as part of the record itself by adding the relevant DarwinCore fields, similar to occurrence datasets.

如果只有學名，在很多例子中對應到核心分類學的結果是不確定或模稜兩可的。例如，異物同名（是不同的類群中不一樣的生物，有完全一樣的學名）、有些剛描述的學名尚未列在現有的分類樹中，或是拼法的變異（錯字或斷字因素等)。為了能正確對應到核心分類學，加入更高階層的學名可以協助解讀並防止錯誤。對於已發布的資料集來說，若呈現資料中的階層結構不是最重要，高階層的學名則可以藉由添加達爾文核心集中相關的欄位成為紀錄本身的一部分，類似於物種出現紀錄資料集。

Names should be scientific (latin) names at major Linnean ranks, like “Animalia” (kingdom) or “Rosaceae” (family). Not: common names (“animals”), abbreviations (“Rosac.”), intermediate rank levels (“Tetrapoda” (superclass)), or polyphyletic or non-taxonomic groupings (“algae”, “herbivora”).

學名必須是拉丁文，置於林奈系統的主要層級之下，像是「Animalia（界）」或「Rosaceae（科）」。不可以是：俗名（「animals」），縮寫（「Rosac.」），中間階層（「Tetrapoda」（超綱）），多系群或是非分類學的分群（「algae（藻類）」、「herbivora（草食性動物）」）。

parentNameUsageID
母學名用法編號（parentNameUsageID）

Darwin Core dataset element, STRONGLY RECOMMENDED for checklist datasets
達爾文資料集核心元素, 在名錄資料集為**強烈建議填寫**

The taxonID of the next available higher-ranked (parent) entry within the checklist dataset, if higher taxon names are supplied as separate entries in the list. See http://rs.tdwg.org/dwc/terms/parentNameUsageID.
This supports the representation of the dataset as a hierarchy, e.g. for the publication of a taxonomy.
名錄資料集中較分類單元直接高一層級的名稱的物種編碼(taxonID)，前提為這個較分類單元高一層級的名稱在列表中為分開輸入。參閱http://rs.tdwg.org/dwc/terms/parentNameUsageID.

    這個編碼可以成為資料集中的階層(hierarchy)代表，亦即用於分類學的出版品。
說明:如果資料集中有輸入學名、屬名及科名等，則屬名的編碼為學名編碼的父名編碼，科名的編碼為屬名的父名編碼。依此類推，可以有效建立分類層級。
[我覺得我的解釋比較好…]

acceptedNameUsageID
接受名稱編碼(acceptedNameUsageID)
Darwin Core dataset element, STRONGLY RECOMMENDED for checklist datasets
達爾維核心資料集元素，名錄型資料強烈建議提供。

Within the record of a synonym, the taxonID of the accepted taxon name entry within the checklist dataset, if both synonyms and accepted names are supplied. See http://rs.tdwg.org/dwc/terms/acceptedNameUsageID
This supports the representation of synonymy for a taxonomic dataset.

假使一名錄型資料集中有提供被接受名及異名，則該異名(synonym)的這個欄位編碼，應為名錄中被接受的分類單元名稱的編碼(taxonID)。見http://rs.tdwg.org/dwc/terms/acceptedNameUsageID 這可以支應一個分類資料集的異名錄的代表性。
說明:因為異名為無效名，所以一定有一個相對應的有效名(被接受名)，故在這一個欄位中填入該有效名作為連結。A種的欄位若填入B的編碼，則表示A為B之次異名。

vernacularName
俗名(vernacularName)
Darwin Core dataset element, SHARE IF AVAILABLE for checklist datasets
達爾維核心資料集元素，名錄型資料盡可能提供。

See http://rs.gbif.org/extension/gbif/1.0/vernacularname.xml. When supplied, also add at least the language of the name, using ISO 639-1 language codes

參照http://rs.gbif.org/extension/gbif/1.0/vernacularname.xml.
若有，也請至少提供名稱所使用哪個國家的語言，可參照ISO 639-1 language codes

title
標題(title)
Dataset metadata EML, REQUIRED for checklist datasets
資料集元資料生態模式語言，名錄型資料為必填。

The title under which the dataset will be published at gbif.org.
每個資料集的標題都會發布在gbif.org網站。

Recommendation: a brief, but descriptive title that characterizes the dataset in an international context and distinguishes it from similar datasets in other institutions. E.g. “Four new generic and 14 new specific synonymies in Pholcidae, and transfer of Pholcoides Roewer to Filistatidae (Araneae)”. Not recommended: “Araneae (Part 1) part.”. The title will, i.a., be part of the dataset citation on use of the data.
建議事項:一段簡短、可以指出資料集的國際背景以及與其他研究單位的資料及區分的描述性文字。例如“Four new generic and 14 new specific synonymies in Pholcidae, and transfer of Pholcoides Roewer to Filistatidae (Araneae)”。不建議使用“Araneae (Part 1) part”。 這表示標題最後會變成資料集引用文獻的標題。
說明:標題盡量避免過於簡短或不容易判斷出處或造成重複。最好明確指出地點、分類群及簡短內容。

description
基本描述(description)
Dataset metadata EML, REQUIRED for checklist datasets
資料集元資料生態模式語言，名錄型資料為必填。

An English language text, describing the dataset.
一段用英文描述資料集內容的文字。
This may include a longer version of title, a description of geographic, temporal and taxonomic scope of the checklist, methodology and purpose of the underlying data compilation (e.g. red list, invasive species, freshwater taxa, regional flora), relevant literature references, and any other information you consider relevant to characterize the dataset. A second version of the description in another language than English may be added underneath.
可以是較長版本的標題，敘明名錄之地理區、溫度及分類範疇、研究方法及目的(例如紅皮書、外來種、淡水物種、地區性植物)、適當的參考文獻或者您認為符合資料集特性的其他資訊。另外一個以英語以外的語言的描述也可置於英語基本描述下方。

publishing organization
發布單位(publishing organization)
Dataset metadata EML, REQUIRED for checklist datasets
資料集元資料生態模式語言，名錄型資料為必填。

The title of the institution or organization that will be listed as the data publisher at gbif.org. 
研究所或組織的名稱在gbif.org中將被列為資料發布者。
The publishing organization is the institution which holds or owns the dataset and is in charge of its contents and maintenance. The title given should be the official title of the organization as registered with relevant authorities, listed on websites, and, if applicable, as stated in the project contract.
發布資料的組織為持有或擁有資料集且負責資料內容及維護的研究所。名稱應為已在相關機構註冊、在網站上明列的組織正式名稱，抑或是計畫合約中所提及之名稱。

type
資料集類別(type)
Dataset metadata EML, REQUIRED for checklist datasets
資料集元資料生態模式語言，名錄型資料為必填。
The type of the dataset. Here: “checklist”.
這邊應該要填入的類別為”名錄(Checklist)”。
The record type describes the main focus of all records contained in the dataset (core records). For a checklist dataset, the record type will always be “checklist”. There may also be occurrences linked to checklist records (e.g. vouchers of a taxonomic treatment, herbarium records documenting a regional flora). The structure and requirements for this linked information follows the guidelines given for occurrence data publication [link].
資料的類別表示資料集中所有紀錄的主要焦點(核心紀錄)。對於名錄型資料，紀錄的類別一定是”checklist”。也有可能是名錄紀錄所連結的出現資料(例如，分類研究的證物標本或紀錄一個地區植物相的博物館記錄)。這個連結的資訊應該依照出現資料發布的指引[link]。

license
許可證照(license)
Dataset metadata EML, REQUIRED for checklist datasets
資料集元資料生態模式語言，名錄型資料為必填。
A machine-readable statement of the rights attached to the published dataset. Use either CC0 or CC BY.
Note: All datasets funded under the BID and BIFA programmes must be published under either a Creative Commons CC0 rights waiver or a CC BY Attribution license.. Datasets without a valid license statement will not be accepted for publication. Machine-readable licenses allow automated data filters that give users clear guidance on the permitted use of records, thereby promoting data use and citation. 
注意:所有由BID及BIFA程式所資助的資料集均需使用Creative Commons CC0 rights waiver或CC BY Attribution license發表。資料集若沒有有效許可證照聲明，將不會被接受作為發表。可被機器讀取的許可證照可以讓資料自動過濾，為用戶提供關於允許使用記錄的明確指南，從而促進數據使用和引用。

contact(s)
聯絡方式(contact(s))
Dataset metadata EML, REQUIRED for checklist datasets
資料集元資料生態模式語言，名錄型資料為必填。

Contact data (minimum: name and email) for at least one administrative contact for the dataset.
內容包含至少一位資料集元資料行政部門聯絡資料(至少有名字與電子郵件)。
Contact data will be publicly visible at gbif.org. This information is required to ensure the possibility of communication about the dataset. The administrative contact is the person/role to be consulted about content, quality, and rights questions concerning the dataset, both by users and by central services (GBIFS). If personal contact data cannot be supplied, it is possible to supply a functional contact through a role name (e.g. “curator”) and email (collections@myhouse.com). It is necessary, though, that responsibilities for handling incoming communication are clearly defined and followed internally.
聯絡資料將可在gbif.org中公開審視。此訊息為必要以確與認資料集(提供者)溝通的可能性。行政部門的聯絡人為GBIFS的使用者及中央服務部門可以就資料集的內容、品質以及版權問題與之協調的人(角色)。如果無法提供個人的連略資訊，也可以提供一個具有功能性的聯絡人(例如:館長)及電子郵件(例如:collections@myhouse.com)。但是，必須要明確定義誰應該負責處理接收到的訊息，且內部應遵守。

creator(s)
建立者(creator(s))
資料集元資料生態模式語言，名錄型資料為必填。
Dataset metadata EML, REQUIRED for checklist datasets

Contact data (minimum: name and email) for the creator of the dataset (see [link])
內容包含資料集元資料創建者聯絡資料(至少有名字與電子郵件)(見[link])。

metadata provider(s)
元資料提供者(metadata provider(s))
資料集元資料生態模式語言，名錄型資料為必填。
Dataset metadata EML, REQUIRED for checklist datasets
Contact data (minimum: name and email) for the author of the dataset metadata (see [link])
內容包含資料集元資料作者聯絡資料(至少有名字與電子郵件)(見[link])。

citation
引用方式(citation)
Dataset metadata EML, STRONGLY RECOMMENDED for checklist datasets
資料集元資料生態模式語言，名錄型資料為必填。
a text specifying how your dataset should be cited in publications that make use of your data.
為一段句子指出使用您資料集的人如何引用您的資料及在發表之中。
To ensure your dataset gets cited the way you want, you can explicitly specify the requested citation. This text will be displayed on the dataset page, and it will be supplied to data users together with downloads that contain any contribution from your dataset. If no text is specified, GBIF will automatically supply a standard format citation that includes the dataset name and the name of the publishing institution, together with the date of the download and a reference to gbif.org.
為確定使用者會依您的意思引用您的資料集，您可以明確地指出引用的方式。這一段句子將會呈現在您的資料集頁面，同時也會提供給使用者所下載的任何含有您所貢獻的資料的其他資料集中。若缺少這一段文字，GBIF將會自動提供您的資料集一個標準的引用格式，包含資料集名稱、發表單位、下載日期及gbif.org的參照連結。

projectID
計畫編碼(projectID)
Dataset metadata EML, REQUIRED for some checklist datasets
資料集元資料生態模式語言，名錄型資料為必填。
A unique identifier for the project from which a dataset is derived.
一個計劃所衍生的資料集獨一無二的編碼。紀錄的形式則為一個GUID或者是全球獨一的識別碼。
The record type is a GUID or other identifier that is near globally unique.
This field is REQUIRED for a dataset that is funded through programmes operated by GBIF. In this case, the projectID is the ID of the funded project as listed in the contract document, e.g. “BID-AF2016-0001-REG”.
若資料集是由GBIF操作(管理?)的程式所資助，此欄位為必填。計畫編碼則為合約文件中所列由GBIF程式所資助的編號(編碼)，例如“BID-AF2016-0001-REG”。

projectTitle
計畫名稱(title)
Dataset metadata EML, REQUIRED for some checklist datasets
資料集元資料生態模式語言，名錄型資料為必填。

for some checklist datasets The title of the funded project as listed in the contract document, but not containing the projectID and other administrative information, such as the project titles listed here.
This field is REQUIRED for a dataset that is funded through programmes operated by GBIF. 
有些名錄性質的資料集的名稱即為合約文件中所列之資助項目名稱，但不包含計畫編碼(projectID)及其他管理資訊。相關範例可以參照計畫項目列表。若資料集是由GBIF操作(管理?)的程式所資助，此欄位為必填。
