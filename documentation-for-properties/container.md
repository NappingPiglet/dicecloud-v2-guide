# Containers

A container is used to store items in the inventory.

## Components

### Name

The name of the container, which will appear on the inventory tab.

### Carried

When this is set to true, the container will count towards your weight carried.

### Value

The value of the container in GP.

### Weight

The weight of the container in pounds.

### Description

A description of the container, which will appear when you click on the container's name on the inventory tab. This field accepts markdown, HTML, and calculations within {}.

## Advanced

### Tags

Tags are used to control which slots this property can be added to. This will usually be left blank unless you're making a library.

### Contents are Weightless

When this is set to true, only the container's weight will count towards your weight carried. If set to false, items that are stored in the container will also contribute their weight.

## Accessible Values

### name\*

The name of the container.

### carried\*

Returns true if the carried field is currently set to true.

### contentsWeightless\*

Returns true if the contents are weightless field is currently set to true.

### weight\*

Returns the weight of the container.

### value\*

Returns the value of the container in GP.

### description\*

The text entered into the description field of the container, unparsed.

### contentsWeight\*

Currently unimplemented.

### contentsValue\*

Currently unimplemented.

{% hint style="warning" %}
All values marked with a \* can only be accessed using an ancestor reference.
{% endhint %}

