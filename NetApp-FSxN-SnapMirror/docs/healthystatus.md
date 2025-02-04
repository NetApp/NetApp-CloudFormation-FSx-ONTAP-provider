# NetApp::FSxN::SnapMirror HealthyStatus

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "<a href="#healthy" title="Healthy">Healthy</a>" : <i>Boolean</i>,
    "<a href="#unhealthyreason" title="UnhealthyReason">UnhealthyReason</a>" : <i>[ String, ... ]</i>
}
</pre>

### YAML

<pre>
<a href="#healthy" title="Healthy">Healthy</a>: <i>Boolean</i>
<a href="#unhealthyreason" title="UnhealthyReason">UnhealthyReason</a>: <i>
      - String</i>
</pre>

## Properties

#### Healthy

Indicates whether the relationship is healthy.

_Required_: No

_Type_: Boolean

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### UnhealthyReason

Reason the relationship is not healthy.

_Required_: No

_Type_: List of String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

