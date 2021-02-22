# Features

A feature is an ability your character has that has text that should be displayed.

## Components

### Name

The name of the feature, which will appear at the top of the feature's card on the features tab.

### Summary

A brief summary of the feature, which will appear beneath the name of the feature on the features tab. This field accepts markdown, HTML, and calculations within {}.

### Description

A long description of the feature, which will appear when you click on the feature's name or summary on the features tab. This field accepts markdown, HTML, and calculations within {}.

### Tags

Tags are used to control which slots this property can be added to. This will usually be left blank unless you're making a library.

## Accessible Values

### name\*

The name of the feature.

### summary\*

The text entered into the summary field of the feature, unparsed.

### description\*

The text entered into the description field of the feature, unparsed.

{% hint style="warning" %}
All values marked with a \* can only be accessed using an ancestor reference.
{% endhint %}

