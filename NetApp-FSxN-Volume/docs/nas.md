# NetApp::FSxN::Volume NAS

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "<a href="#securitystyle" title="SecurityStyle">SecurityStyle</a>" : <i>String</i>,
    "<a href="#junctionpath" title="JunctionPath">JunctionPath</a>" : <i>String</i>,
    "<a href="#exportpolicy" title="ExportPolicy">ExportPolicy</a>" : <i>String</i>
}
</pre>

### YAML

<pre>
<a href="#securitystyle" title="SecurityStyle">SecurityStyle</a>: <i>String</i>
<a href="#junctionpath" title="JunctionPath">JunctionPath</a>: <i>String</i>
<a href="#exportpolicy" title="ExportPolicy">ExportPolicy</a>: <i>String</i>
</pre>

## Properties

#### SecurityStyle

Security style associated with the volume.

_Required_: No

_Type_: String

_Allowed Values_: <code>mixed</code> | <code>ntfs</code> | <code>unix</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### JunctionPath

The fully-qualified path in the owning SVM's namespace at which the volume is mounted.

_Required_: No

_Type_: String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### ExportPolicy

Export Policy associated with the volume.

_Required_: No

_Type_: String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

