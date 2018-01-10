## Rubric-related entities

### <a name="rubric"></a>C.X Rubric

A Caliper [Rubric](#rubric) represents . . . \[TODO\] add description.

#### IRI
http://purl.imsglobal.org/caliper/Rubric

#### Supertype
[DigitalResourceCollection](#digitalResourceCollection), [DigitalResource](#digitalResource)

#### Properties
[Rubric](#rubric) inherits all the properties and requirements defined by its supertypes [DigitalResourceCollection](#digitalResourceCollection) and [DigitalResource](#digitalResource).  Additional requirements are described below:

| Property | Type | Description | Disposition |
| :------- | :--- | ----------- | :---------: |
| id | [IRI](#iriDef) | A valid [IRI](#iriDef) MUST be specified. The [IRI](#iriDef) MUST be unique and persistent. The [IRI](#iriDef) SHOULD also be dereferenceable, i.e., capable of returning a representation of the resource. A [URI](#uriDef) employing the [URN](#urnDef) scheme MAY be provided in cases where a [Linked Data](#linkedDataDef) friendly HTTP URI is either unavailable or inappropriate. | Required |
| type | [Term](#termDef) | The string value MUST be set to the [Term](#termDef) *Rubric*. | Required |
| name | string | A string value comprising a word or phrase by which the [Rubric](#rubric) is known. | Optional |
| description | string |  A string value comprising a brief, written representation of the [Rubric](#rubric). | Optional |
| creators | Array | An ordered collection of [Agent](#agent) entities, typically of type [Person](#person), that are responsible for bringing this [Rubric](#rubric) into being.  Each array item MUST be expressed either as an object or as a string corresponding to the item's [IRI](#iriDef). | Optional |
| mediaType | string | A string value drawn from the list of [IANA](https://www.iana.org/assignments/media-types/media-types.xhtml) approved media types and subtypes that identifies the file format of this [Rubric](#rubric). | Optional |
| keywords | Array | An ordered collection of one or more string values that represent tags or labels used to identify the [Rubric](#rubric). | Optional |
| learningObjectives | Array | An ordered collection of one or more [LearningObjective](#learningobjective) entities that describe what a learner is expected to comprehend or accomplish after engaging with this [Rubric](#rubric).  Each array item MUST be expressed either as an object or as a string corresponding to the item's [IRI](#iriDef). | Optional |
| isPartOf | [Entity](#entity) &#124; [IRI](#iriDef) | A related resource that includes or incorporates this [Rubric](#rubric) as a part of its whole.  The `isPartOf` value MUST be expressed either as an object or as a string corresponding to the associated entity's [IRI](#iriDef). | Optional |
| items | Array | An ordered collection of [RubricItem](#rubricItem) entities.  Each array item MUST be expressed either as an object or as a string corresponding to the item's [IRI](#iriDef). | Optional |
| dateCreated | DateTime | An ISO 8601 date and time value expressed with millisecond precision that describes when the [Rubric](#rubric) was created.  The value MUST be expressed using the format YYYY-MM-DDTHH:mm:ss.SSSZ set to UTC with no offset specified. | Optional |
| dateModified | DateTime | An ISO 8601 date and time value expressed with millisecond precision that describes when the [Rubric](#rubric) was last changed or modified.  The value MUST be expressed using the format YYYY-MM-DDTHH:mm:ss.SSSZ set to UTC with no offset specified. | Optional |
| datePublished | DateTime | An ISO 8601 date and time value expressed with millisecond precision that provides the publication date of the [Rubric](#rubric).  The value MUST be expressed using the format YYYY-MM-DDTHH:mm:ss.SSSZ set to UTC with no offset specified. | Optional |
| version | string | A string value that designates the current form or version of the [Rubric](#rubric). | Optional |
| extensions | Object | A map of additional attributes not defined by the model MAY be specified for a more concise representation of the [Rubric](#rubric). | Optional |

#### Example
```
{ }
```

### <a name="rubricItem"></a>C.4 RubricItem

A Caliper [RubricItem](#rubricItem) represents a . . . \[TODO\] add description.

#### IRI
http://purl.imsglobal.org/caliper/RubricItem

#### Supertype
[DigitalResource](#digitalResource)

#### Properties
[RubricItem](#rubricItem) inherits all the properties and requirements defined by its supertype [DigitalResource](#digitalResource).  Additional requirements are described below:

| Property | Type | Description | Disposition |
| :------- | :--- | ----------- | :---------: |
| id | [IRI](#iriDef) | A valid [IRI](#iriDef) MUST be specified. The [IRI](#iriDef) MUST be unique and persistent. The [IRI](#iriDef) SHOULD also be dereferenceable, i.e., capable of returning a representation of the resource. A [URI](#uriDef) employing the [URN](#urnDef) scheme MAY be provided in cases where a [Linked Data](#linkedDataDef) friendly HTTP URI is either unavailable or inappropriate. | Required |
| type | [Term](#termDef) | The string value MUST be set to the [Term](#termDef) *RubricItem*. | Required |
| name | string | A string value comprising a word or phrase by which the [RubricItem](#rubricItem) is known. | Optional |
| description | string |  A string value comprising a brief, written representation of the [RubricItem](#rubricItem). | Optional |
| creators | Array | An ordered collection of [Agent](#agent) entities, typically of type [Person](#person), that are responsible for bringing this [RubricItem](#rubricItem) into being.  Each array item MUST be expressed either as an object or as a string corresponding to the item's [IRI](#iriDef). | Optional |
| mediaType | string | A string value drawn from the list of [IANA](https://www.iana.org/assignments/media-types/media-types.xhtml) approved media types and subtypes that identifies the file format of this [RubricItem](#rubricItem). | Optional |
| keywords | Array | An ordered collection of one or more string values that represent tags or labels used to identify the [RubricItem](#rubricItem). | Optional |
| learningObjectives | Array | An ordered collection of one or more [LearningObjective](#learningobjective) entities that describe what a learner is expected to comprehend or accomplish after engaging with this [RubricItem](#rubricItem).  Each array item MUST be expressed either as an object or as a string corresponding to the item's [IRI](#iriDef). | Optional |
| isTimeDependent | Boolean | A boolean value indicating whether or not interacting with the item is time dependent. | Optional |
| isPartOf | [Entity](#entity) &#124; [IRI](#iriDef) | A related [Entity](#entity), typically an [Rubric](#rubric), that includes or incorporates the [RubricItem](#rubricItem) as a part of its whole.  The `isPartOf` value MUST be expressed either as an object or as a string corresponding to the associated entity's [IRI](#iriDef). | Optional |
| dateCreated | DateTime | An ISO 8601 date and time value expressed with millisecond precision that describes when the [RubricItem](#rubricItem) was created.  The value MUST be expressed using the format YYYY-MM-DDTHH:mm:ss.SSSZ set to UTC with no offset specified. | Optional |
| dateModified | DateTime | An ISO 8601 date and time value expressed with millisecond precision that describes when the [RubricItem](#rubricItem) was last changed or modified.  The value MUST be expressed using the format YYYY-MM-DDTHH:mm:ss.SSSZ set to UTC with no offset specified. | Optional |
| datePublished | DateTime | An ISO 8601 date and time value expressed with millisecond precision that provides the publication date of the [RubricItem](#rubricItem).  The value MUST be expressed using the format YYYY-MM-DDTHH:mm:ss.SSSZ set to UTC with no offset specified. | Optional |
| version | string | A string value that designates the current form or version of the [RubricItem](#rubricItem). | Optional |
| extensions | Object | A map of additional attributes not defined by the model MAY be specified for a more concise representation of the [RubricItem](#rubricItem). | Optional |

#### Example
```
{ }
```

<a rel="license" href="http://creativecommons.org/licenses/by-nd/4.0/">
<img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nd/4.0/88x31.png" /></a>
<br />
This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nd/4.0/">Creative Commons Attribution-NoDerivatives 4.0 International License</a>.
