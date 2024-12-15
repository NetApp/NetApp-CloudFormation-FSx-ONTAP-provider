# NetApp::FSxN::SnapMirror SnapMirrorDestinationCreation

Use this object to provision the destination endpoint when establishing a SnapMirror relationship for a volume. For FlexGroup SnapMirror relationships, the source and destination FlexGroups must be spread over the same number of aggregates with the same number of constituents per aggregate.

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "<a href="#enabled" title="Enabled">Enabled</a>" : <i>Boolean</i>,
    "<a href="#aggregates" title="Aggregates">Aggregates</a>" : <i>[ String, ... ]</i>
}
</pre>

### YAML

<pre>
<a href="#enabled" title="Enabled">Enabled</a>: <i>Boolean</i>
<a href="#aggregates" title="Aggregates">Aggregates</a>: <i>
      - String</i>
</pre>

## Properties

#### Enabled

_Required_: Yes

_Type_: Boolean

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Aggregates

Aggregate name list hosting the volume.

_Required_: Yes

_Type_: List of String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

