Sen probably makes sense.

※Another languages : [日本語🎌](./docs/ja/README.md) | ...

# sen
省エネ (saving energy) notation. That is sen.

## ◆Idea
### ・Dreaming of type-safe CSV (comma-separated values)
JSON is not very good at passing large sets of records. On the other hand, CSV does not support data structuring and typing.
### ・Reach out to the Machines
Seeking to be both human-friendly and machine-readable. Allows you to describe hints that are useful for machine analysis.
### ・Metadata Isolation
Probably no one wants to pollute the payload or file names with metadata.  
You also don't want to worry about whether the CSV has a header or not.  
Sen contributes to interoperability by providing a generic standard metadata notation.
It allows programs to access meta information with generic code and register the data with BI tools without any hassle.
### ・Multiple text data management
Subprojects provide an access strategy for data across multiple files.

## ◆Considerations
1. Sen must be provided to the spreadsheet software as secure and manageable data.
1. Sen must achieve human friendliness and machine readability.
1. Sen must be designed to be capable of receiving advanced support from the editor software.
1. Sen must provide data structures that are easily accessible from major programming languages.
1. Sen must support row-by-row reading. (More precisely, sequential reading.)
1. Sen must support adding data to the end of a file.
1. Sen must be able to minify under a simple rule.

## ◆Future Targets
1. Interface Description
1. Type versioning
1. Portable function set (low priority)

## ◆
Please feel free to create an Issue if you have any questions or comments.
I'm also waiting for a correction in English grammar.
