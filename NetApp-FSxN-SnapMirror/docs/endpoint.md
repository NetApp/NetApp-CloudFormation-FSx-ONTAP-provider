# NetApp::FSxN::SnapMirror Endpoint

The endpoint of the SnapMirror relationship.

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "<a href="#svm" title="SVM">SVM</a>" : <i><a href="namewithuuidref.md">NameWithUuidRef</a></i>,
    "<a href="#volume" title="Volume">Volume</a>" : <i>String</i>
}
</pre>

### YAML

<pre>
<a href="#svm" title="SVM">SVM</a>: <i><a href="namewithuuidref.md">NameWithUuidRef</a></i>
<a href="#volume" title="Volume">Volume</a>: <i>String</i>
</pre>

## Properties

#### SVM

_Required_: Yes

_Type_: <a href="namewithuuidref.md">NameWithUuidRef</a>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### Volume

_Required_: Yes

_Type_: String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

