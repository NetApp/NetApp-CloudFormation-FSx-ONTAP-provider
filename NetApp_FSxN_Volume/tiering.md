# NetApp::FSxN::Volume Tiering

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "<a href="#policy" title="Policy">Policy</a>" : <i>String</i>,
    "<a href="#mincoolingdays" title="MinCoolingDays">MinCoolingDays</a>" : <i>Integer</i>
}
</pre>

### YAML

<pre>
<a href="#policy" title="Policy">Policy</a>: <i>String</i>
<a href="#mincoolingdays" title="MinCoolingDays">MinCoolingDays</a>: <i>Integer</i>
</pre>

## Properties

#### Policy

Policy that determines whether the user data blocks of a volume in a FabricPool will be tiered to the cloud store when they become cold.

_Required_: Yes

_Type_: String

_Allowed Values_: <code>all</code> | <code>auto</code> | <code>none</code> | <code>snapshot_only</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### MinCoolingDays

This parameter specifies the minimum number of days that user data blocks of the volume must be cooled before they can be considered cold and tiered out to the cloud tier.

_Required_: No

_Type_: Integer

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

