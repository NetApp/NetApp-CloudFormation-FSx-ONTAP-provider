# NetApp::FSxN::ClusterPeer ClusterPeerStatus

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "<a href="#state" title="State">State</a>" : <i>String</i>,
    "<a href="#updatetime" title="UpdateTime">UpdateTime</a>" : <i>String</i>
}
</pre>

### YAML

<pre>
<a href="#state" title="State">State</a>: <i>String</i>
<a href="#updatetime" title="UpdateTime">UpdateTime</a>: <i>String</i>
</pre>

## Properties

#### State

_Required_: No

_Type_: String

_Allowed Values_: <code>available</code> | <code>partial</code> | <code>unavailable</code> | <code>pending</code> | <code>unidentified</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### UpdateTime

The last time the state was updated.

_Required_: No

_Type_: String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

