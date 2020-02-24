{:.py-4 .mt-4 #subjects}
***

## Subjects Page

{% include bootstrap/image.md img="/theme/subjects.jpg" %}

{% capture subject-text %}
- **subjects-page**: Turns subject generation on (`true`) or off (`false`). 
	- `false` lowers dev build time (Note: If you turn it off, the page won't work!!)
	- Options: `true`, `false`
	- example --> `subjects-off: false`

- **subjects-fields**: Chooses metadata fields from your collection metadata CSV to be included in the Subjects page tag cloud.
	- Multiple fields must be separated by a semi-colon(`;`)
	- example --> `subject;creator`

- **subjects-min**: Minimum number of times a subject term must appear before being displayed in the tag cloud. 
	- Use this to improve load and build times. Too many terms = slow load time!
	- Range: `1` - `30` (note that a really large number will likely make no subjects appear)
	- example --> `subject-min: 4`

- **subjects-stopwords**: A set of words/phrases to be removed from the tag cloud.
	- Multiple fields must be separated by a semi-colon(`;`)
	- example --> `stopwords: boxers;boxing;boxer`
{% endcapture %}

{% include bootstrap/card.md text=subject-text %}