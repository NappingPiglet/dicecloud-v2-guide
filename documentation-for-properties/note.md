# Notes

A note is a way to record miscellaneous on the persona tab, whether this is a note of something that needs to be done, your build for different levels or information about your character. It can also serve as a way to store information for users in libraries.

## Components

### Name

The name of the note, which will appear above the description in the persona tab.

### Description

The text of the note. This field accepts Markdown, HTML, and calculations within {}. This will appear when you click on the note, whether from the persona page or from another property.

### Tags

Tags are used to control which slots this property can be added to. This will usually be left blank unless you're making a library.

## Accessible Values

Note that all values listed here can only be accessed using the `#note.<valueName>` syntax from a child of the property.

### name

Returns the name of the note.

### description

Returns the text entered into the description field, unparsed.
