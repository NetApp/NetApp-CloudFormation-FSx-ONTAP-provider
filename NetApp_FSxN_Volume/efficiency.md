# NetApp::FSxN::Volume Efficiency

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "<a href="#compaction" title="Compaction">Compaction</a>" : <i>String</i>,
    "<a href="#compression" title="Compression">Compression</a>" : <i>String</i>,
    "<a href="#dedupe" title="Dedupe">Dedupe</a>" : <i>String</i>,
    "<a href="#crossvolumededupe" title="CrossVolumeDedupe">CrossVolumeDedupe</a>" : <i>String</i>
}
</pre>

### YAML

<pre>
<a href="#compaction" title="Compaction">Compaction</a>: <i>String</i>
<a href="#compression" title="Compression">Compression</a>: <i>String</i>
<a href="#dedupe" title="Dedupe">Dedupe</a>: <i>String</i>
<a href="#crossvolumededupe" title="CrossVolumeDedupe">CrossVolumeDedupe</a>: <i>String</i>
</pre>

## Properties

#### Compaction

_Required_: No

_Type_: String

_Allowed Values_: <code>inline</code> | <code>none</code> | <code>mixed</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Compression

_Required_: No

_Type_: String

_Allowed Values_: <code>inline</code> | <code>background</code> | <code>both</code> | <code>none</code> | <code>mixed</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Dedupe

_Required_: No

_Type_: String

_Allowed Values_: <code>inline</code> | <code>background</code> | <code>both</code> | <code>none</code> | <code>mixed</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### CrossVolumeDedupe

_Required_: No

_Type_: String

_Allowed Values_: <code>inline</code> | <code>background</code> | <code>both</code> | <code>none</code> | <code>mixed</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

