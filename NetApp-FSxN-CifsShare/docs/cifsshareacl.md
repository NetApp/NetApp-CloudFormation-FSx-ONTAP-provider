# NetApp::FSxN::CifsShare CifsShareAcl

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "<a href="#permission" title="Permission">Permission</a>" : <i>String</i>,
    "<a href="#type" title="Type">Type</a>" : <i>String</i>,
    "<a href="#userorgroup" title="UserOrGroup">UserOrGroup</a>" : <i>String</i>
}
</pre>

### YAML

<pre>
<a href="#permission" title="Permission">Permission</a>: <i>String</i>
<a href="#type" title="Type">Type</a>: <i>String</i>
<a href="#userorgroup" title="UserOrGroup">UserOrGroup</a>: <i>String</i>
</pre>

## Properties

#### Permission

Access rights that a user or group has on the defined CIFS Share

_Required_: Yes

_Type_: String

_Allowed Values_: <code>no_access</code> | <code>read</code> | <code>change</code> | <code>full_control</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Type

Type of the user or group to add to the access control list on the defined CIFS share

_Required_: Yes

_Type_: String

_Allowed Values_: <code>windows</code> | <code>unix_user</code> | <code>unix_group</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### UserOrGroup

User or group name to add to the access control list on the defined CIFS share

_Required_: Yes

_Type_: String

_Pattern_: <code>^[a-zA-Z0-9_-]{1,256}$</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

