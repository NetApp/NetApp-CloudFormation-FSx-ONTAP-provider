# NetApp::FSxN::Volume Snaplock

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "<a href="#snaplocktype" title="SnaplockType">SnaplockType</a>" : <i>String</i>,
    "<a href="#minimumretention" title="MinimumRetention">MinimumRetention</a>" : <i>String</i>,
    "<a href="#maximumretention" title="MaximumRetention">MaximumRetention</a>" : <i>String</i>,
    "<a href="#defaultretention" title="DefaultRetention">DefaultRetention</a>" : <i>String</i>
}
</pre>

### YAML

<pre>
<a href="#snaplocktype" title="SnaplockType">SnaplockType</a>: <i>String</i>
<a href="#minimumretention" title="MinimumRetention">MinimumRetention</a>: <i>String</i>
<a href="#maximumretention" title="MaximumRetention">MaximumRetention</a>: <i>String</i>
<a href="#defaultretention" title="DefaultRetention">DefaultRetention</a>: <i>String</i>
</pre>

## Properties

#### SnaplockType

The SnapLock type of the volume.

_Required_: No

_Type_: String

_Allowed Values_: <code>compliance</code> | <code>enterprise</code> | <code>non_snaplock</code>

_Update requires_: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

#### MinimumRetention

Specifies the allowed retention period for files committed to the WORM state on the volume. The retention value represents a duration and must be specified in the ISO-8601 duration format. The retention period can be in years, months, days, hours, and minutes. A duration specified for years, month,s and days is represented in the ISO-8601 format as "PY", "PM", "PD" respectively, for example "P10Y" represents a duration of 10 years. A duration in hours and minutes is represented by "PTH" and "PTM" respectively. The retention string must contain only a single time element that is, either years, months, days, hours, or minutes. A duration which combines different periods is not supported, for example "P1Y10M" is not supported. Apart from the duration specified in the ISO-8601 format, the duration field also accepts the string "infinite" to set an infinite retention period.

_Required_: No

_Type_: String

_Pattern_: <code>^(P(\d+Y)?(\d+M)?(\d+D)?(T(\d+H)?(\d+M)?)?|infinite)$</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### MaximumRetention

Specifies the allowed retention period for files committed to the WORM state on the volume. The retention value represents a duration and must be specified in the ISO-8601 duration format. The retention period can be in years, months, days, hours, and minutes. A duration specified for years, month,s and days is represented in the ISO-8601 format as "PY", "PM", "PD" respectively, for example "P10Y" represents a duration of 10 years. A duration in hours and minutes is represented by "PTH" and "PTM" respectively. The retention string must contain only a single time element that is, either years, months, days, hours, or minutes. A duration which combines different periods is not supported, for example "P1Y10M" is not supported. Apart from the duration specified in the ISO-8601 format, the duration field also accepts the string "infinite" to set an infinite retention period.

_Required_: No

_Type_: String

_Pattern_: <code>^(P(\d+Y)?(\d+M)?(\d+D)?(T(\d+H)?(\d+M)?)?|infinite)$</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### DefaultRetention

Specifies the allowed retention period for files committed to the WORM state on the volume. The retention value represents a duration and must be specified in the ISO-8601 duration format. The retention period can be in years, months, days, hours, and minutes. A duration specified for years, month,s and days is represented in the ISO-8601 format as "PY", "PM", "PD" respectively, for example "P10Y" represents a duration of 10 years. A duration in hours and minutes is represented by "PTH" and "PTM" respectively. The retention string must contain only a single time element that is, either years, months, days, hours, or minutes. A duration which combines different periods is not supported, for example "P1Y10M" is not supported. Apart from the duration specified in the ISO-8601 format, the duration field also accepts the string "infinite" to set an infinite retention period.

_Required_: No

_Type_: String

_Pattern_: <code>^(P(\d+Y)?(\d+M)?(\d+D)?(T(\d+H)?(\d+M)?)?|infinite)$</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

