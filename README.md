# novel-outline-sync
Sync a novel outline specified in arbitrary metadata in multiple Markdown files to external files.

## What Problem Is to Be Solved

Novelists as well as any writer of long-form fiction and nonfiction need to structure their ideas
in some kind of outline. Tools for creating and managing such a structure are many and varied
but are often maintained outside of the manuscript (ms) itself and thus over time the outline and ms
diverge and become out-of-sync, resulting in less effective restructuring during the revision process.

## What Are the Constraints

Authors should be able to decide what metadata they want in their outline; some typical kinds
of metadata are: chapter title, POV character, physical location, and the character's goal.
However, they might want things like word count, antagonist, and story beat.

For interoperability with other applications and languages, extensibility, and maintainability,
the data structure for the metadata should be in common use.

Authors would like to write their mss in the tool of their choice; however, that choice needs
to be balanced against practicality.

Authors would like to export and sync the outline metadata to some common file formats such as Word,
LibreOffice Writer, HTML, and spreadsheets. Yet again, these file formats must be balanced
against practicality.

## What are Possible Implementations

The program could be written as a Python script that could be run on Markdown files.
Initially, the program would parse the Markdown files for metadata structures that represent the outline
and export them to a file; for example, a CSV file. Later, the program would sync the metadata structures
in the ms's Markdown files with the CSV file. Alternatively, the program could generate the ms's
Markdown files from the CSV file.

### Metadata Structure

For customization by an author to suit their needs, an arbitrary metadata structure is needed.
Let's start with JSON since it is a popular standard. Here are some examples:

```
{
"story":[
    {"pov":"Chie"},
    {"location:"Abyss of Perturbation"},
    {"Subarc GMC:"Chie must get to the floating island, find her allies, and convince them
    to take her on their airship to Ishigumi where Ken is waiting for her."}
]
}
```

### Referencing the Metadata

### Syncing the Metadata

## Future Enhancements

Because of the arbitrary nature of the metadata structure, the program could export and sync such metadata
to a story-universe file. For example, a story-universe metadata for an item could be the following:

```
{
"idea":[
    {"term":"nanomachine Tengu mask"},
    {"abbreviation":"ntm"},
    {"category":"item"},
    {"definition":"A Tengu mask that cannibalizes body cells into oxygen;
                    used at high-altitudes."}
]
}
```
