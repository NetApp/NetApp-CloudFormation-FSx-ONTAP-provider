# NetApp::FSxN::Volume Clone

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "<a href="#parentsvm" title="ParentSVM">ParentSVM</a>" : <i><a href="namewithuuidref.md">NameWithUuidRef</a></i>,
    "<a href="#parentvolume" title="ParentVolume">ParentVolume</a>" : <i><a href="namewithuuidref.md">NameWithUuidRef</a></i>,
    "<a href="#parentsnapshot" title="ParentSnapshot">ParentSnapshot</a>" : <i><a href="namewithuuidref.md">NameWithUuidRef</a></i>,
    "<a href="#iscloned" title="IsCloned">IsCloned</a>" : <i>Boolean</i>
}
</pre>

### YAML

<pre>
<a href="#parentsvm" title="ParentSVM">ParentSVM</a>: <i><a href="namewithuuidref.md">NameWithUuidRef</a></i>
<a href="#parentvolume" title="ParentVolume">ParentVolume</a>: <i><a href="namewithuuidref.md">NameWithUuidRef</a></i>
<a href="#parentsnapshot" title="ParentSnapshot">ParentSnapshot</a>: <i><a href="namewithuuidref.md">NameWithUuidRef</a></i>
<a href="#iscloned" title="IsCloned">IsCloned</a>: <i>Boolean</i>
</pre>

## Properties

#### ParentSVM

_Required_: Yes

_Type_: <a href="namewithuuidref.md">NameWithUuidRef</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### ParentVolume

_Required_: Yes

_Type_: <a href="namewithuuidref.md">NameWithUuidRef</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### ParentSnapshot

_Required_: No

_Type_: <a href="namewithuuidref.md">NameWithUuidRef</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### IsCloned

Setting 'IsCloned' attribute to false splits the clone from its parent volume.

_Required_: No

_Type_: Boolean

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

