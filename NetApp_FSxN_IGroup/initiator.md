# NetApp::FSxN::IGroup Initiator

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "<a href="#name" title="Name">Name</a>" : <i>String</i>
}
</pre>

### YAML

<pre>
<a href="#name" title="Name">Name</a>: <i>String</i>
</pre>

## Properties

#### Name

The FC WWPN, iSCSI IQN, or iSCSI EUI that identifies the host initiator.

_Required_: Yes

_Type_: String

_Pattern_: <code>^(?:iqn\.[0-9]{4}-[0-9]{2}\.([a-zA-Z0-9-]+\.)+[a-zA-Z0-9-]+:[^:]+$|eui\.[0-9A-Fa-f]{16}$|[0-9a-fA-F]{2}(:[0-9a-fA-F]{2}){7}$)</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

