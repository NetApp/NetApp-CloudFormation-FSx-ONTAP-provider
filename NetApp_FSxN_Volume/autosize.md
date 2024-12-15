# NetApp::FSxN::Volume Autosize

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "<a href="#mode" title="Mode">Mode</a>" : <i>String</i>,
    "<a href="#minimum" title="Minimum">Minimum</a>" : <i>Double</i>,
    "<a href="#maximum" title="Maximum">Maximum</a>" : <i>Double</i>,
    "<a href="#growthreshold" title="GrowThreshold">GrowThreshold</a>" : <i>Integer</i>,
    "<a href="#shrinkthreshold" title="ShrinkThreshold">ShrinkThreshold</a>" : <i>Integer</i>
}
</pre>

### YAML

<pre>
<a href="#mode" title="Mode">Mode</a>: <i>String</i>
<a href="#minimum" title="Minimum">Minimum</a>: <i>Double</i>
<a href="#maximum" title="Maximum">Maximum</a>: <i>Double</i>
<a href="#growthreshold" title="GrowThreshold">GrowThreshold</a>: <i>Integer</i>
<a href="#shrinkthreshold" title="ShrinkThreshold">ShrinkThreshold</a>: <i>Integer</i>
</pre>

## Properties

#### Mode

Autosize mode for the volume.

_Required_: No

_Type_: String

_Allowed Values_: <code>grow</code> | <code>grow_shrink</code> | <code>off</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Minimum

Minimum size in bytes up to which the volume shrinks automatically. This size cannot be greater than or equal to the maximum size of volume.

_Required_: No

_Type_: Double

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Maximum

Maximum size in bytes up to which a volume grows automatically. This size cannot be less than the current volume size, or less than or equal to the minimum size of volume.

_Required_: No

_Type_: Double

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### GrowThreshold

Used space threshold size, in percentage, for the automatic growth of the volume. When the amount of used space in the volume becomes greater than this threhold, the volume automatically grows unless it has reached the maximum size. The volume grows when 'space.used' is greater than this percent of 'space.size'. The 'grow_threshold' size cannot be less than or equal to the 'shrink_threshold' size.

_Required_: No

_Type_: Integer

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### ShrinkThreshold

Used space threshold size, in percentage, for the automatic shrinkage of the volume. When the amount of used space in the volume drops below this threshold, the volume automatically shrinks unless it has reached the minimum size. The volume shrinks when the 'space.used' is less than the 'shrink_threshold' percent of 'space.size'. The 'shrink_threshold' size cannot be greater than or equal to the 'grow_threshold' size.

_Required_: No

_Type_: Integer

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

