# NetApp::FSxN::SnapshotPolicy SnapshotPolicyCopy

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "<a href="#count" title="Count">Count</a>" : <i>Integer</i>,
    "<a href="#schedulename" title="ScheduleName">ScheduleName</a>" : <i>String</i>,
    "<a href="#prefix" title="Prefix">Prefix</a>" : <i>String</i>,
    "<a href="#retentionperiod" title="RetentionPeriod">RetentionPeriod</a>" : <i>String</i>,
    "<a href="#snapmirrorlabel" title="SnapmirrorLabel">SnapmirrorLabel</a>" : <i>String</i>
}
</pre>

### YAML

<pre>
<a href="#count" title="Count">Count</a>: <i>Integer</i>
<a href="#schedulename" title="ScheduleName">ScheduleName</a>: <i>String</i>
<a href="#prefix" title="Prefix">Prefix</a>: <i>String</i>
<a href="#retentionperiod" title="RetentionPeriod">RetentionPeriod</a>: <i>String</i>
<a href="#snapmirrorlabel" title="SnapmirrorLabel">SnapmirrorLabel</a>: <i>String</i>
</pre>

## Properties

#### Count

The number of snapshot copies to maintain for this schedule.

_Required_: Yes

_Type_: Integer

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### ScheduleName

Schedule name at which snapshot copies are captured on the volume.

_Required_: Yes

_Type_: String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Prefix

The prefix to use while creating snapshot copies at regular intervals.

_Required_: No

_Type_: String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### RetentionPeriod

The retention period of snapshot copies for this schedule. The retention period value represents a duration and must be specified in the ISO-8601 duration format. The retention period can be in years, months, days, hours, and minutes. A period specified for years, months, and days is represented in the ISO-8601 format as 'PY', 'PM', 'PD' respectively, for example 'P10Y' represents a duration of 10 years. A duration in hours and minutes is represented by 'PTH' and 'PTM' respectively. The period string must contain only a single time element that is, either years, months, days, hours, or minutes. A duration which combines different periods is not supported, for example 'P1Y10M' is not supported.

_Required_: No

_Type_: String

_Pattern_: <code>^(P(\d+Y|\d+M|\d+D|T\d+H|T\d+M))$</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### SnapmirrorLabel

Label for SnapMirror operations. SnapMirror Label name must contain at least one character and must not contain leading or trailing white space.

_Required_: No

_Type_: String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

