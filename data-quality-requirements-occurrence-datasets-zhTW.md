https://www.gbif.org/zh-tw/data-quality-requirements-occurrences

#### Document Control
| Date | Description | Author(s) |
| ---- | ----------- | --------- |
|  | 翻譯  | 柯智仁    |
|  | 發布  |    |

# Data quality requirements: Occurrence datasets

By following these data quality requirements and  recommendations, data publishers can improve the quality, completeness  and value of their occurrence datasets.

​     

[Occurrence datasets](/dataset-classes#occurrences) make up the core of data published through GBIF.org, offering evidence of the occurrence of a species (or other taxon) at a particular place on a specified date.

By following these data quality requirements and recommendations, data publishers can improve the quality, completeness and value of their occurrence datasets.

### **Darwin Core records**

|Term | [Status](#status) |
|--|--|
|[occurrenceID](#dcOccurrenceID) | Required |
|[basisOfRecord](#dcBasis) | Required |
|[scientificName](#dcSciName) | Required |
|[eventDate](#dcEventDate) | Required |
|[countryCode](#dcCountryCode) | Strongly recommended |
|[taxonRank](#dcTaxonRank) | Strongly recommended |
|[kingdom](#dcKingdom) | Strongly recommended | 
|[decimalLatitude & decimalLongitude](#dcLatLong) | Strongly recommended |
|[geodeticDatum](#dcGeodeticDatum) | Strongly recommended |
|[coordinateUncertaintyInMeters](#dcUncertainty) | Strongly recommended |
|[individualCount, organismQuantity & organismQuantityType](#dcCount) | Strongly recommended |
|[informationWithheld](#dcWithheld) | Share if available |
|[dataGeneralizations](#dcGeneralizations) | Share if available |
|[eventTime](#dcEventTime) | Share if available |
|[country](#dcCountry) | Share if available |

### **Dataset metadata (EML)**

|Term | [Status](#status) |
|--|--|
|[title](#emlTitle) | Required |
|[description](#emlDescription) | Required |
|[publishing organization](#emlPublisher) | Required |
|[type](#emlType) | Required | 
|[license](#emlLicense) | Required |
|[contact(s)](#emlContact) | Required |
|[creator(s)](#emlCreator) | Required |
|[metadata provider(s)](#emlMetadataProvider) | Required |
|[citation](#emlCitation) | Strongly recommended |
|[additional metadata](#emlAdditional) | Share if available |

Note: If the dataset is funded through a programme operated by GBIF (e.g. [BID](/programme/82243), [BIFA](/programme/82629), [CESP](/programme/82219)), __two additional fields are required__:

| | |
|--|--|
|[projectID](#emlProjectID) | Required |
|[projectTitle](#emlProjectTitle) | Required |

### Status<a name="status"></a>

#### Required information

The items listed below constitute the minimum formal requirements for publishing an occurrence dataset. GBIF.org will not accept a dataset without these terms and will not index the records. While these items are mandatory for publishing the dataset at all, they are only the starting point. The usefulness of the published data will still be severely limited unless additional information is supplied.

#### Strongly recommended

In addition to the mandatory data elements, we strongly recommend completing several more  fields that help improve the usefulness of the dataset because:
+ some information supports the integration into a global data resource and prevents ambiguity, e.g. in matching scientific names that could apply to more than one organism (homonyms) to the correct place within the backbone taxonomy
+ more precise geo-location data (coordinates) significantly increase the usefulness of the data for a wide range of use cases
+ additional qualifiers for some data elements, e.g. coordinates, support the interpretation of those elements and help users to better estimate their usefulness for a given data use case
+ some data redundancy supports quality control and error detection (e.g. testing country codes against coordinates where both are supplied)
+ last not least, the richer the spectrum of available information of a dataset is, the more potential usage areas it becomes available for, meaning the dataset will me more widely accessible and used and cited more often

#### Share if available

If additional data are available, consider sharing them in order to increase the usefulness of your published data.

### Terms

**occurrenceID**<a name="dcOccurrenceID"></a><br />*Darwin Core dataset element*, REQUIRED for occurrence-only datasets<br />A unique identifier for the occurrence, allowing the same occurrence to be recognized across dataset versions as well as through data downloads and use (see [*Darwin Core Terms: A quick reference guide*](http://rs.tdwg.org/dwc/terms/#occurrenceID))<br />Ideally, the occurrenceID is a persistent global unique identifier. As a minimum requirement, it has to be unique within the published dataset. It allows to recognize the same occurrence over time when the dataset indexing is refreshed; it links additional data like images; and it makes it possible to cite records e.g. in usage reports or in publications. This means that the occurrenceID needs to reliably stay with the occurrence at source, and to consistently refer to the same occurrence in published datasets and any underlying source data.

**basisOfRecord**<a name="dcBasis"></a><br />*Darwin Core dataset element*, REQUIRED for occurrence-only datasets<br />The type of the individual record, e.g. observation, physical specimen, fossil, living ex-situ, culture collection specimen (note the [metadata entry](#emlBasis) above as well as [*Darwin Core Terms: A quick reference guide*](http://rs.tdwg.org/dwc/terms/#basisOfRecord)<br />Even if the basis of record is supplied for the dataset as a whole, it is recommended practice to add it to each individual record as well to make the information explicitly available, e.g. in downloads containing data from a range of different datasets.

**scientificName**<a name="dcSciName"></a><br />*Darwin Core dataset element*, REQUIRED for occurrence-only datasets<br />The full scientific name of the organism, to the lowest level taxonomic rank that is possible to supply, and including authorship and year of the name where applicable<br />The scientific name is one of the most important and frequently used search criteria for data access, and is indispensable for identifying the biological organism that is at the center of any occurrence record (see [*Darwin Core Terms: A quick reference guide*](http://rs.tdwg.org/dwc/terms/scientificName). As occurrence records are the evidence of the occurrence of a species (or other taxa) at a particular place on a specified date, the scientific name is one of the core pieces of information required for any record. Ideally, the name supplied is at species level or below. If the determination only allows for information on a higher level, this is acceptable as well. Valid scientific names are Latin names following the syntax rules of the respective taxon group (e.g. botanical nomenclature). Not permitted are, i.e., working names ("*Mallomonas* sp.4"), common names ("fruit fly"), or names containing identification qualifiers ("*Anemone cf. nemorosa*").

**eventDate**<a name="dcEventDate"></a><br />*Darwin Core dataset element*, REQUIRED for occurrence-only datasets<br />The date or date interval during which the occurrence record was collected, following ISO 8601 date-time standard (see [*Darwin Core Terms: A quick reference guide*](http://rs.tdwg.org/dwc/terms/#eventDate))<br />The date span e.g. of a sampling trip, if the exact date of the occurrence event cannot be determined to the day, or else the precise date.  Supply the information to the best level of detail possible, using ISO 8601 notation, but contrary to the ISO specification, *do not* include time of day, and do not use leading zeros to pad incomplete dates. The year has to be four-digit, i.e. '2016', *not* '16'. In some cases, especially for historical data, only years may be known, in other cases, full dates can be supplied. For the levels of information that are unknown, avoid padding and instead end the value, to limit ambiguity of interpretation. If, for example, only year and month are known, represent this as 2016-04, *not* as 2016-04-01. Note that the *time should not be included as part of this element*, using eventTime instead where required.

**countryCode**<a name="dcCountryCode"></a><br />*Darwin Core dataset element*, STRONGLY RECOMMENDED for occurrence-only datasets<br />A two-letter standard abbreviation for the country of the occurrence locality (see [*Darwin Core Terms: A quick reference guide*](http://rs.tdwg.org/dwc/terms/countryCode). As the third core part of the documentation of a taxon occurrence, information on the collection or observation locality (geographic reference) is essential for any record. The country code is the proposed minimum standard to supply this information. The format for this field follows the [ISO 3166-1-alpha-2 standard for country codes](https://www.iso.org/iso-3166-country-codes.html). Those are two-letter codes for each country; lists can be found on-line. Note that for this data item, use of the codes is required, and full country names (in any language) will not be accepted. Publishers who wish to supply the country name in addition may add the [appropriate element](http://rs.tdwg.org/dwc/terms/country). In most cases, occurrences can be linked to a specific country. In cases where it is not possible to supply a country code (e.g. marine data outside of coastal zones), geographical coordinates should be supplied instead. 

**taxonRank**<a name="dcTaxonRank"></a><br />*Darwin Core dataset element*, STRONGLY RECOMMENDED for occurrence-only datasets<br />The taxonomic rank of the supplied scientific name (see [*Darwin Core Terms: A quick reference guide*](http://rs.tdwg.org/dwc/terms/taxonRank))
The taxon rank supports the interpretation of the scientific name during indexing, and supports matching the occurrence record to the core taxonomy, especially in the case of names at genus level or above (monomials). While the format of higher taxon names in some groups contains indicators of their rank, this is not consistent across or even within groups, and cannot be reliably used for interpretation. For placing names correctly, explicitly specifying the taxon rank, alongside information on the higher taxonomy, is an important criterion. For practical purposes, the ranks used have to be (major) Linnean ranks: kingdom, phylum, class, order, family, genus, species. Both Latin or English terms are accepted.

**kingdom**<a name="dcKingdom"></a><br />*Darwin Core dataset element*, STRONGLY RECOMMENDED for occurrence-only datasets<br />the full scientific name specifying the kingdom that the occurrence's scientific name is classified under (see [*Darwin Core Terms: A quick reference guide*](http://rs.tdwg.org/dwc/terms/kingdom) and other higher taxonomy, if possible<br />
With scientific names, there are numerous cases where the matching of a given name against the core taxonomy is unsure or ambiguous. This is the case, for example, with homonyms (identical names exist for different organisms, usually across groups), newly described names that are not yet part of the existing taxonomic tree, or spelling variants (typos, hyphenation etc). To support exact matching of a scientific name against the core taxonomy, additional names at higher ranks help interpretation and error prevention.
Names should be scientific (latin) names at major Linnean ranks, like "Animalia" (kingdom) or "Rosaceae" (family). *Not*: common names ("animals"), abbreviations ("Rosac."), intermediate rank levels ("Tetrapoda" (superclass)), or polyphyletic or non-taxonomic groupings ("algae", "herbivora").

**decimalLatitude** & **decimalLongitude**<a name="dcLatLong"></a><br />*Darwin Core dataset element*, STRONGLY RECOMMENDED for occurrence-only datasets<br />The geographic latitude or longitude, resp., in decimal degrees. Where coordinate values are available, both fields need to be supplied (see *Darwin Core Terms: A quick reference guide* on [latitude](http://rs.tdwg.org/dwc/terms/decimalLatitude) and [longitude](http://rs.tdwg.org/dwc/terms/decimalLongitude)<br />
Valid values lie between -90 and 90 incl. (latitude; 0: Equator), or -180/180 incl. (longitude; 0: Greenwich Meridian). Decimal coordinate values provide a geolocation of the occurrence that is much more informative than the country name alone, and that is stable over time (unlike the borders of countries). Many data use cases require coordinates if the data are to be of value or usable at all, for example species distribution modeling or population studies in specific areas.
A number of issues concerning coordinates are encountered frequently. While the indexing process makes efforts to identify such cases and propose corrections, e.g. by plausibility-testing coordinates against country names, attention is needed already at the level of data preparation and publication. Such issues include: transformation errors (resulting from e.g. conversion of degrees-minutes-seconds into decimal values), accidental swapping of values, either in the dataset or during the mapping process (latitude and longitude are reversed), or negation of values (transposition of locations from north to south, east to west or vice versa through the accidental or systematic loss or addition of minus-values). Additional points to keep in mind during data preparation are technical defaults (e.g. database settings substituting 0-values instead of unknown values resulting in records supplying lat/long as 0/0; over-precision of data by automatic number-padding (lat -17.79200000 where lat -17.792 would be appropriate), or the need to blur coordinate precision for e.g. the protection of sensitive species. Also note that gridded data, i.e. where coordinates represent centroids of grid cells in a field survey rather than the actual occurrence locality, may be better represented by publishing the dataset as sample data rather than as occurrence records. Especially in such cases, it is essential to also supply the [coordinateUncertaintyInMeters](#dcUncertainty).

**geodeticDatum**<a name="dcGeodeticDatum"></a><br />*Darwin Core dataset element*, STRONGLY RECOMMENDED for occurrence-only datasets<br />The coordinate system and set of reference points upon which the geographic coordinates are based (see [*Darwin Core Terms: A quick reference guide*](http://rs.tdwg.org/dwc/terms/geodeticDatum)<br />
Different geodetic systems exist, and the exact locality of a point depends on which reference system the coordinates refer to. This is why the system should always be explicitly named when known: depending on the geographic region, the datum shift between two systems can vary from zero to hundreds of meters for a given point. When no value is supplied, GBIF's indexing process assumes the reference system to be WGS 84 (World Geodetic System 1984, a global approximation at sea level and, i.e., base of GPS data); but the more frequently the geodetic datum can be supplied explicitly by data publishers, the more reliable the geographic representation of occurrences will become, e.g. through datum conversion. It is likewise important to explicitly document the lack of knowledge of the system used, as this increases confidence in data interpretation. Examples: WGS84;EPSG:4326; unknown. 

**coordinateUncertaintyInMeters**<a name="dcUncertainty"></a><br />*Darwin Core dataset element*, STRONGLY RECOMMENDED for occurrence-only datasets<br />The horizontal distance from the given decimalLatitude and decimalLongitude in meters, describing the smallest circle containing the whole of the Location (see [*Darwin Core Terms: A quick reference guide*](http://rs.tdwg.org/dwc/terms/coordinateUncertaintyInMeters))<br />
This is an indicator for the accuracy of the coordinate location, described as the radius of a circle around the stated point location. It allows to estimate the potential distance of the real occurrence location from the recorded values, and largely depends on the methodology used in coordinate determination. Thus, the value may be specific to or estimated from the methodology or device used for geolocating, e.g. 30 (reasonable lower limit of a GPS reading under good conditions if the actual precision was not recorded at the time). Note that 0 (zero) is not a valid value for this measure. If the value is unknown or not applicable, the value should be empty (null). If for some reason the coordinateUncertaintyInMeters was artificially increased, for example by rounding the coordinate values, the fields informationWithheld or dataGeneralizations must be filled in addition. Examples: 30; 71; [empty]. Not: 0.

**individualCount, organismQuantity & organismQuantityType**<a name="dcCount"></a><br />*Darwin Core dataset element*, STRONGLY RECOMMENDED for occurrence-only datasets<br />To record the quantity of a species occurrence, e.g. as the number of individuals, percentage of vegetation coverage, or the biomass (see *Darwin Core Terms: A quick reference guide* on [individualCount](http://rs.tdwg.org/dwc/terms/individualCount), [organismQuantity](http://rs.tdwg.org/dwc/terms/organismQuantity) and [organismQuantityType](http://rs.tdwg.org/dwc/terms/organismQuantityType)<br />
In many cases, a single occurrence record represents more than one individual, and for uses like population studies, this information is interesting to users of data. A record could, for example, represent a flock of birds, a beech forest, a plankton sample, or a herbarium sheet with several specimens of a given species of grass. If the dataset derives from standard protocols for measuring and monitoring biodiversity (e.g. a vegetation transect, a bird census, or freshwater and marine sampling), first of all **check whether the dataset type of sampling-event data may be more appropriate to use**, and if yes, continue [there](/dataset-classes#samplingevents). If the purpose is to document the occasional individual count or batch size, or if there is no uniform underlying sampling protocol to the dataset, then such counts can be documented within an occurrence dataset. Use the individualCount element if all such counts concern individual organisms, or else add the quantity type information to the dataset and map the numbers to the organismQuantity element, and the type to the organismQuantityType. Examples: individualCount: "5". Or: organismQuantity: "5"/ organismQuantityType: "individuals". organismQuantity: "r" / organismQuantityType: "BraunBlanquetScale".

**informationWithheld**<a name="dcWithheld"></a><br />*Darwin Core dataset element*, SHARE IF AVAILABLE for occurrence-only datasets<br />See http://rs.tdwg.org/dwc/terms/informationWithheld

**dataGeneralizations**<a name="dcGeneralizations"></a><br />*Darwin Core dataset element*, SHARE IF AVAILABLE for occurrence-only datasets<br />See http://rs.tdwg.org/dwc/terms/dataGeneralizations

**eventTime**<a name="dcEventTime"></a><br />*Darwin Core dataset element*, SHARE IF AVAILABLE for occurrence-only datasets<br />See http://rs.tdwg.org/dwc/terms/eventTime

**country**<a name="dcCountry"></a><br />*Darwin Core dataset element*, SHARE IF AVAILABLE for occurrence-only datasets<br />See http://rs.tdwg.org/dwc/terms/country

**title**<a name="emlTitle"></a><br />*Dataset metadata EML*, REQUIRED for occurrence-only datasets<br />The title displayed for the dataset on GBIF.org<br />Recommended: a brief, but descriptive title that characterizes the dataset in an international context and distinguishes it from similar datasets in other institutions, e.g., 'Birds fallen at Danish Lighthouses 1883 through 1939', rather than "Birds". The title will be part of the dataset citation on use of the data.

**description**<a name="emlDescription"></a><br />*Dataset metadata EML*, REQUIRED for occurrence-only datasets<br />An English language text describing the dataset<br />This may include a longer version of title, a description of geographic, temporal and taxonomic scope of the collection, methodology and purpose of the underlying project or collection, relevant literature references, and any other information you consider relevant to characterize the dataset. A second version of the description in another language than English may be added underneath

**publishing organization**<a name="emlPublisher"></a><br />*Dataset metadata EML*, REQUIRED for occurrence-only datasets<br />The name of the institution or organization listed as the data publisher on GBIF.org<br />The publishing organization is the institution which holds or owns the dataset and is in charge of its contents and maintenance. The title given should be the official title of the organization as registered with relevant authorities, listed on websites, and, if applicable, as stated in the project contract.

**type**<a name="emlType"></a><br />*Dataset metadata EML*, REQUIRED for occurrence-only datasets<br />The type, or class, of the dataset<br />The record type describes the 'core' or main focus of all records contained in a given dataset. For an occurrence-only dataset, the value here will always be "occurrence". *N.B.: Occurrences may also appear as part of checklists and sample-event datasets.*

**license**<a name="emlLicense"></a><br />*Dataset metadata EML*, REQUIRED for occurrence-only datasets<br />A machine-readable statement of the rights assigned to the published dataset<br />Datasets without a valid license statement will not be accepted for publication. Machine-readable licenses allow automated data filters and give users clear guidance on permitted uses of the data, thereby promoting data use and citation. *Note: All datasets funded under the [BID](/programme/82243) and [BIFA programmes](/programme/82629/) must be published under either a Creative Commons [CC0 rights waiver](https://creativecommons.org/about/cc0) or a [CC BY Attribution license](https://creativecommons.org/licenses/by/4.0).*

**contact(s)**<a name="emlContact"></a><br />*Dataset metadata EML*, REQUIRED for occurrence-only datasets<br />Contact data—at least a name and email—for at least one administrative contact for the dataset<br />Contact data will be publicly visible at gbif.org. This information is required to ensure the possibility of communication about the dataset. The administrative contact is the person/role to be consulted about content, quality, and rights questions concerning the dataset, both by users and by the GBIF Secretariat. If personal contact data cannot be supplied, it is possible to supply a functional contact through a role name (e.g. "Curator") and email (e.g. collections@museum.org). It is necessary, though, that responsibilities for handling incoming communication are clearly defined and followed internally.

**creator(s)**<a name="emlCreator"></a><br />*Dataset metadata EML*, REQUIRED for occurrence-only datasets<br />The full name of the person, organization, or position who created the resource (see [Ecological Metadata Language (EML) Specification](https://knb.ecoinformatics.org/#external//emlparser/docs/eml-2.1.1/./eml-resource.html#creator)).

**metadata provider(s)**<a name="emlMetadataProvider"></a><br />*Dataset metadata EML*, REQUIRED for occurrence-only datasets<br />The full name of the person, organization, or position who created documentation for the resource (see [Ecological Metadata Language (EML) Specification](https://knb.ecoinformatics.org/#external//emlparser/docs/eml-2.1.1/./eml-resource.html#metadataProvider)). 

**citation**<a name="emlCitation"></a><br />*Dataset metadata EML*, STRONGLY RECOMMENDED for occurrence-only datasets<br />–A text specifying how your dataset should be cited in publications that make use of your data (see [Ecological Metadata Language (EML) Specification](https://knb.ecoinformatics.org/#external//emlparser/docs/eml-2.1.1/./eml.html#citation)).<br />
To ensure your dataset gets cited the way you want, you can explicitly specify the requested citation. This text will be displayed on the dataset page, and it will be supplied to data users together with downloads that contain any contribution from your dataset. If no text is specified, GBIF will automatically supply a standard format citation that includes the dataset name and the name of the publishing institution, together with the date of the download and a reference to gbif.org. A resource that describes a literature citation that one might find in a bibliography.

**additional metadata**<a name="emlAdditional"></a><br />*Dataset metadata EML*, SHARE IF AVAILABLE for occurrence-only datasets<br />Enrich the description and improve the fitness of use of your dataset<br />See [complete description of all supported elements](https://github.com/gbif/ipt/wiki/IPT2ManualNotes.wiki#basic-metadata).

**projectID**<a name="emlProjectID"></a><br />*Dataset metadata EML*, REQUIRED for some occurrence-only datasets<br />A unique identifier for the project from which a dataset is derived<br />The record type is a GUID or other identifier that is near globally unique.<br />This field is _REQUIRED for a dataset that is funded through programmes operated by GBIF. In this case, the projectID is the ID of the funded project as listed in the contract document, e.g. "BID-AF2016-0001-REG"._

**projectTitle**<a name="emlProjectTitle"></a><br />*Dataset metadata EML*, REQUIRED for some occurrence-only datasets<br />The title of the funded project as listed in the contract document, but not containing the projectID and other administrative information, such as the [project titles listed here](/programme/82243/#projects).<br />This field is _REQUIRED for a dataset that is funded through programmes operated by GBIF_.