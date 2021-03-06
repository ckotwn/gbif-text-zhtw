[Checklist datasets](/dataset-classes#checklists) provide a catalogue, rapid summary or baseline inventory a set of named organisms, or taxa. While they may include additional details like local species names or specimen citations, checklists typically categorize information along taxonomic, geographic, and thematic lines, or some combination of the three.

By following these data quality requirements and recommendations, data publishers can improve the quality, completeness and value of their checklist datasets.

### **Darwin Core records**

|Term | [Status](#status) |
|--|--|
|[taxonID](#dcTaxon) | Required |
|[scientificName](#dcSciName) | Required |
|[taxonRank](#dcTaxonRank) | Required |
|[kingdom](#dcKingdom) | Strongly recommended | 
|[parentNameUsageID](#dcParentName) | Strongly recommended | 
|[acceptedNameUsageID](#dcAcceptedName) | Strongly recommended | 
|[vernacularName](#dcVernacularName) | Share if available | 

### **Dataset metadata (EML)**

|Term | [Status](#status) |
|--|--|
|[title](#emlTitle) | Required |
|[description](#emlDescription) | Required |
|[publisher](#emlPublisher) | Required |
|[type](#emlType) | Required | 
|[license](#emlLicense) | Required |
|[contact](#emlContact) | Required |
|[creator](#emlCreator) | Required |
|[metadataProvider](#emlMetadataProvider) | Required |
|[citation](#emlCitation) | Strongly recommended |

Note: If the dataset is funded through a programme operated by GBIF (e.g. [BID](/programme/82243), [BIFA](/programme/82629), [CESP](/programme/82219)), __two additional fields are required__:

| | |
|--|--|
|[projectID](#emlProjectID) | Required |
|[projectTitle](#emlProjectTitle) | Required |

<a name="status"></a>
### Status

#### Required information

The items listed below constitute the minimum formal requirements for publishing an checklist dataset. GBIF.org will not accept a dataset without these terms and will not index the records. While these items are mandatory for publishing the dataset at all, they are only the starting point. The usefulness of the published data will still be severely limited unless additional information is supplied.

#### Strongly recommended

In addition to the mandatory data elements, we strongly recommend completing several more fields that help improve the usefulness of the dataset because:
+ some information supports the integration into a global data resource and prevents ambiguity, e.g. in matching scientific names that could apply to more than one organism (homonyms) to the correct place within the backbone taxonomy
+ more precise geo-location data (coordinates) significantly increase the usefulness of the data for a wide range of use cases
+ additional qualifiers for some data elements, e.g. coordinates, support the interpretation of those elements and help users to better estimate their usefulness for a given data use case
+ some data redundancy supports quality control and error detection (e.g. testing country codes against coordinates where both are supplied)
+ last but not least, the richer the spectrum of available information of a dataset is, the more potential usage areas it becomes available for, meaning the dataset will me more widely accessible and used and cited more often

#### Share if available

If additional data are available, consider sharing them in order to increase the usefulness of your published data.

<a name="terms"></a>
### Terms

**taxonID**<a name="dcTaxon"></a><br />*Darwin Core dataset element*, REQUIRED for checklist datasets<br />A unique identifier for the taxon, allowing the same taxon to be recognized across dataset versions as well as through data downloads and use (see [*Darwin Core Terms: A quick reference guide*](https://dwc.tdwg.org/list/#dwc_taxonID)<br />
Ideally, the taxonID is a persistent global unique identifier. As a minimum requirement, it has to be unique within the published dataset. It allows to recognize the same set of taxon information over time when the dataset indexing is refreshed; it links additional data like images or occurrence records; and it makes it possible to cite records e.g. in usage reports or in publications. This means that the taxonID needs to reliably stay with the taxon information at source, and to consistently refer to the same set of taxon information in published datasets and any underlying source data.

**scientificName**<a name="dcSciName"></a><br />*Darwin Core dataset element*, REQUIRED for checklist datasets<br />The full scientific name, including authorship and year of the name where applicable. In the context of a checklist, the scientific name is the core data element of a taxon list or hierarchy that the dataset is set out to collate and publish (see [*Darwin Core Terms: A quick reference guide*](ttps://dwc.tdwg.org/list/#dwc_scientificName)<br />
Depending on the purpose of the checklist, scientific names may be of any hierarchical level, though typically would be of species rank or below for, e.g., regional floristic or faunistic checklists, Red List collations, or thematic inventories like marine organisms or taxonomic revisions of species groups. If the checklist is intended to publish a hierarchy (tree-like structure), add separate entries for the relevant upper taxonomic ranks, e.g. kingdom, class and family, and link them into a hierarchical structure using the parentNameUsageID (see below) to support unambiguous interpretation of the checklist entries.<br />
Valid scientific names are Latin names following the syntax rules of the respective taxon group (e.g. botanical nomenclature). Not permitted are, i.a., working names ("Mallomonas sp.4"), common names ("fruit fly"), or names containing identification qualifiers ("Anemone cf. nemorosa"). If common names are used, they should be supplied in addition to the scientific names, using the VernacularName set of fields(see below).

**taxonRank**<a name="dcTaxonRank"></a><br />*Darwin Core dataset element*, REQUIRED for checklist datasets<br />The taxonomic rank of the supplied scientific name (see [*Darwin Core Terms: A quick reference guide*](https://dwc.tdwg.org/list/#dwc_taxonRank)<br />
The taxon rank supports the interpretation of the scientific name during indexing, and supports matching the checklist records to the core taxonomy, especially in the case of names at genus level or above (monomials). While the format of higher taxon names in some groups contains indicators of their rank, this is not consistent across or even within groups, and cannot be reliably used for interpretation. For placing names correctly, explicitly specifying the taxon rank, alongside information on the higher taxonomy, is an important criterion. For practical purposes, the ranks used have to be (major) Linnean ranks: kingdom, phylum, class, order, family, genus, species. Both Latin or English terms are accepted.

**kingdom**<a name="dcKingdom"></a><br />*Darwin Core dataset element*, STRONGLY RECOMMENDED for checklist datasets<br />The full scientific name specifying the kingdom that the scientific name is classified under (see [*Darwin Core Terms: A quick reference guide*](http://rs.tdwg.org/dwc/terms/kingdom) and other higher taxonomy, if possible<br />
With scientific names, there are numerous cases where the matching of a given name against the core taxonomy is unsure or ambiguous. This is the case, for example, with homonyms (identical names exist for different organisms, usually across groups), newly described names that are not yet part of the existing taxonomic tree, or spelling variants (typos, hyphenation etc). To support exact matching of a scientific name against the core taxonomy, additional names at higher ranks help interpretation and error prevention. For datasets where the hierarchical representation in the published data is not important, higher level names can be supplied as part of the record itself by adding the relevant DarwinCore fields, similar to occurrence datasets. 

Names should be scientific (latin) names at major Linnean ranks, like "Animalia" (kingdom) or "Rosaceae" (family). Not: common names ("animals"), abbreviations ("Rosac."), intermediate rank levels ("Tetrapoda" (superclass)), or polyphyletic or non-taxonomic groupings ("algae", "herbivora").

**parentNameUsageID**<a name="dcParentName"></a><br />*Darwin Core dataset element*, STRONGLY RECOMMENDED for checklist datasets<br />The taxonID of the next available higher-ranked (parent) entry within the checklist dataset, if higher taxon names are supplied as separate entries in the list. See https://dwc.tdwg.org/list/#dwc_parentNameUsageID.<br />This supports the representation of the dataset as a hierarchy, e.g. for the publication of a taxonomy.

**acceptedNameUsageID**<a name="dcAcceptedName"></a><br />*Darwin Core dataset element*, STRONGLY RECOMMENDED for checklist datasets<br />Within the record of a synonym, the taxonID of the accepted taxon name entry within the checklist dataset, if both synonyms and accepted names are supplied. See http://rs.tdwg.org/dwc/terms/acceptedNameUsageID<br />This supports the representation of synonymy for a taxonomic dataset.

**vernacularName**<a name="dcVernacularName"></a><br />*Darwin Core dataset element*, SHARE IF AVAILABLE for checklist datasets<br />See http://rs.gbif.org/extension/gbif/1.0/vernacularname.xml. When supplied, also add at least the language of the name, using [ISO 639-1 language codes](http://rs.gbif.org/vocabulary/iso/639-1.xml).

**title**<a name="emlTitle"></a><br />*Dataset metadata EML*, REQUIRED for checklist datasets<br />The title under which the dataset will be published at gbif.org.<br />Recommendation: a brief, but descriptive title that characterizes the dataset in an international context and distinguishes it from similar datasets in other institutions. E.g. "Four new generic and 14 new specific synonymies in Pholcidae, and transfer of Pholcoides Roewer to Filistatidae (Araneae)". Not recommended: "Araneae (Part 1) part.". The title will, i.a., be part of the dataset citation on use of the data.

**description**<a name="emlDescription"></a><br />*Dataset metadata EML*, REQUIRED for checklist datasets<br />An English language text, describing the dataset.<br/>
This may include a longer version of title, a description of geographic, temporal and taxonomic scope of the checklist, methodology and purpose of the underlying data compilation (e.g. red list, invasive species, freshwater taxa, regional flora), relevant literature references, and any other information you consider relevant to characterize the dataset. A second version of the description in another language than English may be added underneath. 

**publisher**<a name="emlPublisher"></a><br />*Dataset metadata EML*, REQUIRED for checklist datasets<br />The title of the institution or organization that will be listed as the data publisher at gbif.org.<br />
The publishing organization is the institution which holds or owns the dataset and is in charge of its contents and maintenance. The title given should be the official title of the organization as registered with relevant authorities, listed on websites, and, if applicable, as stated in the project contract.

**type**<a name="emlType"></a><br />*Dataset metadata EML*, REQUIRED for checklist datasets<br />The type of the dataset. Here: "checklist".<br />
The record type describes the main focus of all records contained in the dataset (core records). For a checklist dataset, the record type will always be "checklist". There may also be occurrences linked to checklist records (e.g. vouchers of a taxonomic treatment, herbarium records documenting a regional flora). The structure and requirements for this linked information follows the guidelines given for [occurrence data publication](https://ipt.gbif.org/manual/en/ipt/2.5/occurrence-data).

**license**<a name="emlLicense"></a><br />*Dataset metadata EML*, REQUIRED for checklist datasets<br />A machine-readable statement of the rights attached to the published dataset. Use either CC0 or CC BY.<br />
*Note: All datasets funded under the [BID](/programme/82243) and [BIFA programmes](/programme/82629/) must be published under either a Creative Commons [CC0 rights waiver](https://creativecommons.org/about/cc0) or a [CC BY Attribution license](https://creativecommons.org/licenses/by/4.0)*. Datasets without a valid license statement will not be accepted for publication. Machine-readable licenses allow automated data filters that give users clear guidance on the permitted use of records, thereby promoting data use and citation.

**contact**<a name="emlContact"></a><br />*Dataset metadata EML*, REQUIRED for checklist datasets<br />Contact(s) data (minimum: name and email) for at least one administrative contact for the dataset.<br />Contact data will be publicly visible at gbif.org. This information is required to ensure the possibility of communication about the dataset. The administrative contact is the person/role to be consulted about content, quality, and rights questions concerning the dataset, both by users and by central services (GBIFS). If personal contact data cannot be supplied, it is possible to supply a functional contact through a role name (e.g. "curator") and email (collections@myhouse.com). It is necessary, though, that responsibilities for handling incoming communication are clearly defined and followed internally.

**creator**<a name="emlCreator"></a><br />*Dataset metadata EML*, REQUIRED for checklist datasets<br />Contact data (minimum: name and email) for the creator(s) of the dataset (see [creator](http://web.archive.org/web/2013if_/http://knb.ecoinformatics.org/software/eml/eml-2.1.1/eml-resource.html#creator)).

**metadataProvider**<a name="emlMetadataProvider"></a><br />*Dataset metadata EML*, REQUIRED for checklist datasets<br />Contact data (minimum: name and email) for the author(s) of the dataset metadata (see [metadataProvider](http://web.archive.org/web/2013if_/http://knb.ecoinformatics.org/software/eml/eml-2.1.1/eml-resource.html#metadataProvider)).

**citation**<a name="emlCitation"></a><br />*Dataset metadata EML*, STRONGLY RECOMMENDED for checklist datasets<br />a text specifying how your dataset should be cited in publications that make use of your data.<br />
To ensure your dataset gets cited the way you want, you can explicitly specify the requested citation. This text will be displayed on the dataset page, and it will be supplied to data users together with downloads that contain any contribution from your dataset. If no text is specified, GBIF will automatically supply a standard format citation that includes the dataset name and the name of the publishing institution, together with the date of the download and a reference to gbif.org.

**projectID**<a name="emlProjectID"></a><br />*Dataset metadata EML*, REQUIRED for some checklist datasets<br />A unique identifier for the project from which a dataset is derived<br />The record type is a GUID or other identifier that is near globally unique.<br />This field is _REQUIRED for a dataset that is funded through programmes operated by GBIF. In this case, the projectID is the ID of the funded project as listed in the contract document, e.g. "BID-AF2016-0001-REG"._

**projectTitle**<a name="emlProjectTitle"></a><br />*Dataset metadata EML*, REQUIRED for some checklist datasets<br />The title of the funded project as listed in the contract document, but not containing the projectID and other administrative information, such as the [project titles listed here](/programme/82243/#projects).<br />This field is _REQUIRED for a dataset that is funded through programmes operated by GBIF_.