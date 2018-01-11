# IMS Caliper Rubric-related entities (draft)

## Rationale
Currently, Caliper provides no vocabulary for describing performance expectations for a given [AssignableDigitalResource](#AssignableDigitalResource) or a way of linking a [Result](#result) or a [Score](#score) to the underlying evaluative criteria employed in the scoring process.  We propose extending the Caliper vocabulary with a set of Rubric-related entities . . . .  \[TODO\ rationale]

## Telemetry
\[TODO\]
* Link a [Rubric](./rubric.md) [AssignableDigitalResource](#AssignableDigitalResource), [Result](#result) or a [Score](#score) in order to simplify analysis of performance criteria.
* Track a learner who views a [Rubric](./rubric.md) associated with an [AssignableDigitalResource](#AssignableDigitalResource), [Result](#result) or a [Score](#score).
* Track an Instructor who creates, edits or deletes a [Rubric](./rubric.md) and or [RubricItem](./rubricItem) and/or links a [Rubric](./rubric.md) to an [AssignableDigitalResource](#assignableDigitalResource).

## Proposed vocabulary additions:

### Rubric
A Caliper [Rubric](./rubric.md) represents . . . \[TODO define \].

#### Supertype
[DigitalResourceCollection](#digitalResourceCollection)

#### JSON-LD term mapping
```
{
  "Rubric": "caliper:Rubric"
}
```

### RubricItem
A Caliper [RubricItem](./rubricItem.md) represents . . . \[TODO define \].

#### Supertype
[DigitalResource](#digitalResource)

#### JSON-LD term mapping
```
{
  "RubricItem": "caliper:RubricItem"
}
```

### rubric
An optional Caliper Object property of type [Rubric](#rubric) that will be added to [AssignableDigitalResource](#assignableDigitalResource), [
Result](#result) and [Score](#score).

#### JSON-LD term mapping
```
{
  "rubric": {"@id": "caliper:rubric", "@type": "@id"}

}
```

## Profiles, Events and Entities impacted
| Profiles | Events | Entities |
| :------- | :--- | ----------- |
| [Assessment Profile](#assessmentProfile) | [AssessmentEvent](#assessmentEvent), [AssessmentItemEvent](#assessmentItemEvent) | [Assessment](#assessment), [AssessmentItem](#assessmentItem) |
| [Assignable Profile](#assignableProfile) | [AssignableEvent](#assignableEvent) | [AssignableDigitalResource](#assignableDigitalResource) |
| [Grading Profile](#gradingProfile) | [AssignableEvent](#assignableEvent) | [AssignableDigitalResource](#assignableDigitalResource), [Result](#result), [Score](#score) |
| \*[Entity Management Profile](#entityMgmtProfile) | [EntityMgmtEvent](#entityMgmtEvent), [ViewEvent](#viewEvent) | [AssignableDigitalResource](#assignableDigitalResource)
\*Proposed for Caliper 1.2

### Open Questions
* Do we need a Rubric profile?
* Are Rubric-related entities also assignable?
* Is it sufficient to link an [AssignableDigitalResource](#assignableDigitalResource)
(e.g. [AssessmentItem](#assessmentItem)) to a [Rubric](./rubric.md) or do we need
to be able to link it to an individual [RubricItem](./rubricItem)?
* What additional metadata (e.g. properties) do we need to add to Rubric](./rubric.md) and [RubricItem](./rubricItem)?

[Rubric](./rubric.md)
* scoreBounds<?> (Criteria and point values)
* weighting?

[RubricItem](./rubricItem)
* scoringType\<string\> (constant values: negative scoring, positive scoring)
* pointValue\<int\>

<a rel="license" href="http://creativecommons.org/licenses/by-nd/4.0/">
<img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nd/4.0/88x31.png" /></a>
<br />
This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nd/4.0/">Creative Commons Attribution-NoDerivatives 4.0 International License</a>.
