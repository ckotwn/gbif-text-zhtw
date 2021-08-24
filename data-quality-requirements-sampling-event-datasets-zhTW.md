https://www.gbif.org/zh-tw/data-quality-requirements-sampling-events

#### Document Control
| Date | Description | Author(s) |
| ---- | ----------- | --------- |
|  | 翻譯  | 柯智仁    |
|  | 發布  |    |


# Data quality requirements: Sampling-event datasets

By following these data quality requirements and  recommendations, data publishers can improve the quality, completeness  and value of their sampling-event datasets.

[Sampling-event datasets](/dataset-classes#samplingevents) provide greater detail about a species occurring at a given location and date, including the methods, events and relative abundance of species recorded in a sample. By improving comparisons of data collected using the same protocols at different times and places, these datasets can enable researchers to infer the absence of particular species from particular sites.

By following these data quality requirements and recommendations, data publishers can improve the quality, completeness and value of their sampling-event datasets.

### **Darwin Core records**

|Term | [Status](#status) |
|--|--|
|[eventID](#dcEventID) | Required |
|[eventDate](#dcEventDate2) | Required |
|[samplingProtocol](#dcSamplingProtocol) | Required |
|[samplingSizeValue & samplingSizeUnit](#dcSamplingSize)  | Required |
|[countryCode](#dcCountryCode2) | Strongly recommended |
|[parentEventID](#dcParentEventID) | Strongly recommended |
|[samplingEffort](#dcSamplingEffort) | Strongly recommended |
|[locationID](#dcLocationID) | Strongly recommended |
|[decimalLatitude & decimalLongitude2](#dcLatLong) | Strongly recommended |
|[geodeticDatum](#dcGeodeticDatum2) | Strongly recommended |
|[coordinateUncertaintyInMeters](#dcUncertainty2) | Strongly recommended |
|[footprintWKT](#dcFootprintWKT) | Strongly recommended |
|[occurrenceStatus](#dcOccurrenceStatus) | Strongly recommended |

## **Dataset metadata (EML)**

|Term | [Status](#status) |
|--|--|
|[title](#emlTitle3) | Required |
|[description](#emlDescription3) | Required |
|[publishing organization](#emlPublisher3) | Required |
|[type](#emlType3) | Required | 
|[license](#emlLicense3) | Required |
|[contact(s)](#emlContact3) | Required |
|[creator(s)](#emlCreator3) | Required |
|[metadata provider(s)](#emlMetadataProvider3) | Required |
|[citation](#emlCitation3) | Strongly recommended |

Note: If the dataset is funded through a programme operated by GBIF (e.g. [BID](/programme/82243), [BIFA](/programme/82629), [CESP](/programme/82219)), __two additional fields are required__:

| | |
|--|--|
|[projectID](#emlProjectID) | Required |
|[projectTitle](#emlProjectTitle) | Required |

<a name="status"></a>
### Status

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

<a name="terms"></a>
### Terms

**eventID**<a name="dcEventID"></a><br />*Darwin Core dataset element*, REQUIRED for sampling-event datasets<br />A unique identifier for the sampling event, allowing to link individual occurrences to a specific event, and to cross reference events to document e.g. time series (resampling) or synchronized sampling across a wider area (see [*Darwin Core Terms: A quick reference guide*](http://rs.tdwg.org/dwc/terms/eventID))<br />
The eventID can be a persistent global unique identifier, or an identifier specific to the dataset. Its main function is to allow linking to related data (occurrences, other sampling events, site images etc.). While dataset-specific eventIDs are sufficient to refer to occurence records published within the same dataset, it is worth considering that very simple IDs like numbers could easily reoccur in other, unrelated datasets, and make external linkages ambiguous. In addition, the eventID needs to reliably stay with the sampling event information at source, and consistently refer to the same event, or else any data links will be broken.

**eventDate**<a name="dcEventDate2"></a><br/>*Darwin Core dataset element*, REQUIRED for sampling-event datasets<br />The date or date interval during which the sampling event as a whole took place, following ISO 8601 date-time standard (see [*Darwin Core Terms: A quick reference guide*](http://rs.tdwg.org/dwc/terms/#eventDate)<br />
The date or date span of e.g. a vegetation survey, a sampling trip, or the exposure period of an insect trap if it is defined as a single, continuous event. Supply the information to the best level of detail possible, using ISO 8601 notation, but contrary to the ISO specification, *do not* include time of day, and do not use leading zeros to pad incomplete dates. The year has to be four-digit, i.e. '2016', *not* '16'. In some cases, especially for historical data, only years may be known, in other cases, full dates can be supplied. For the levels of information that are unknown, avoid padding and instead end the value, to limit ambiguity of interpretation. If, for example, only year and month are known, represent this as 2016-04, *not* as 2016-04-01. Note that the *time should not be included as part of this element*, using eventTime instead where required. 

**samplingProtocol**<a name="dcSamplingProtocol"></a><br/>*Darwin Core dataset element*, REQUIRED for sampling-event datasets<br />The name of, reference to, or description of the method or protocol used during a sample event (see [*Darwin Core Terms: A quick reference guide*](http://rs.tdwg.org/dwc/terms/samplingProtocol))<br />
Sample events typically use specific methods or follow certain protocols that standardize the sampling effort to a certain degree. Knowledge about the sampling protocol gives users additional information that is helpful for the interpretation of the attached occurrence records, e.g. what kind of organisms to expect or not expect within the dataset and whether the absence of a recording signifies absence in nature, or was outside the target group of the applied sampling methodology (e.g. "UV light trap"). If a more detailed description of the method or protocol exists, providing a reference is strongly encouraged (e.g. [*Penguins from space: faecal stains reveal the location of emperor penguin colonies*](http://dx.doi.org/10.1111/j.1466-8238.2009.00467.x). While there is no controlled vocabulary for this element, the goal is to, across datasets, gradually assemble a library of references for reuse, and to allow users to identify datasets that are based on comparable methods and protocols.

**sampleSizeValue** & **sampleSizeUnit**<a name="dcSamplingSize"></a><br/>*Darwin Core dataset element*, REQUIRED for sampling-event datasets<br />A numeric value and the corresponding unit for the value, specifying the size of an individual sample in the sampling event (see [*Darwin Core Terms: A quick reference guide*](http://rs.tdwg.org/dwc/terms/sampleSizeValue and http://rs.tdwg.org/dwc/terms/sampleSizeUnit))<br />
The two sampleSize fields always go together, and specify the size of an individual sample within a sample event. The sample size can relate to time duration, a spatial lengths (e.g. of a trawl), an area or a volume. A vegetation plot, for example, may have a sampleSizeValue of 2 with a sampleSizeUnit of "square kilometer". Recommended best practice is to use a controlled vocabulary for the sampleSizeUnit.

**countryCode**<a name="dcCountryCode2"></a><br/>*Darwin Core dataset element*, STRONGLY RECOMMENDED for sampling-event datasets<br />A two-letter standard abbreviation for the country, territory or island that the sampling event took place in (see [*Darwin Core Terms: A quick reference guide*](http://rs.tdwg.org/dwc/terms/countryCode)<br />
The country code is the proposed minimum standard to supply information about the geographic locality of the sampling event. It specifies the country, territory or island that the sampling event took place in; for countries with connections to marine areas, this includes the adjacent Exclusive Economic Zone (EEZ). The format for this field follows the ISO 3166-1-alpha-2 standard for country codes. Those are two-letter codes for each entity; lists can be found on-line. Note that for this data item, use of the codes is required, and full country names (in any language) will not be accepted. If you want to supply the [country name](http://rs.tdwg.org/dwc/terms/country) in addition, add the appropriate element.<br />
In most cases, a sampling event can be linked to a specific country. In cases where it is not possible to supply a country code (e.g. marine data outside of coastal zones, or transects spanning more than one country), geographical coordinates should be supplied instead.

**parentEventID**<a name="dcParentEventID"></a><br/>*Darwin Core dataset element*, STRONGLY RECOMMENDED for sampling-event datasets<br />A cross-reference to the eventID of a broader event, e.g. a long-term monitoring project that the specific event is a part of, or a general vegetation survey of a larger area that is comprised of a number of sub-plots (see [*Darwin Core Terms: A quick reference guide*](http://rs.tdwg.org/dwc/terms/parentEventID))
In order to be able to reference a parent event, this event needs to be specified as a separate entry, typically within the same dataset, carrying its own eventID. Refer to the eventID of the parent event in the sample event record to specify the relationship between the two entries. 

**samplingEffort**<a name="dcSamplingEffort"></a><br/>*Darwin Core dataset element*, STRONGLY RECOMMENDED for sampling-event datasets<br />The measure for the amount of effort that was expended during a sampling event (see [*Darwin Core Terms: A quick reference guide*](http://rs.tdwg.org/dwc/terms/samplingEffort))<br />
The amount of effort expended during a sampling event often has an influence on the result. It included factors like the number of observers involved, or the total time spent at collecting, the number of traps exposed over a certain amount of time, the total distance covered, and mode of transport used, while surveying a plot, etc. Examples for sampling effort are "40 trap-nights", "10 observer-hours". While there is no controlled vocabulary, the recommendation is to keep this information brief and factual, giving users enough information to compare between sampling events.

**locationID**<a name="dcLocationID"></a><br/>*Darwin Core dataset element*, STRONGLY RECOMMENDED for sampling-event datasets<br />An internal or external reference that links to a set of data describing the sample event location, if available (see [*Darwin Core Terms: A quick reference guide*](http://rs.tdwg.org/dwc/terms/locationID))<br />
Example: http://www.geonames.org/10793757/dnb-6.html. Note: if such a reference cannot be meaningfully supplied, consider supplying more location detail, e.g. through use of the data elements locality, minimumElevationInMeters, minimumDepthInMeters, stateProvince, locationRemarks (see http://rs.tdwg.org/dwc/terms/)

**decimalLatitude & decimalLongitude**<a name="dcLatLong"></a><br/>*Darwin Core dataset element*, STRONGLY RECOMMENDED for sampling-event datasets<br />The geographic latitude or longitude, resp., in decimal degrees. Where coordinate values are available, both fields need to be supplied, together with the geodetic datum (below)(see *Darwin Core Terms: A quick reference guide* on [decimalLatitude](http://rs.tdwg.org/dwc/terms/decimalLatitude), [decimalLongitude](http://rs.tdwg.org/dwc/terms/decimalLongitude))<br />
Valid values lie between -90 and 90 incl. (latitude; 0: Equator), or -180/180 incl. (longitude; 0: Greenwich Meridian). Decimal coordinate values provide a geolocation of the sample site that is much more informative than the country name alone, and that is stable over time (unlike the borders of countries). In the context of a sample event, coordinates also provide a means to consistency-check that individual, linked occurrence records fall within the site of the sample event as a whole.
Note that a sample event that spans an area rather than a point location should additionally supply the coordinateUncertaintyInMeters (see below) to specify the approximate extension of the area. In any case, coordinate information should always be qualified by the geodetic datum (see below).

**geodeticDatum**<a name="dcGeodeticDatum2"></a><br/>*Darwin Core dataset element*, STRONGLY RECOMMENDED for sampling-event datasets<br />The coordinate system and set of reference points upon which the geographic coordinates are based (see [*Darwin Core Terms: A quick reference guide*](http://rs.tdwg.org/dwc/terms/geodeticDatum))<br />
Different geodetic systems exist, and the exact locality of a point depends on which reference system the coordinates refer to. This is why the system should always be explicitly named when known: depending on the geographic region, the datum shift between two systems can vary from zero to hundreds of meters for a given point. When no value is supplied, GBIF's indexing process assumes the reference system to be WGS 84 (World Geodetic System 1984, a global approximation at sea level and, i.a., base of GPS data); but the more frequently the geodetic datum can be supplied explicitly by data publishers, the more reliable the geographic representation of occurrences will become, e.g. through datum conversion. It is likewise important to explicitly document the lack of knowledge of the system used, as this increases confidence in data interpretation.
Examples: WGS84;EPSG:4326; unknown. 

**coordinateUncertaintyInMeters**<a name="dcUncertainty2"></a><br/>*Darwin Core dataset element*, STRONGLY RECOMMENDED for sampling-event datasets<br />The horizontal distance from the given decimalLatitude and decimalLongitude in meters, describing the smallest circle containing the whole of the Location (see [*Darwin Core Terms: A quick reference guide*](http://rs.tdwg.org/dwc/terms/coordinateUncertaintyInMeters))<br />
This is an indicator for the accuracy of the coordinate location, described as the radius of a circle around the stated point location. In the context of sample events, it combines with the decimal coordinates to specify the area covered by the sample event. Note that 0 (zero) is not a valid value for this measure. If the value is unknown or not applicable, the value should be empty (null). Examples: 30; 71; [empty]. Not: 0.

**footprintWKT**<a name="dcFootprintWKT"></a><br/>*Darwin Core dataset element*, STRONGLY RECOMMENDED for sampling-event datasets<br />An alternative area description, specifying the location of the sample event in Well-known text (WKT) markup language (see [*Darwin Core Terms: A quick reference guide*](See http://rs.tdwg.org/dwc/terms/footprintWKT)) or [Wikipedia](https://en.wikipedia.org/wiki/Well-known_text))<br />
A WKT representation of the shape (footprint, geometry) that defines the location. This differs from the point-radius representation that is combined from the elements decimalLatitude, decimalLongitude and coordinateUncertaintyInMeters in that it can define shapes that are not circles. Example: a one-degree bounding box with opposite corners at (longitude=10, latitude=20) and (longitude=11, latitude=21) would be expressed in well-known text as "POLYGON ((10 20, 11 20, 11 21, 10 21, 10 20))". Note that it is possible to supply both a point-radius and a footprintWKT location for the same sample event.

**occurrenceStatus**<a name="dcOccurrenceStatus"></a><br/>*Darwin Core dataset element*, STRONGLY RECOMMENDED for sampling-event datasets<br />Note: this applies to associated occurrence data, not to the sample event itself. A qualifier for individual occurrence records, marking a taxon as either present or absent at a location during the sampling event (see [*Darwin Core Terms: A quick reference guide*](http://rs.tdwg.org/dwc/terms/occurrenceStatus))<br />
Since sample datasets document the sampling effort exerted during the event, it can often be valuable to not only document taxa as being present (observed, collected) at the location at the time, but also to record negative occurrences (absences) for taxa that could be reasonably expected, but were not encountered in the event. An example is a floristic survey that estimates the abundance or coverage of plants in a certain area, working from a list of species that were encountered on earlier surveys of that same region. Recommendation: used the standard values of either "present" or "absent" to mark individual occurrence records. Note that absence records are currently not handled in the GBIF indexing processes, but that this is part of the medium term plans; that fact that processing is not yet implemented on that side does not hinder the collection and publication of absence data, making them available through the published dataset at source.

#### **Dataset metadata (EML)**

**title**<a name="emlTitle3"></a><br />*Dataset metadata EML*, REQUIRED for sampling-event datasets<br />The title under which the dataset will be published at gbif.org<br /> 
Recommendation: a brief, but descriptive title that characterizes the dataset in an international context and distinguishes it from similar datasets in other institutions. E.g. " Israeli Butterfly Monitoring Scheme (BMS-IL)". Not recommended: "Butterflies". The title will, i.a., be part of the dataset citation on use of the data.

**description**<a name="emlDescription3"></a><br />*Dataset metadata EML*, REQUIRED for sampling-event datasets<br />An English language text, describing the dataset.<br />
This may include a longer version of title, a description of geographic, temporal and taxonomic scope of the dataset, methodology and purpose of the underlying data compilation (e.g. protected habitat surveillance, faunistic inventory, deep sea trawl data), relevant literature references, and any other information you consider relevant to characterize the dataset. A second version of the description in another language than English may be added underneath. 

**publishing organization**<a name="emlPublisher3"></a><br />*Dataset metadata EML*, REQUIRED for sampling-event datasets<br />The title of the institution or organization that will be listed as the data publisher at gbif.org<br />The publishing organization is the institution which holds or owns the dataset and is in charge of its contents and maintenance. The title given should be the official title of the organization as registered with relevant authorities, listed on websites, and, if applicable, as stated in the project contract.

**type**<a name="emlType3"></a><br />*Dataset metadata EML*, REQUIRED for sampling-event datasets<br />The type of the dataset. Here: "samplingEvent".<br />
The record type describes the main focus of all records contained in the dataset (core records). For a sample event dataset, the record type will always be "samplingEvent". There should also be occurrences linked to sample event records. The structure and requirements for this linked information follows the guidelines given for occurrence data publication [link].

**license**<a name="emlLicense3"></a><br />*Dataset metadata EML*, REQUIRED for sampling-event datasets<br />A machine-readable statement of the rights attached to the published dataset. Use either CC0 or CC BY.<br />
_Note: All datasets funded under the [BID](/programme/82243) and [BIFA programmes](/programme/82629/) must be published under either a Creative Commons [CC0 rights waiver](https://creativecommons.org/about/cc0) or a [CC BY Attribution license](https://creativecommons.org/licenses/by/4.0)_. Datasets without a valid license statement will not be accepted for publication. Machine-readable licenses allow automated data filters that give users clear guidance on the permitted use of records, thereby promoting data use and citation.

**contact(s)**<a name="emlContact3"></a><br />*Dataset metadata EML*, REQUIRED for sampling-event datasets<br />Contact data (minimum: name and email) for at least one administrative contact for the dataset<br />
Contact data will be publicly visible at gbif.org. This information is required to ensure the possibility of communication about the dataset. The administrative contact is the person/role to be consulted about content, quality, and rights questions concerning the dataset, both by users and by central services (GBIFS). If personal contact data cannot be supplied, it is possible to supply a functional contact through a role name (e.g. "curator") and email (collections@myhouse.com). It is necessary, though, that responsibilities for handling incoming communication are clearly defined and followed internally.

**creator(s)**<a name="emlCreator3"></a><br />*Dataset metadata EML*, REQUIRED for sampling-event datasets<br />Contact data (minimum: name and email) for the creator of the dataset (see [link])

**metadata provider(s)**<a name="emlMetadataProvider3"></a><br />*Dataset metadata EML*, REQUIRED for sampling-event datasets<br />Contact data (minimum: name and email) for the author of the dataset metadata (see [link])

**citation**<a name="emlCitation3"></a><br />*Dataset metadata EML*, STRONGLY RECOMMENDED for sampling-event datasets<br />A text specifying how your dataset should be cited in publications that make use of your data.<br />To ensure your dataset gets cited the way you want, you can explicitly specify the requested citation. This text will be displayed on the dataset page, and it will be supplied to data users together with downloads that contain any contribution from your dataset. If no text is specified, GBIF will automatically supply a standard format citation that includes the dataset name and the name of the publishing institution, together with the date of the download and a reference to gbif.org.


**projectID**<a name="emlProjectID"></a><br />*Dataset metadata EML*, REQUIRED for some sampling-event datasets<br />A unique identifier for the project from which a dataset is derived<br />The record type is a GUID or other identifier that is near globally unique.<br />This field is _REQUIRED for a dataset that is funded through programmes operated by GBIF. In this case, the projectID is the ID of the funded project as listed in the contract document, e.g. "BID-AF2016-0001-REG"._


**projectTitle**<a name="emlProjectTitle"></a><br />*Dataset metadata EML*, REQUIRED for some sampling-event datasets<br />The title of the funded project as listed in the contract document, but not containing the projectID and other administrative information, such as the [project titles listed here](/programme/82243/#projects).<br />This field is _REQUIRED for a dataset that is funded through programmes operated by GBIF_.