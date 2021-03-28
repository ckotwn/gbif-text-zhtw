#### Document Control
| Date | Description | Author(s) |
| ---- | ----------- | --------- |
|      | 初譯        | 何宣慶    |
|  | 覆譯及審閱  | 柯智仁    |
|  | 發布  |    |


https://www.gbif.org/data-quality-requirements-checklists?fbclid=IwAR11wSu0wOWaRzi-DGQZuJjocVB2uEFg8auVdaCN-rTSgDpdRP3gzesdrr4
資料品質需求:名錄資料集
Data quality requirements: Checklist datasets
透過依循這些資料品質的需求及建議，資料發布者可以改善他們的名錄資料集的品質、完整性及價值。
By following these data quality requirements and recommendations, data publishers can improve the quality, completeness and value of their checklist datasets.

名錄資料集提供一組已具學名的生物或分類單元(註)的目錄、快速總結(簡易總結?)或基本清單。雖然它們可能包含其他細節，如當地物種名稱或標本佐證，但名錄通常依照分類上、地理上或主題系列或此三者中一些組合來進行資訊的分類。透過依循這些資料品質的需求及建議，資料發布者可以改善他們的名錄資料集的品質、完整性及價值。
註:分類單元(taxa)代表一個族群，可以是一個種、一個亞種或者種以上位階。
Checklist datasets provide a catalogue, rapid summary or baseline inventory a set of named organisms, or taxa. While they may include additional details like local species names or specimen citations, checklists typically categorize information along taxonomic, geographic, and thematic lines, or some combination of the three.
By following these data quality requirements and recommendations, data publishers can improve the quality, completeness and value of their checklist datasets.

Darwin Core紀錄(達爾文核心紀錄)
Darwin Core records 

欄位名稱	需求狀態
taxonID(物種編號)
必填
scientificName(學名)
必填
taxonRank(物種位階)
必填
kingdom(界)
強烈建議填寫
parentNameUsageID(目前使用學名編號)
強烈建議填寫
acceptedNameUsageID(接受使用學名編號)	強烈建議填寫
vernacularName(俗名)
盡可能填寫

巨資料集(EML)
Dataset metadata (EML)
欄位名稱	需求狀態
title(資料集名稱)
必填
description(基本描述)
必填
publishing organization(發布單位)
必填
type(資料類型)
必填
license(證照、許可證)
必填
contact(s)(聯絡資訊)
必填
creator(s)(創立者)
必填
metadata provider(s) (資料集提供者)
必填
citation(引用資訊/文獻)
強烈建議填寫
註:若一資料集為GBIF所操作之程式所資助(亦即BID, BIFA, CESP)，則需要額外填寫下兩個欄位。
Note: If the dataset is funded through a programme operated by GBIF (e.g. BID, BIFA, CESP), two additional fields are required:
	
projectID (計畫編號)
必填
projectTitle (計畫名稱)
必填

欄位名稱說明
	需求狀態
	必填資訊
    以下所列的項目為發表出現資料集所需最少必要需求。BGIF.org網站將不會接受缺少這些資訊的資料集，也不會使用這些紀錄。雖然這些欄位是發佈資料必備的，但這也只是開始而已。除非提供額外資訊，否則這些已經發佈數據的被使用程度仍有很多限制。
Required information
The items listed below constitute the minimum formal requirements for publishing an occurrence dataset. GBIF.org will not accept a dataset without these terms and will not index the records. While these items are mandatory for publishing the dataset at all, they are only the starting point. The usefulness of the published data will still be severely limited unless additional information is supplied.

	強烈建議
    除了必要的資料外，我們也強烈建議提供一些欄位用以協助改善資料庫的用處。理由是:
	有些資訊會被匯集到全球資料源頭以及用於防止不一致，例如將可能被用在超過一個物種的學名(即異物同名)放在正確的分類群位置中。
	越精確的地理位置資訊(經緯度)越可以有效地增加資料被其他案例廣泛使用的可能性。
	可以為某些資料元素(即經緯度)增加選擇性，進一步提供這些元素的釋疑，讓使用者更容易評估使用一個數據的可能性。
	有些額外的資訊可以用以支援資料品質控管以及錯誤偵測(例如:測試原提供的國家編碼與經緯度的一致性)。
	資料集的有效資訊範圍越豐富，就有可能被用在更多的地方，這意味這個資料集會更廣泛被觸及、使用以及更常被引用。
[這一整段我覺得不太能用英文直接翻，因為我們不會這樣用]

Strongly recommended
In addition to the mandatory data elements, we strongly recommend completing several more fields that help improve the usefulness of the dataset because: 

	some information supports the integration into a global data resource and prevents ambiguity, e.g. in matching scientific names that could apply to more than one organism (homonyms) to the correct place within the backbone taxonomy
	more precise geo-location data (coordinates) significantly increase the usefulness of the data for a wide range of use cases
	additional qualifiers for some data elements, e.g. coordinates, support the interpretation of those elements and help users to better estimate their usefulness for a given data use case 
	some data redundancy supports quality control and error detection (e.g. testing country codes against coordinates where both are supplied) 
	last not least, the richer the spectrum of available information of a dataset is, the more potential usage areas it becomes available for, meaning the dataset will me [will be] more widely accessible and used and cited more often

	盡可能提供
如果有所列項目以外的資料，可以考慮盡可能分享這些資訊，用以增加發表資料被使用的可能性。
Share if available
If additional data are available, consider sharing them in order to increase the usefulness of your published data.

名詞解釋Terms 

物種編碼(taxonID)
Darwin Core資料集之元素，名錄型資料集為必填。
    這欄位為一個分類單元獨一無二的識別碼，可以讓同一個分類單元在不同的資料集版本以及透過下載和使用的資料中被確認(參閱達爾文核心專有名詞:快速參考指南)
    理想狀態中，物種編號為一個全球獨一無二的識別碼，或至少在一個資料集中是唯一的編碼。這個數字可以讓同一個分類單元的資訊隨著時間修訂後，仍可以持續被確認；可以連結其他額外的訊息，如影像及出現紀錄；以及可以連結引用紀錄，例如報告或出版品。這代表物種的編碼需要確實與來源的分類單元資訊連結，用以指出同一份發表的資料集及任何下一層級一樣的分類單元資訊。

taxonID
Darwin Core dataset element, REQUIRED for checklist datasets
A unique identifier for the taxon, allowing the same taxon to be recognized across dataset versions as well as through data downloads and use (see Darwin Core Terms: A quick reference guide

Ideally, the taxonID is a persistent global unique identifier. As a minimum requirement, it has to be unique within the published dataset. It allows to recognize the same set of taxon information over time when the dataset indexing is refreshed; it links additional data like images or occurrence records; and it makes it possible to cite records e.g. in usage reports or in publications. This means that the taxonID needs to reliably stay with the taxon information at source, and to consistently refer to the same set of taxon information in published datasets and any underlying source data.

學名(scientificName)
達爾文核心資料集元素，名錄型資料集為必填。
    這個欄位為一個完整的學名，包含其作者及年代。
    在名錄中，學名為一個準備收集及發表分類群列表或各層級的核心資料元素。(參閱達爾文核心專有名詞:快速參考指南)。
    依照名錄的需求，學名可以是任何分類層級(hierarchical level)。通常會是種級或是種級以下，例如用作地區性植物相或動物相名錄、紅皮書或外來種，或是海洋生物或物種種群的分類重新檢視。假使一個名錄準備發表一個具有不同層級的資料(樹狀結構)，可以在資料集中增加一些相對較高階的分類單元，例如界、綱、科，並利用父名稱使用編碼(parentNameUsageID)欄位將這些連結到一個明確解釋的架構，可以清楚解釋來支援名錄中的欄位。
   有效的學名應為遵循依不同類群所設定的法條規範所建立的拉丁化學名。不可以使用臨時名稱(例如“Mallomonas sp.4”)，通用名稱(例如“fruit fly”)或具有不確定性的名稱(例如“Anemone cf. nemorosa”)。如要使用通用名稱(俗名)則只能當成學名的補充，可以使用俗名(VernacularName)的欄位設定(如下)。

scientificName
Darwin Core dataset element, REQUIRED for checklist datasets
The full scientific name, including authorship and year of the name where applicable. In the context of a checklist, the scientific name is the core data element of a taxon list or hierarchy that the dataset is set out to collate and publish (see Darwin Core Terms: A quick reference guide)
Depending on the purpose of the checklist, scientific names may be of any hierarchical level, though typically would be of species rank or below for, e.g., regional floristic or faunistic checklists, Red List collations, or thematic inventories like marine organisms or taxonomic revisions of species groups. If the checklist is intended to publish a hierarchy (tree-like structure), add separate entries for the relevant upper taxonomic ranks, e.g. kingdom, class and family, and link them into a hierarchical structure using the parentNameUsageID (see below) to support unambiguous interpretation of the checklist entries.
Valid scientific names are Latin names following the syntax rules of the respective taxon group (e.g. botanical nomenclature). Not permitted are, i.a., working names (“Mallomonas sp.4”), common names (“fruit fly”), or names containing identification qualifiers (“Anemone cf. nemorosa”). If common names are used, they should be supplied in addition to the scientific names, using the VernacularName set of fieds [fields] (see below).


物種階級(taxonRank)
達爾文核心資料集元素，名錄型資料集為必填。
    用以表示學名的分類層級(參閱達爾文核心專有名詞:快速參考指南)
    物種階級之用在處理學名的釋疑以及用於核對名錄紀錄中的核心分類，尤其是屬級或更高的層級(單詞)。雖然有些較高層級的分類單元名稱已經包含可以指出其層級的字元，但這在群體間甚或群體內部不一定一致，所以無法被用作解釋層級。為使學名可以在層級中被正確歸位，在一個分類單元的更高層級中明確指出其分類層級為必要。為切合這些目的，分類層級(主要)應該依循林奈所設立的層級:界、門、綱、目、科、屬、種。這裡使用拉丁文或英文的用法都可以。

taxonRank
Darwin Core dataset element, REQUIRED for checklist datasets
The taxonomic rank of the supplied scientific name (see Darwin Core Terms: A quick reference guide

The taxon rank supports the interpretation of the scientific name during indexing, and supports matching the checklist records to the core taxonomy, especially in the case of names at genus level or above (monomials). While the format of higher taxon names in some groups contains indicators of their rank, this is not consistent across or even within groups, and cannot be reliably used for interpretation. For placing names correctly, explicitly specifying the taxon rank, alongside information on the higher taxonomy, is an important criterion. For practical purposes, the ranks used have to be (major) Linnean ranks: kingdom, phylum, class, order, family, genus, species. Both Latin or English terms are accepted.

界(kingdom)
達爾文資料集核心元素, 在名錄型資料集中為強烈建議提供。
    完整的學名加上這個學名所屬的界級分類(參閱達爾文核心專有名詞:快速參考指南)或者其他更高層分類(如有)。
    如果只有學名，有很多例子很可能無法完全配對到正確的分類群。例如，異物同名(通常是不同的類群中不一樣的生物，完全一樣的學名)或者有些剛描述的學名尚未列在現有的分類樹中，亦或者因為拼法的變異(如錯字或斷字因素等)。為可以正確配對到核心分類的學名，增加更高層級的名稱可以協助釋疑以及防止錯誤。對於數據集來說，已發表的資料中的層級結構並不是最重要的，可以藉由添加DarwinCore中的相對欄位來提供更高層級的名稱作為記錄本身的一部分，類似於出現資料集。
    這些學名必須為拉丁學名，置於林奈的分類層級之下，例如”Animalia”(界)或”Rosaceae”(科)。不可以是俗名(“animals”)，縮寫(“Rosac.”)，中間層級(“Tetrapoda”(上綱))或多係群或非分類之分群(“algae”, “herbivora”)。
(這一段落落長…真是令人生氣，不過就是說加上綱或屬以上層級避免異物同名情形發生…就好)

kingdom
Darwin Core dataset element, STRONGLY RECOMMENDED for checklist datasets
The full scientific name specifying the kingdom that the scientific name is classified under (see Darwin Core Terms: A quick reference guide and other higher taxonomy, if possible

With scientific names, there are numerous cases where the matching of a given name against the core taxonomy is unsure or ambiguous. This is the case, for example, with homonyms (identical names exist for different organisms, usually across groups), newly described names that are not yet part of the existing taxonomic tree, or spelling variants (typos, hyphenation etc). To support exact matching of a scientific name against the core taxonomy, additional names at higher ranks help interpretation and error prevention. For datasets where the hierarchical representation in the published data is not important, higher level names can be supplied as part of the record itself by adding the relevant DarwinCore fields, similar to occurrence datasets.
Names should be scientific (latin) names at major Linnean ranks, like “Animalia” (kingdom) or “Rosaceae” (family). Not: common names (“animals”), abbreviations (“Rosac.”), intermediate rank levels (“Tetrapoda” (superclass)), or polyphyletic or non-taxonomic groupings (“algae”, “herbivora”).

父名編碼(parentNameUsageID)
達爾文資料集核心元素, 在名錄型資料集中為強烈建議提供。
名錄型資料集中較分類單元直接高一層級的名稱的物種編碼(taxonID)，前提為這個較分類單元高一層級的名稱在列表中為分開輸入。參閱http://rs.tdwg.org/dwc/terms/parentNameUsageID.
    這個編碼可以成為資料集中的階層(hierarchy)代表，亦即用於分類學的出版品。
說明:如果資料集中有輸入學名、屬名及科名等，則屬名的編碼為學名編碼的父名編碼，科名的編碼為屬名的父名編碼。依此類推，可以有效建立分類層級。
[我覺得我的解釋比較好…]

parentNameUsageID
Darwin Core dataset element, STRONGLY RECOMMENDED for checklist datasets
The taxonID of the next available higher-ranked (parent) entry within the checklist dataset, if higher taxon names are supplied as separate entries in the list. See http://rs.tdwg.org/dwc/terms/parentNameUsageID.
This supports the representation of the dataset as a hierarchy, e.g. for the publication of a taxonomy.

接受名稱編碼(acceptedNameUsageID)
達爾維核心資料集元素，名錄型資料強烈建議提供。
    假使一名錄型資料集中有提供被接受名及異名，則該異名(synonym)的這個欄位編碼，應為名錄中被接受的分類單元名稱的編碼(taxonID)。見http://rs.tdwg.org/dwc/terms/acceptedNameUsageID
    這可以支應一個分類資料集的異名錄的代表性。
說明:因為異名為無效名，所以一定有一個相對應的有效名(被接受名)，故在這一個欄位中填入該有效名作為連結。A種的欄位若填入B的編碼，則表示A為B之次異名。

acceptedNameUsageID
Darwin Core dataset element, STRONGLY RECOMMENDED for checklist datasets
Within the record of a synonym, the taxonID of the accepted taxon name entry within the checklist dataset, if both synonyms and accepted names are supplied. See http://rs.tdwg.org/dwc/terms/acceptedNameUsageID
This supports the representation of synonymy for a taxonomic dataset.

俗名(vernacularName)
    達爾維核心資料集元素，名錄型資料盡可能提供。
參照http://rs.gbif.org/extension/gbif/1.0/vernacularname.xml.
若有，也請至少提供名稱所使用哪個國家的語言，可參照ISO 639-1 language codes

vernacularName
Darwin Core dataset element, SHARE IF AVAILABLE for checklist datasets
See http://rs.gbif.org/extension/gbif/1.0/vernacularname.xml. When supplied, also add at least the language of the name, using ISO 639-1 language codes

標題(title)
資料集元資料生態模式語言，名錄型資料為必填。
    每個資料集的標題都會發布在gbif.org網站。
    建議事項:一段簡短、可以指出資料集的國際背景以及與其他研究單位的資料及區分的描述性文字。例如“Four new generic and 14 new specific synonymies in Pholcidae, and transfer of Pholcoides Roewer to Filistatidae (Araneae)”。不建議使用“Araneae (Part 1) part”。 這表示標題最後會變成資料集引用文獻的標題。
說明:標題盡量避免過於簡短或不容易判斷出處或造成重複。最好明確指出地點、分類群及簡短內容。

title
Dataset metadata EML, REQUIRED for checklist datasets
The title under which the dataset will be published at gbif.org.
Recommendation: a brief, but descriptive title that characterizes the dataset in an international context and distinguishes it from similar datasets in other institutions. E.g. “Four new generic and 14 new specific synonymies in Pholcidae, and transfer of Pholcoides Roewer to Filistatidae (Araneae)”. Not recommended: “Araneae (Part 1) part.”. The title will, i.a., be part of the dataset citation on use of the data.

基本描述(description)
資料集元資料生態模式語言，名錄型資料為必填。
    一段用英文描述資料集內容的文字。
    可以是較長版本的標題，敘明名錄之地理區、溫度及分類範疇、研究方法及目的(例如紅皮書、外來種、淡水物種、地區性植物)、適當的參考文獻或者您認為符合資料集特性的其他資訊。另外一個以英語以外的語言的描述也可置於英語基本描述下方。
description
Dataset metadata EML, REQUIRED for checklist datasets
An English language text, describing the dataset.
This may include a longer version of title, a description of geographic, temporal and taxonomic scope of the checklist, methodology and purpose of the underlying data compilation (e.g. red list, invasive species, freshwater taxa, regional flora), relevant literature references, and any other information you consider relevant to characterize the dataset. A second version of the description in another language than English may be added underneath.

發布單位(publishing organization)
資料集元資料生態模式語言，名錄型資料為必填。
    研究所或組織的名稱在gbif.org中將被列為資料發布者。
    發布資料的組織為持有或擁有資料集且負責資料內容及維護的研究所。名稱應為已在相關機構註冊、在網站上明列的組織正式名稱，抑或是計畫合約中所提及之名稱。
publishing organization
Dataset metadata EML, REQUIRED for checklist datasets
The title of the institution or organization that will be listed as the data publisher at gbif.org. 
The publishing organization is the institution which holds or owns the dataset and is in charge of its contents and maintenance. The title given should be the official title of the organization as registered with relevant authorities, listed on websites, and, if applicable, as stated in the project contract.

資料集類別(type)
資料集元資料生態模式語言，名錄型資料為必填。
    這邊應該要填入的類別為”名錄(Checklist)”。
    資料的類別表示資料集中所有紀錄的主要焦點(核心紀錄)。對於名錄型資料，紀錄的類別一定是”checklist”。也有可能是名錄紀錄所連結的出現資料(例如，分類研究的證物標本或紀錄一個地區植物相的博物館記錄)。這個連結的資訊應該依照出現資料發布的指引[link]。
The record type describes the main focus of all records contained in the dataset (core records). For a checklist dataset, the record type will always be “checklist”. There may also be occurrences linked to checklist records (e.g. vouchers of a taxonomic treatment, herbarium records documenting a regional flora). The structure and requirements for this linked information follows the guidelines given for occurrence data publication [link].

type
Dataset metadata EML, REQUIRED for checklist datasets
The type of the dataset. Here: “checklist”.
The record type describes the main focus of all records contained in the dataset (core records). For a checklist dataset, the record type will always be “checklist”. There may also be occurrences linked to checklist records (e.g. vouchers of a taxonomic treatment, herbarium records documenting a regional flora). The structure and requirements for this linked information follows the guidelines given for occurrence data publication [link].

許可證照(license)
資料集元資料生態模式語言，名錄型資料為必填。
    注意:所有由BID及BIFA程式所資助的資料集均需使用Creative Commons CC0 rights waiver或CC BY Attribution license發表。資料集若沒有有效許可證照聲明，將不會被接受作為發表。可被機器讀取的許可證照可以讓資料自動過濾，為用戶提供關於允許使用記錄的明確指南，從而促進數據使用和引用。
license
Dataset metadata EML, REQUIRED for checklist datasets
A machine-readable statement of the rights attached to the published dataset. Use either CC0 or CC BY.
Note: All datasets funded under the BID and BIFA programmes must be published under either a Creative Commons CC0 rights waiver or a CC BY Attribution license.. Datasets without a valid license statement will not be accepted for publication. Machine-readable licenses allow automated data filters that give users clear guidance on the permitted use of records, thereby promoting data use and citation. 

聯絡方式(contact(s))
資料集元資料生態模式語言，名錄型資料為必填。
    內容包含至少一位資料集元資料行政部門聯絡資料(至少有名字與電子郵件)。
    聯絡資料將可在gbif.org中公開審視。此訊息為必要以確與認資料集(提供者)溝通的可能性。行政部門的聯絡人為GBIFS的使用者及中央服務部門可以就資料集的內容、品質以及版權問題與之協調的人(角色)。如果無法提供個人的連略資訊，也可以提供一個具有功能性的聯絡人(例如:館長)及電子郵件(例如:collections@myhouse.com)。但是，必須要明確定義誰應該負責處理接收到的訊息，且內部應遵守。

contact(s)
Dataset metadata EML, REQUIRED for checklist datasets
Contact data (minimum: name and email) for at least one administrative contact for the dataset.
Contact data will be publicly visible at gbif.org. This information is required to ensure the possibility of communication about the dataset. The administrative contact is the person/role to be consulted about content, quality, and rights questions concerning the dataset, both by users and by central services (GBIFS). If personal contact data cannot be supplied, it is possible to supply a functional contact through a role name (e.g. “curator”) and email (collections@myhouse.com). It is necessary, though, that responsibilities for handling incoming communication are clearly defined and followed internally.

建立者(creator(s))
資料集元資料生態模式語言，名錄型資料為必填。
內容包含資料集元資料創建者聯絡資料(至少有名字與電子郵件)(見[link])。

creator(s)
Dataset metadata EML, REQUIRED for checklist datasets
Contact data (minimum: name and email) for the creator of the dataset (see [link])

元資料提供者(metadata provider(s))
資料集元資料生態模式語言，名錄型資料為必填。
內容包含資料集元資料作者聯絡資料(至少有名字與電子郵件)(見[link])。
metadata provider(s)
Dataset metadata EML, REQUIRED for checklist datasets
Contact data (minimum: name and email) for the author of the dataset metadata (see [link])

引用方式(citation)
資料集元資料生態模式語言，名錄型資料為必填。
    為一段句子指出使用您資料集的人如何引用您的資料及在發表之中。
    為確定使用者會依您的意思引用您的資料集，您可以明確地指出引用的方式。這一段句子將會呈現在您的資料集頁面，同時也會提供給使用者所下載的任何含有您所貢獻的資料的其他資料集中。若缺少這一段文字，GBIF將會自動提供您的資料集一個標準的引用格式，包含資料集名稱、發表單位、下載日期及gbif.org的參照連結。
citation
Dataset metadata EML, STRONGLY RECOMMENDED for checklist datasets
a text specifying how your dataset should be cited in publications that make use of your data.
To ensure your dataset gets cited the way you want, you can explicitly specify the requested citation. This text will be displayed on the dataset page, and it will be supplied to data users together with downloads that contain any contribution from your dataset. If no text is specified, GBIF will automatically supply a standard format citation that includes the dataset name and the name of the publishing institution, together with the date of the download and a reference to gbif.org.

計畫編碼(projectID)
資料集元資料生態模式語言，名錄型資料為必填。
一個計劃所衍生的資料集獨一無二的編碼。紀錄的形式則為一個GUID或者是全球獨一的識別碼。
若資料集是由GBIF操作(管理?)的程式所資助，此欄位為必填。計畫編碼則為合約文件中所列由GBIF程式所資助的編號(編碼)，例如“BID-AF2016-0001-REG”。
projectID
Dataset metadata EML, REQUIRED for some checklist datasets
A unique identifier for the project from which a dataset is derived.
The record type is a GUID or other identifier that is near globally unique.
This field is REQUIRED for a dataset that is funded through programmes operated by GBIF. In this case, the projectID is the ID of the funded project as listed in the contract document, e.g. “BID-AF2016-0001-REG”.

計畫名稱(title)
資料集元資料生態模式語言，名錄型資料為必填。
有些名錄性質的資料集的名稱即為合約文件中所列之資助項目名稱，但不包含計畫編碼(projectID)及其他管理資訊。相關範例可以參照計畫項目列表。若資料集是由GBIF操作(管理?)的程式所資助，此欄位為必填。

for some checklist datasets The title of the funded project as listed in the contract document, but not containing the projectID and other administrative information, such as the project titles listed here.
This field is REQUIRED for a dataset that is funded through programmes operated by GBIF. 


